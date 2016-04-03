# Documentation for processing lib


## mouse

#### Property

* mouse.x
* mouse.y
* mouse.px (?)
* mouse.py (?)
* mouse.button

#### Functions

* mousePressed
* mouseMoved
* mouseReleased

Example:

```python
from processing import *

def mousePressed():
    print "pressed at:", mouse.x, mouse.y
    # left button is 37, right button is 39
    print "mouse button:", mouse.button

def mouseMoved():
    print "mouse moved"

def mouseReleased():
    print "released ..."

run()
```
