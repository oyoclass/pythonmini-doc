## turtle — Turtle graphics

Turtle graphic implements a subset functions of the [Python Turtle Library](https://docs.python.org/2/library/turtle.html).

### Setup

```python
from turtle import Turtle

# Generate Turtle object, name it like your pet
nick = Turtle()
```

Now you have your own turtle (in this example I called it *nick*, but you can change it), there are several functions you can use to control your turtle.

### Move and draw

* ```turtle.forward(distance)``` or ```turtle.fd(distance)``` : Move the turtle forward by *distance*, in the direction the turtle is headed.
* ```turtle.backward(distance)``` or ```turtle.back(distance)``` or ```turtle.bk(distance)``` : Move the turtle backward by *distance*, opposite to the direction the turtle is headed. This function doesn't change turtle's heading.
* ```turtle.right(angle)``` or ```turtle.rt(angle)``` :
* ```turtle.left(angle)``` or ```turtle.lt(angle)``` :
* ```turtle.goto(x, y)``` :
* ```turtle.setposition(x, y)``` or ```turtle.setpos(x, y)``` :
* ```turtle.setworldcoordinates()``` : ?
* ```turtle.setx(x)``` :
* ```turtle.sety(y)``` :
* ```turtle.setheading(dir)``` or ```turtle.seth(dir)``` :
* ```turtle.home()``` :
* ```turtle.circle()``` :
* ```turtle.dot()``` :
* ```turtle.stamp()``` :
* ```turtle.speed()``` :

### Appearance
* ```turtle.shape()``` :

### Tell Turtle's State
* ```turtle.position()``` or ```turtle.pos()``` : Return the turtle’s current location (x, y)
* ```turtle.towards(x, y)``` : Return the angle between the line from turtle position to position specified by (x, y), the vector or the other turtle.
* ```turtle.xcor()``` :
* ```turtle.ycor()``` :
* ```turtle.heading()``` :
* ```turtle.distance()``` :

### Pen control
* ```turtle.pendown()``` or ```turtle.pd()``` or ```turtle.down()``` :
* ```turtle.penup()``` or ```turtle.pu()``` or ```turtle.up()``` :
* ```turtle.pensize(number)``` or ```turtle.width(number)``` :
* ```turtle.isdown()``` :

### Color control
* ```turtle.color()``` :
* ```turtle.pencolor()``` :
* ```turtle.fillcolor()``` :

### Filling
* ```turtle.fill()``` :
* ```turtle.begin_fill()``` :
* ```turtle.end_fill()``` :

### Visibility
* ```turtle.showturtle()``` or ```turtle.st()``` :
* ```turtle.hideturtle()``` or ```turtle.ht()``` :
* ```turtle.isvisible()``` :

### Animation control
* ```turtle.delay()``` :
* ```turtle.tracer()``` :
* ```turtle.update()``` :

### Reset
* ```turtle.reset()``` :
* ```turtle.clear()``` :

### Examples

* Draw line and circle

```python
from turtle import Turtle
nick = Turtle()

# move forward 100 steps
nick.forward(100)
```

* Draw square


* Pixel Art


### Reference

* [turtle library](https://docs.python.org/2/library/turtle.html)
