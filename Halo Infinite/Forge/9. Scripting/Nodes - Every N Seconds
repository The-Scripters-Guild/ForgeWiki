# Every N Seconds

If you need an "Every N Seconds" event to fire more frequently than the 0.10 second limit present on the node, you can use a workaround by passing a number from another node into the Seconds pin.

If you set the value to 0 this way, it will fire at tick rate, which can vary both during a game and between modes. 4v4 modes simulate at 60hz, while BTB simulates at 30Hz, in matchmaking, for instance.

By dividing two numbers, you can pass any quotient refresh rate you want it to run at. However, be aware that if you set it too low, it may result in visual jitter and issues related to calls being exceeded that tick.

In testing, setting the refresh rate to 1/60 resulted in visual jitter and issues, while setting it to 1/59 gave the smoothest performance of scripts that relied on it to do things like set velocity.

This workaround can be useful if you need more precise control over the timing of your events in your scripts.