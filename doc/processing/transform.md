## Transform

* [applyMatrix()](http://processingjs.org/reference/applyMatrix_/)
* [popMatrix()](http://processingjs.org/reference/popMatrix_/)
* [pushMatrix()](http://processingjs.org/reference/pushMatrix_/)
* [resetMatrix()](http://processingjs.org/reference/resetMatrix_/)
* [rotate()](http://processingjs.org/reference/rotate_/)
* [rotateX()](http://processingjs.org/reference/rotateX_/)
* [rotateY()](http://processingjs.org/reference/rotateY_/)
* [rotateZ()](http://processingjs.org/reference/rotateZ_/)
* [scale()](http://processingjs.org/reference/scale_/)
* [translate()](http://processingjs.org/reference/translate_/)

### Example

```python
from processing import *
import math

rotate = PI/6
def setup():
    size(400, 400, P3D)

def draw():
    global rotate
    background(180)
    noFill()
    translate(150, 150, 0)
    rotate += 0.01
    if rotate >= TWO_PI:
        rotate = 0
    rotateY(rotate)
    stroke(153)
    box(35)
    # Set rotation angles
    ct = math.cos(PI/9.0)
    st = math.sin(PI/9.0)          
    # Matrix for rotation around the Y axis
    applyMatrix( ct,  0.0,  st,  0.0,
                 0.0, 1.0, 0.0,  0.0,
                 -st, 0.0,  ct,  0.0,
                 0.0, 0.0, 0.0,  1.0)
    stroke(255)
    box(50)

run()
```

### Reference

* [Processingjs](http://processingjs.org/reference/)
* [Processingjs applyMatrix](http://processingjs.org/reference/applyMatrix_/)
