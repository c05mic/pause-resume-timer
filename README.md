pause-resume-timer
==================

A generic timer utility that supports pause and resume operations. Can be used for Android as well.

To create a timer, extend the `Timer` class

```
public class ExampleTimer extends Timer{
 
    public ExampleTimer() {
        super();
    }
 
    public ExampleTimer(long interval, long duration){
        super(interval, duration);
    }
 
    @Override
    protected void onTick() {
        System.out.println("onTick called!");
    }
 
    @Override
    protected void onFinish() {
        System.out.println("onFinish called!");
    }
 
}
```

To use the timer:

```
//This creates a timer which will tick every second indefinitely.
Timer oneSecondInfiniteTimer = new ExampleTimer();
 
//This creates a timer which ticks every 2 seconds, and runs for 20 seconds.
Timer twoSecondTimer = new ExampleTimer(2000l, 20000l);
 
//Start the timer.
twoSecondTimer.start();
 
//Pause the timer.
twoSecondTimer.pause();
 
//Resume the timer
twoSecondTimer.resume();
```
