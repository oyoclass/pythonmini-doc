## Typography

* [PFont](http://processingjs.org/reference/PFont/)

### Loading & Displaying

* [createFont()](http://processingjs.org/reference/createFont_/)
* [text()](http://processingjs.org/reference/text_/)
* [textFont()](http://processingjs.org/reference/textFont_/)

### Attributes

* [textAlign()](http://processingjs.org/reference/textAlign_/)
* [textLeading()](http://processingjs.org/reference/textLeading_/)
* [textMode()](http://processingjs.org/reference/textMode_/)
* [textSize()](http://processingjs.org/reference/textSize_/)
* [textWidth()](http://processingjs.org/reference/textWidth_/)

### Metrics

* [textAscent()](http://processingjs.org/reference/textAscent_/)
* [textDescent()](http://processingjs.org/reference/textDescent_/)


### Example

```python
from processing import *

myFont = None

def setup():
    global myFont
    size(400, 400)
    background(0)
    myFont = createFont("Georgia", 32);

def draw():
    fill(255, 255, 255)
    textFont(myFont)
    textAlign(LEFT)
    text("Hello World", 100, 200)

    fill(255, 0, 0)
    textSize(30)
    text("Start Game", 100, 300)


run()
```


### Reference

* [Processingjs](http://processingjs.org/reference/)
