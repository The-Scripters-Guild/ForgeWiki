# Node Operations - Mutate vs. Non-Mutate

*The goal of this write up is to address common misconceptions and try to help frame the node execution process in an easy to understand way - regardless of prior programming knowledge. Please do not skim this, as many examples intentionally show bad approaches.*

**First Scenario**
So you are creating your first script and you are trying to add to a number every time a player is killed, this is the script you have so far.
You are declaring a local Scope Number variable with an initial value of 0. You are then Getting that Number and adding 1 to it, and printing that to the Killfeed.

Image https://cdn.discordapp.com/attachments/1050097501178433637/1050097501375582238/image.png

If you are familiar with programming, this might intuitively look like this:
```
let number = new Number(0);
number++;
console.log(number);
//The above changes Number from 0 to 1 and logs 1.
```

However, what is really happening is this:
```
let number = new Number(0);
console.log(number+1);
//The above does NOT change Number, but logs 1.
```

For those without programming knowledge, the pitfall of the script above is that it is not actually modifying the number variable. Instead it is simply logging that variable + 1, which is fine for a log - but since we didn't actually save that new number to the variable, the variable's value is still 0.

So how would we add/subtract etc. to a variable in a way that is saved?

It seems counter intuitive at first, but you need to Set that variable to a new value, and for that value to be the variable's value + 1.

Image https://cdn.discordapp.com/attachments/1050097501178433637/1050098391281053736/image.png

Now we have a new problem, we go to test the script and it is logging 2 the first time a player is killed, what's happening?

Whenever a "Data" Node is called, (like Add, Subtract, etc.) it's data output pin is calculated at the time it is called.

The above script is adding 1 to 0, then setting the number variable to that operation's output (which is 1). Then, the Print Number to Killfeed Node triggers, and since it's connected to the Add Node, Add calculates a new number for it's output. In this case, it adds 1 to the current value of the variable (1), which is 2, and prints it to the killfeed. You can resolve this by simply connecting Get Number Variables output number to your Print Number to Killfeed Node input number.

When Get Number Variable is called, it provides the current value of that variable. This means that even though we are connecting multiple nodes to it, each node will receive the current value of that variable at the time that node is executed. Since execution is sequential, you can trust that it will always provide an accurate output. In this example, it will always print the number variable's value after we have added 1. 

Image https://cdn.discordapp.com/attachments/1050097501178433637/1050101065938378793/image.png

This is an example of a non-mutating operation. Even though we are modifying the number variable, we are doing so explicitly via the Set Variable Type Nodes.

Math nodes like Add simply perform an operation based on it's inputs, and provide an output which can be called upon by the nodes it is connected to. It is an extremely powerful system which allows you to chain together a series of calculations and call upon it multiple times within the same script. (Like using an Add or Subtract's output based on a branch in your script). 

#### Contributors
Captain Punch
AgentZero