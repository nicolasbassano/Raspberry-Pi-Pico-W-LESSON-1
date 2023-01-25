To make the Pico recognizable we need to first press the “bootsel” button on the Pico and then plug it in.

Download MicroPython for the Raspberry Pi Picco W

[https://www.raspberrypi.com/documentation/microcontrollers/micropython.html](https://www.raspberrypi.com/documentation/microcontrollers/micropython.html)

Install MicroPython by drag and dropping  the downloaded file into the Pico (in the file explorer). After that the Pico will reboot.

Download and install Thonny IDE from [https://thonny.org/](https://thonny.org/)

---

Once you start Thonny you need to select the MicroPython on the bottom right of Thonny.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bd6e5ffb-d21a-42fc-8830-355aa1dce8c7/Untitled.png)

---

Run our first program…

```python
print('Hello World!')
```

To run the script click on the green play button or hit F5…

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8c3d6786-bc85-41f1-9b4d-e4d7695d175d/Untitled.png)

---

Lets code something more interesting…

```python
from machine import Pin  # machine library, Pin method
myLED=Pin('LED',Pin.OUT) # creates myLED object that sets the LED (special pin) as an output
myLED.value(1)           # Sets the value of the object to 1. 1 is equal to ON. 0 is off.
```

This will work too…

```python
from machine import Pin
myLED=Pin('LED',Pin.OUT) 
myLED.on()
```

```python
from machine import Pin
myLED=Pin('LED',Pin.OUT) 
myLED.off()
```

Lets make it blink…

For this wee need the “time” library and the “sleep” method and use a “while loop” too…

```python
from machine import Pin
from time import sleep
myLED=Pin('LED',Pin.OUT)
while True:
    myLED.value(1)
    sleep(1)
    myLED.value(0)
    sleep(1)
```

This will make it blink faster…

```python
from machine import Pin
from time import sleep
myLED=Pin('LED',Pin.OUT)
while True:
    myLED.value(1)
    sleep(.1)
    myLED.value(0)
    sleep(.1)
```

We could also toggle the blinking…

```python
from machine import Pin
from time import sleep
myLED=Pin('LED',Pin.OUT)
while True:
    myLED.toggle()
    sleep(1)
```

---

Homework

=======

-Write the code we learned without checking the lesson.

-Make the LED blink faster until you can’t notice the blinking.
