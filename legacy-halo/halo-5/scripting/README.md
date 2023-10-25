---
description: >-
  Scripting is a type of user-level object manipulation, first featured in Halo
  2: Anniversary, and included with Forge in the Infinity's Armory update to
  Halo 5: Guardians. It reappeared in the Windows
---

# Scripting

_This information was compiled for your use as a reference and learning resource. Please keep in mind that Halo 5 Forge updates over the years, including but not limited to the huge Monitor's Bounty update, means you may find information that is no longer relevant or was modified in an update. We're working to get this info up-to-date. Feel free to contact staff if you find deprecated information, when they can forward your concern to the appropriate team for correction._

***

### Scripting In Halo 5: Guardians

In Halo 5: Guardians, scripting is used by Forgers to manipulate objects. Much like the game dev counterpart, scripting involves sequences of "When" (**Conditions**) and "Do" (**Actions**). With the scripting interface, players input "When" Condition(s), which upon validation, triggers "Do" Action(s). Scripts allow Forgers to make their maps function dynamically by tracking events, moving and rotating object(s), sending message(s), and more.

Most of the objects in Forge can be given scripts, up to 8. Each Script is created with one Condition and one Action, and additional Actions can be added, up to four. The Conditions check if certain events occur in the game. Some events are specific to the **object**, such as spawning or taking damage. Other events are observed by all objects in the game, such as **message broadcasts** or **timer events**.

When the Condition of a Script is met, it executes its Actions. Some Actions are universal (sending messages or power changes), but most are **object specific** and do things like move the object or change its color.

Scripts seem to be processed for every game cycle, which is each round of calculations and graphics generation done by the game. In testing, scripts ran 60 times a second (which matches Halo 5's targeted frame rate), though it might vary a little.

#### Script Execution Order

During gameplay, events happen: objects spawn, timers occur, objects take damage, players interact with switches, etc. When these happen, the game “broadcasts” events that our script Conditions listen for. In each cycle, the Conditions are first checked to see if their events happened, and the Actions of those scripts are run one script at a time in a fixed order.

**Scripts are evaluated in order by earliest to latest** Generally, the first/earliest scripts added to the map are evaluated first. It seems to actually have an array that contains the scripts and the lowest-numbered available slot is where a new script gets added. Think of the scripts as having a hidden number (1 to max 512) that doesn't change & removing a script leaves its array slot open. If there are no open slots from deleted scripts, a new script gets the number = the current script count +1.

_There are exceptions, here is one of the biggest GOTCHAS! in Halo 5 Scripting! Deleting a script in one object (Tommy) can cause the next script added to another object (Olive) to run earlier than that (Olive) object's lower-numbered scripts because that next added script will take the deleted script's place in the order Conditions run. This will effectively change the order your Conditions run, so they will no longer run in the order they were created._

Scripts with Conditions that pass their test then have their Actions executed.

**Actions are executed in order** Once a Script's Condition is triggered, its Actions are executed in the order they were created, so top #1 to bottom #4. If any Actions have a Time interval, later Actions are executed after the Timed one completes.

When Actions execute (or begin if they're timed) on the same object during the same game tick, it seems the conflict is handled by the following behavior:

* The highest number Power Set action wins
* The lowest number Move or Rotate action wins
* Damage: Ratio actions accumulate, so the assigned numbers don't matter
* The highest number Spawn or Despawn script wins

#### Message and Power Channels Intro

**Messages** and **Power State** changes send broadcasts that all objects on your map can detect. This broadcast system is completely under your control and is the main way to have objects and their Scripts communicate with each other. (There are other ways to have some objects interact with each other, but these are workarounds that are difficult to use and less reliable.)

Forge provides us with 26 message and 26 power channels, both named like the NATO phonetic alphabet (alpha to zulu). Message and power channels of the same name don't affect each other.

Messages and Power State **broadcasts** are simply that: messages. They contain no information or options. When you use the **Message: Send** action, the broadcast is instantly sent for the selected channel and only lasts for that instant (one game tick). Every script that contains the **Message: Received**, **Power: Check**, or **Message/Power: Multi Conditions** will listen and activate their Actions when appropriate.

* These broadcasts are for your customization; the game doesn’t automatically create any broadcasts.
* There are 26 channels to send these broadcasts over. They are named like the NATO radio message standard for spelling the alphabet: alpha, bravo, charlie… zulu.
* Both messages and power channel changes behave like events that will be detected by script conditions on the next script cycle check.

**Messages**

Messages are simple events that you can broadcast from any object that can contain scripts. Any Script that has 'Message: Received' Conditions will listen for a message broadcast being sent over the channel it is listening to (alpha-zulu).

#### Power States

You can use the **Power: Set** Action to attempt to set a State to **On** or **Off** or to **Toggle** it from whatever its current value is. When a Script Action attempts to set a Channel that's On to On, or Off to Off, then no change occurs and no broadcast is sent. When **Toggle** is used, or anytime the State switches between On and Off in either direction, a broadcast is sent.

At the start of a match or Forge session, every channel's Power state seems to behave as if it’s Off.

* Setting it to Off doesn't trigger any scripts.
* Using the Toggle or On options turn it On, and conditions that listen for On events trigger.
* Conditions that listen for Off events don't trigger at match start, so the behavior doesn’t seem like the channels are switched to Off right when the game starts. It's like they were already turned Off before the game started.
* A Multi condition with an On Power condition set to Off will trigger without changing that power state as long as it has another condition that broadcasts and causes it to be evaluated.

**Message/Power: Multi**

The **Message/Power: Multi** Condition includes checks for the current **States** of Power channels. If a Condition checks for a power channel state to be On or Off, then that Condition is true even if the power was set previously. It doesn't have to act like an event that just triggered. Note that at least one of a Multi's conditions needs to be triggered during the previous cycle for the script to activate.

\[Spoiler="Detecting Power State"] **Detecting Power State Broadcasts**

Power broadcasts can be detected by either the Message: Received or Message/Power: Multi conditions. Power: Check simply detects broadcasts for On or Off States. It is only triggered when a Power State changes to the State it's set to listen for (On or Off). It will not detect when an action attempts to set a channel to its current state (no broadcast).

Message/Power: Multi can be quite complicated, but it detects Power change broadcasts just like the Power: Check condition does. It also has a Toggle option which detects a Power broadcast whether it's changed to On or Off. A Multi condition with Minimum of 1 with only one Power condition set to On or Off works exactly like the equivalent Power: Check condition. If the same script is changed to the Toggle setting, it detects both On and Off broadcasts.

**Testing Power State On/Off Values With Multi**

Message/Power: Multi is the only way to test the value of a Power State outside the moments it gets changed and broadcasts. The Power State On and Off conditions within Multi conditions evaluate to true (and count as 1 for the Minimum to trigger setting) whenever that Power State currently has that value. It's not limited to when Power channels broadcast when they change. However, at least one of the conditions set in Multi must be broadcast to trigger the Multi condition.

The Power State Trigger and Message Send conditions within Multi can only trigger as a result of broadcasts. \[/Spoiler]

#### Additional Notes on Scripting in Halo 5

Grouped objects have their own individual scripts. Scripts added to a group are added to each object within. Welding a group does not change this. Welding is, however, necessary to rotate an entire group as if it is a single object. Otherwise, each piece of the group will rotate on its own axis.

#### General Script GOTCHAS!

Following are some general scripting seeming glitches or **Gotchas!**. You will find other more specific **Gotchas!** in their respective sections.

* Normally, Conditions will run in the order they are created. However, deleting a script in one object (Timmy) can cause the next script added to another object (Olive) to run earlier than that (Olive) object's lower-numbered scripts because that next added script will take the deleted script's place in the order Conditions run.
* Number Changes for a currently dirty number can affect any Number Checks for that number that run later (have a higher Map Script Slot number).
* There are three known things that will cause pieces on your map to load crooked in Halo 5 custom games on the Xbox One (they'll work fine in Forge and on PC).
  1. Placing any label on the object, whether via its Properties menu or via the Label Change Action, even if the Action hasn't run. If the label is added via a script, simply removing the script fixes the crooked glitch, but if it was added directly to the piece in Properties the piece must be deleted.
  2. Setting a Spawn Order in the object's Properties menu.
  3. Putting any scripts on the piece.
