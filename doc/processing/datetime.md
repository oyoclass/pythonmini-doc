## Date & Time

* [day()](http://processingjs.org/reference/day_/)
* [hour()](http://processingjs.org/reference/hour_/)
* [millis()](http://processingjs.org/reference/millis_/)
* [minute()](http://processingjs.org/reference/minute_/)
* [month()](http://processingjs.org/reference/month_/)
* [second()](http://processingjs.org/reference/second_/)
* [year()](http://processingjs.org/reference/year_/)


### Example

```python
from processing import *

def setup():
    size(500, 400)

def draw():
    background(0)
    s = "Current time: %02d:%02d:%02d" % (hour(), minute(), second())
    textSize(35)
    fill(0, 255, 0)
    text(s, 80, 200)


run()
```

### Reference

* [Processingjs](http://processingjs.org/reference/)
