## Math

* [PVector](http://processingjs.org/reference/PVector/)

### Calculation

* [constrain()](http://processingjs.org/reference/constrain_/)
* [dist()](http://processingjs.org/reference/dist_/)
* [lerp()](http://processingjs.org/reference/lerp_/)
* [mag()](http://processingjs.org/reference/mag_/)
* [map()](http://processingjs.org/reference/map_/)
* [norm()](http://processingjs.org/reference/norm_/)
* [sq()](http://processingjs.org/reference/sq_/)

### Trigonometry

* [degrees()](http://processingjs.org/reference/degrees_/)
* [radians()](http://processingjs.org/reference/radians_/)

### Random

* [noise()](http://processingjs.org/reference/noise_/)
* [noiseDetail()](http://processingjs.org/reference/noiseDetail_/)
* [noiseSeed()](http://processingjs.org/reference/noiseSeed_/)
* [random()](http://processingjs.org/reference/random_/)
* [randomSeed()](http://processingjs.org/reference/randomSeed_/)

### Example

```python
from processing import *

xoff = 0.0
width = 400
height = 300

def setup():
    size(400, 400)

def draw():
    global xoff
    background(204)
    xoff = xoff + .01
    n = noise(xoff) * width
    line(n, 0, n, height)

run()
```

### Reference

* [Processingjs](http://processingjs.org/reference/)
* [Processingjs noise function](http://processingjs.org/reference/noise_/)
