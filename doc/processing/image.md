## Image

* [PImage](http://processingjs.org/reference/PImage/)
* [createImage()](http://processingjs.org/reference/createImage_/)

### Loading & Displaying

* [image()](http://processingjs.org/reference/image_/)
* [imageMode()](http://processingjs.org/reference/imageMode_/)
* [loadImage()](http://processingjs.org/reference/loadImage_/)
* [requestImage()](http://processingjs.org/reference/requestImage_/)

### Pixels

* [blend()](http://processingjs.org/reference/blend_/)
* [copy()](http://processingjs.org/reference/copy_/)
* [filter()](http://processingjs.org/reference/filter_/)
* [getPixel()](http://processingjs.org/reference/get_/)
* [setPixel()](http://processingjs.org/reference/set_/)

### Example

```python
from processing import *

pikachu = None
ball = None

def setup():
    global pikachu, ball
    size(400, 400)
    colorMode(RGB, 100)
    # you may want to change the image url below
    pikachu = loadImage("http://www.avatars101.com/avatars/Pokemon/301BE8845F43838DE7A6B6DFEB2B963E/Pikachu.gif")
    ball = requestImage("http://vignette4.wikia.nocookie.net/pokemon/images/4/46/Timer_Ball.png")

def draw():
    background(0, 200, 200)
    image(pikachu, 100, 100)

    if ball.width != 0 and ball.width != -1:
        image(ball, 200, 50, 65, 65)    

run()
```

### Reference

* [Processingjs](http://processingjs.org/reference/)
