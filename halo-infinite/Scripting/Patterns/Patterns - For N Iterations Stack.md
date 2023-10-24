# For N Iterations Stack
We are provided the Branch node for creating branches in execution, but it can get complicated and be extremely inefficient to use nested branches, especially when there are things that need to always be checked, and thus have to be duplicated to make sure they would always be processed. 

One way to work around this is to use Custom Events and have multiple outputs, or to just use multiple copies of the initial trigger, each with their own output. The issue with both of these is that you don't have control over execution order. It will be deterministic, with some of that hinging on the order objects and nodes were placed in, but it won't be something you can influence in any reasonable way. 

The For N Iterations Stack solves this issue by providing a way to string a bunch of branch statements together without them having to directly flow into each other while also providing an easy to read structure on the screen.

## Understanding the For N Iterations Node

The For N Iterations node is a basic loop for running a series of actions N times. By setting the value of the N pin to 1 (iteration), it can be used to run a series of actions one time and then execute a final action upon completion. 

This can be helpful in avoiding the need for duplicate nodes in a circuit or event triggers, which can create clutter and require additional events to be created.

Note: when using the For N Iterations node is that data cannot be passed automatically between the current iteration and the continued execution. Instead, local or object scope variables can be used to pass data between each circuit attached to each For N Iterations node.

Overall, the For N Iterations node can be a powerful tool for executing a series of actions once and then performing a final action upon completion, without creating clutter or requiring duplicate nodes.

## How to Implement The Pattern

- Place your initial trigger for this circuit. 
- Place For N Iterations and Branch nodes.
- Set the value on the N pins of each For N Iterations node to 1.
- Attach a Branch node to the Execute Iteration pin of each For N Iterations node.
- Connect the execution output of the initial trigger to the input of the first For N Iterations node.
- Connect the On Completion pin of the first For N Iterations node to the second.
- Connect data inputs of the Branch nodes to relevant data or set manually to use similar to dipswitches.

#### Contributors
Captain Punch
AgentZero
