# Lesson 5: Twin-Motor Robocars

## [拼砌教學](https://www.artec-kk.co.jp/school/cl/textbooks/material_en/topic_6-1/6-1_build_E.pdf)

## [完整編碼](./lesson5_extra.md)

## 初始化機械車

```python
from pyatcrobo2.parts import DCMotor
import time

dcm_l = DCMotor('M1')
dcm_r = DCMotor('M2')

dcm_l.power(100)
dcm_r.power(100)
```

## 向前行

```python
def move_forward():
    dcm_l.ccw()
    dcm_r.ccw()
```

## 向後倒退

```python
def move_backward():
    dcm_l.cw()
    dcm_r.cw()
```

## 向左旋轉

```python
def spin_left():
    dcm_l.cw()
    dcm_r.ccw()
```

## 向右旋轉

```python
def spin_right():
    dcm_l.ccw()
    dcm_r.cw()
```

## 向左轉

```python
def turn_left():
    dcm_l.brake()
    dcm_r.ccw()
```

## 向右轉

```python
def turn_right():
    dcm_l.ccw()
    dcm_r.brake()
```

## 停止（有緩衝）

```python
def stop():
    dcm_l.stop()
    dcm_r.stop()
```

## 立即停止（沒有緩衝）

```python
def brake():
    dcm_l.brake()
    dcm_r.brake()
```
