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
* ```turtle.right(angle)``` or ```turtle.rt(angle)``` : Turn turtle right by *angle* units.
* ```turtle.left(angle)``` or ```turtle.lt(angle)``` : Turn turtle left by *angle* units.
* ```turtle.goto(x, y)``` : Move turtle to an absolute position. If the pen is down, draw line.
* ```turtle.setposition(x, y)``` or ```turtle.setpos(x, y)``` : Move turtle to an absolute position without drawing the line. *Notice:* this one is different with Python's official turtle module documentation, in which *setposition* is the same as *goto*.
* ```turtle.setworldcoordinates()``` : ?
* ```turtle.setx(x)``` :
* ```turtle.sety(y)``` :
* ```turtle.setheading(dir)``` or ```turtle.seth(dir)``` :
* ```turtle.home()``` :
* ```turtle.circle()``` :
* ```turtle.dot()``` :
* ```turtle.stamp()``` :
* ```turtle.speed(number=None)``` : Set the turtle’s speed to an integer value in the range 0..10. If no argument is given, return current speed. If speed number is set to 0 or less than 0 or greater than 10, speed will be set to 0, which is fastest and no animation takes place. 1 is slowest, 3 is slow, 6 is normal, 10 is fast. By default, its speed is 6.


### Appearance

* ```turtle.shape(name)``` : Set turtle shape to shape with given name or, if name is not given, return name of current shape. Shape's name could be one of followings: "arrow", "turtle", "circle", "square", "triangle", "classic".

### Tell Turtle's State
* ```turtle.position()``` or ```turtle.pos()``` : Return the turtle’s current location (x, y)
* ```turtle.towards(x, y)``` : Return the angle between the line from turtle position to position specified by (x, y), the vector or the other turtle.
* ```turtle.xcor()``` : Return the turtle’s x coordinate.
* ```turtle.ycor()``` : Return the turtle’s y coordinate.
* ```turtle.heading()``` : Return the turtle’s current heading.
* ```turtle.distance(x, y)``` : Return the distance from the turtle to (x, y)

### Pen control
* ```turtle.pendown()``` or ```turtle.pd()``` or ```turtle.down()``` : Pull the pen down – drawing when moving.
* ```turtle.penup()``` or ```turtle.pu()``` or ```turtle.up()``` : Pull the pen up – no drawing when moving.
* ```turtle.pensize(number)``` or ```turtle.width(number)``` : Set the line thickness to width or return it.
* ```turtle.isdown()``` : Return True if pen is down, False if it’s up.

### Color control
* ```turtle.pencolor()``` :
* ```turtle.fillcolor()``` :
* ```turtle.color()``` :

### Filling
* ```turtle.fill()``` :
* ```turtle.begin_fill()``` :
* ```turtle.end_fill()``` :

### Visibility
* ```turtle.showturtle()``` or ```turtle.st()``` : Make the turtle visible.
* ```turtle.hideturtle()``` or ```turtle.ht()``` : Make the turtle invisible.
* ```turtle.isvisible()``` : Return True if the Turtle is shown, False if it’s hidden.

### Animation control
* ```turtle.delay()``` :
* ```turtle.tracer()``` :

### Reset
* ```turtle.reset()``` : Delete the turtle’s drawings from the screen, re-center the turtle and set variables to the default values.
* ```turtle.clear()``` : Delete the turtle’s drawings from the screen. Do not move turtle. State and position of the turtle as well as drawings of other turtles are not affected.

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
