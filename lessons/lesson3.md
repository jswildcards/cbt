# Lesson 3: Using Artec Robo

## DC Motors
```python
from pyatcrobo2.parts import DCMotor
import time

dcm = DCMotor('M1')
dcm.power(100)
dcm.cw()

time.sleep(5)

dcm.ccw()

time.sleep_ms(5000)

dcm.stop()
```

## Servomotors
```python
from pyatcrobo2.parts import Servomotor
import time

servo = Servomotor('P13') 
servo.set_angle(0)

time.sleep_ms(1000)

servo.set_angle(180)
```

## IR Photoreflectors
```python
from pyatcrobo2.parts import IRPhotoReflector
import time

ir = IRPhotoReflector('P0') 

while True:
    value = ir.get_value()
    print(value)
    time.sleep_ms(500)
```

## Ultrasonic Sensors
```python
from pyatcrobo2.parts import UltrasonicSensor
import time

us = UltrasonicSensor('P1')

while True:
    distance = us.get_distance()
    print(distance)
    time.sleep_ms(1000)
```

## Color Sensors
```python
from pyatcrobo2.parts import ColorSensor
from pystubit.board import button_a
import time

cs = ColorSensor('I2C')

while True:
    if button_a.is_pressed():
        values = cs.get_values()
        print(values)
        time.sleep_ms(1000)
```
