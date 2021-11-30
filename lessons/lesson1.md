# Python Programming Basics

[Reference](http://bit.do/winstars_basic-python)

## Your First Python Program

```python
print("Hello world!")
```

## Creating Variables

```python
x = "Hello world!"
print(x)
```

## Variable Types

### Example 1

```python
x = "Hello world!"
print(x)

x = 12345
print(x)

x = 12.3
print(x)
```

### Example 2

```python
x = "Hello world!"
print(type(x))

x = 12345
print(type(x))

x = 12.3
print(type(x))
```

### Example 3

```python
x = True
print(x)
print(type(x))
```

## Mathematical Operators

### Example 1

```python
x = 1
y = 2
z = x + y # - * / % **
print(z)
```

### Example 2

```python
x = '1'
y = '2'
z = x + y
print(z)
```

### Example 3

```python
x = 1
y = '2'
z = x + y
print(z)
```

## Input

```python
x = input("type in something: ")
print(x)
```

## 條件及關係運算子 Conditioning & Relational Operators

### Example 1

```python
x = input("type in 'k': ")
if x == 'k':
  print("correct")
```

### Example 2

```python
x = input("1 + 1 = ? : ")
if x == '2':
  print("correct!")
else:
  print("incorrect!")
```

### Example 3

```python
value = input("input score: ")
value = int(value)

if value >= 90:
  print("A")
elif value > 70:
  print("B")
elif value > 50:
  print("C")
else:
  print("F")
```

## 邏輯運算子 Logical Operators (Logic Gate)

### Example 1

```python
A = True
B = False

print("A and B = " + str(A and B))
print("A or B = " + str(A or B))
print("not A = " + str(not A))
print("not B = " + str(not B))
```

### Example 2

```python
A = True
B = False

if A and (not B):
  print("and")
if A or B:
  print("or")
if not B:
  print("not")
```

## 順序和迴圈 Sequential and Looping

### While-Loop

#### Example 1

```python
x = input("1 + 1 = ? : ")
while x != '2':
  x = input("incorrect! please try again: ")
print("correct!")
```

#### Example 2

```python
while True: # not False:
  x = input("type in something: ")
print(x)
```

#### Example 3

```python
count = 0
while count < 5:
  val = input("type in something: ")
  print(val)
  if val == 'b':
    count += 1
print()
print('end')
```

#### Example 4

```python
count = 0
while count < 5:
  val = input("type in something: ")
  if val == 'b':
    count += 1
  else:
    count = 0
  print("val: " + val + " | count: " + str(count))
  print()

print('end')
```

#### Example 5

```python
count = 0
while count < 10:
  count += 1
  print(count)
print('end')
```

### For-Loop

#### Example 1

```python
for count in range(10):
  print(count)
print('end')
```

#### Example 2

```python
for count in range(1,10,2):
  print(count)
print('end')
```

## Library Import

### Example 1

```python
import time
for count in range(10):
  print(count)
  time.sleep(1)
print('end')
```

### Example 2

```python
from time import sleep
for count in range(10):
  print(count)
  sleep(1)
print('end')
```

## 練習

```python
# e.g. A sensor return values from 0 - 100

# 0 - 100 --> black to white

# write a program to separate 2 scenes

while True:
  sensor_value = int(input("Your sensor value: "))
  if sensor_value > 50:
    print("white")
  else:
    print("black")
```
