# Pythontimers

Timers object to simulate hardware timer function of executing cyclic functions without blocking and a very simple API.

```python

>>from pythontimers import SoftTimer

>>def myfunction(message, value):
>>    print("The message is %s, with value of %d." % (message, value))
    
>>timer0 = SoftTimer(0.1, myfunction, "my args", 1)

>>timer0.start()

            
```

The response will be like: "*The message is my args, with value of 1.*"


Defined functions by in this class:

SoftTimer(*period*, *callback*, **args*) -> timer object

​	period in seconds

SoftTimer.**start()**

​	Starts the timer.

SoftTimer.**stop()**

​	Stops the timer.



PS. The timer needs at least one loop iteration to correct the callback execution time
