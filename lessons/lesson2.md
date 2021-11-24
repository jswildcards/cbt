# Lesson 2: Programming an Electronics Board with Python

## Displaying Images

### Example 1

```python
from pystubit.board import display, Image

image = Image('00000:01010:00000:10001:01110:')
display.show(image)
```

### Example 2

```python
from pystubit.board import display, Image

image = Image('00100:00100:01110:11111:01010:')
display.show(image)
```

## Animated Images

### Example 1

```python
from pystubit.board import display, Image

image1 = Image('00000:00100:11001:11110:01001:')
image2 = Image('00000:01000:11001:11110:00110:')

image1.set_base_color((31, 31, 0))
image2.set_base_color((31, 31, 0))

while True:
    display.show(image1)
    display.show(image2)
```

### Example 2

```python
from pystubit.board import display, Image

image1 = Image('11100:01100:00100:00110:00111')
image2 = Image('10000:11000:11111:00011:00001')
image3 = Image('00001:00111:11111:11000:10000')
image4 = Image('00111:00110:00100:01100:11100')

image1.set_base_color((0, 31, 31))
image2.set_base_color((0, 31, 31))
image3.set_base_color((0, 31, 31))
image4.set_base_color((0, 31, 31))

while True:
    display.show(image1, 200)
    display.show(image2, 200)
    display.show(image3, 200)
    display.show(image4, 200)
```

## Displaying Strings

### Example 1

```python
from pystubit.board import display
display.show("A")
```

### Example 2

```python
from pystubit.board import display
display.scroll("AKIRA")
```

## Light Show

### Example 1
```python
from pystubit.board import display
import time

colors = ((31, 0, 0), (31, 31, 0), (0, 31, 0), (0, 31, 31), (0, 0, 31), (31, 0, 31))
display.clear()

while True:
    for color in colors:
        for x in range(0, 5):
            for y in range(0, 5):
                display.set_pixel(x, y, color)
                time.sleep_ms(100)
```

### Example 2
```python
from pystubit.board import display
import time

colors = ((31, 0, 0), (31, 31, 0), (0, 31, 0), (0, 31, 31), (0, 0, 31), (31, 0, 31))
display.clear()

while True:
    for color in colors:
        for y in range(0, 5):
            for x in range(0, 5):
                display.set_pixel(x, y, color)
            time.sleep_ms(100)

```
