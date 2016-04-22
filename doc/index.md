## What's Python?

Quote from [Python official website](python.org):

> Python is an easy to learn, powerful programming language. It has efficient high-level data structures and a simple but effective approach to object-oriented programming. Python’s elegant syntax and dynamic typing, together with its interpreted nature, make it an ideal language for scripting and rapid application development in many areas on most platforms.

## Why Python?

* Easy to learn, a lot of top universities use Python to teach "Programming 101".
* Not a toy, quite powerful and versatile, from basic tools to web development, to data analytics, etc, Python can handle all of them.
* Write once, run everywhere. Once you finished the code, it can be run in Windows, Mac OS, Linux/Unix.

## About PythonMini

PythonMini is an online python interpreter to help you write python in browser, without installing it to your computer. It implements a subset of Python 2, plus one additional graphical libraries - *Processing*.

## Quick Start

Copy following example code to PythonMini editor then click "Run":

* Say hello

```python
print "hello"
```

* Doing math

```python
print 123 * 456     # calculate 123 times 456
print 180 / 12      # calculate 180 divided by 12
```

* Ask a question

```python
answer = raw_input("What's your name?")
print "hello", answer
```

* Draw a circle

```python
from turtle import Turtle
t = Turtle()
t.circle(40)    # a circle with radius 40
```

* Draw a 3D rotating box

```python
from processing import *

rotating = 0.01

def setup():
    size(400, 400, P3D)

def draw():
    global rotating
    background(0, 0, 0)
    translate(200, 100, 0)
    rotateY(rotating)
    rotating += 0.01
    if rotating >= PI:
        rotating = 0.01
    fill(255, 0, 0)
    box(40)

run()
```

There are a lot more you can do with PythonMini, for more information and examples, check the documentation on the left.

## Feedback

If you find any error about this documentation, please help us improve it, mail us at <a href="mailto:feedback@oyoclass.com">feedback@oyoclass.com</a>

## Credits

* [Skulpt](skulpt.org)
* [Python Official Documentation](https://docs.python.org/2/)
* [Processingjs](http://py.processing.org/reference/)
