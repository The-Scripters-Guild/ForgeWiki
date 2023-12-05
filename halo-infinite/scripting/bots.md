# Bots

### Spawning Multiple Bots at Once via Script

When spawning bots via scripts, it's crucial to introduce a 0.3-second delay between each spawn event to ensure that the bots will be added to the match.

### Team Changes and Bot Replacement

Upon a bot changing teams, it is automatically replaced with a new bot. However, when a bot's Free-For-All (FFA) affiliation is altered, the bot is not replaced.&#x20;

### Blocking Bot Spawns at Round Start

To prevent bot spawns at the beginning of a game, developers need to implement the blocking mechanism at Round Start with no delay.&#x20;

### Bot Interaction with Vehicles

Bots in a game environment can be forced to enter vehicles, expanding gameplay possibilities. While bots exhibit competent driving skills with Ghosts and Wraiths, users may encounter issues when bots interact with other types of vehicles.

### Player and Bot Slot Limitations

In a game with both players and bots, up to 24 players can join a match that includes 8 bots. However, it's important to note that bots cannot be added to a match that already has all 24 player/bot slots filled.

### UX Code Iteration Issues with Bot Inclusion

Including bots in lists that are iterated over for modifying player User Experience (UX) can lead to complications. Users should be cautious about potential disruptions to UX code when bots are included in lists undergoing iteration.

### Gravity Hammer Shockwave Behavior

Bots with Gravity Hammers still create shockwaves when attacking.

**Contributors**\
Captain Punch\
AddiCt3d 2CHa0s\
Kwatzy\
All Seeing Sage\
Cookies

