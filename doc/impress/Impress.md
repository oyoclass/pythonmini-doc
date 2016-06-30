# Impress

Impress can be used to create slideshows that are more than just a simple left to right, slide by slide implementation like Powerpoint. Take a look at this demo [here](http://impress.github.io/impress.js/#/bored).

## Slideshow Functions

* `impress.Slideshow(width, height)` : Creates a slideshow that will open upon presentation in a window with the specified width and height. It also returns a _Slideshow_ object (the class is explained below).
* `impress.Slide(x, y, z)` : Creates a slide at position (x, y, z) that can be edited and added to a slideshow. If z is not included, it is set to 0 by default. This also returns a _Slide_ object (the class is explained below).
* `impress.Paragraph()` : Creates a paragraph object that can be added to a slide. It returns _Paragraph_ object that can be modified.
* `impress.builtinFonts()` : Returns a list of names of built in  fonts.
* `impress.builtinThemes()` : Returns a list of names of built in themes.

## Slideshow Class

* `slideshow.setTitle(title)` : Sets the title of the Slideshow to the string title. The default title is "Default Title".
* `slideshow.setTheme(theme)` : Sets the theme of the Slideshow to the built in theme passed in the string theme. If the theme is not set, it will be set to the default theme.
* `slideshow.setFont(font)` : Sets the font of all the text in the slideshow to the built in font passed in the string font.
* `slideshow.addSlides(slides)` : Sets the list of slides for the Slideshow to the list of Slides that is passed in the function call
* `slideshow.present()` : Creates the HTML for the slideshow and opens it in a new window.

## Slide Class

* `slide.setPosition(x, y[, z=0])` : Sets the position of the slide to the specified (x, y, z) coordinates. This function can also be called with only x and y.
* `slide.setRotation(x, y, z)` : Sets the rotation of the slide around the x-axis, the y-axis, and the z-axis. If the slideshow will remain 2-D, call this function with `(0, 0, z)`.
* `slide.setScale(number)` : Sets the scale for the current slide. This number must be greater than or equal to 1.
* `slide.addList(list)` : Adds the list to the elements that are added in the current slide.
* `slide.addImage(imageURL[, alignment="center"])`: Adds the image with the specified URL to the current slide with the specified alignment. The default alginment is "center". You can set the alignment to "right", "center", or "left".
* `slide.addHeader(text, level[, alignment="center"])`: Adds a header with the specified text to the current Slide. The level must be a number between 1 and 6, as it represents the HTML tags `<h1>, <h2>, ... <h6>`. By default, the alignment is "center". You can set the alignment to "right", "center", or "left".
* `slide.addParagraph(paragraph[, alignment="center"])`: Adds a paragraph to the specified slide. Default alignment is "center". You can set the alignment to "right", "center", or "left".

## Paragraph Class

* `paragraph.addText(text[, bold=False, italic=False])`: Adds text to the current paragraph that is bold and/or italicized. Default values for bold and italic are both False.
* `paragraph.addLink(text, address[, target="new"])`: Adds a hyperlink to the current paragraph. The text that is shown is the text that appears in place of the web address. If you want the webpage to open in a new window, you must pass the target as "self". If you want the link to open in the same window, do not include the third parameter.
* `paragraph.addBreak()`: Adds a line break to the current paragraph.

## Example
```python
import impress

print impress.builtinFonts()
# ['Slabo', 'Roboto Condensed', 'Titillium Web', 'PT Sans']
print impress.builtinThemes()
# ['blue', 'red', 'green', 'dark']

list1 = [1, 2, 3, 4, 5]

x = impress.Slideshow(1000, 500)
x.setTheme("green")
x.setFont("Slabo")

slide1 = impress.Slide(50, 10, 0)
slide1.setScale(1)
slide1.addList(list1)
slide1.addImage("http://cdn.bulbagarden.net/upload/thumb/0/0d/025Pikachu.png/250px-025Pikachu.png", "center")
slide1.addHeader("Hello, World", 1, "center")

slide2 = impress.Slide(300, 1000, 0)
slide2.setRotation(0, 0, 90)
slide2.setScale(3)
slide2.addHeader("Second Slide", 2, "center")
slide2.addImage("http://cdn.bulbagarden.net/upload/thumb/8/85/385Jirachi.png/250px-385Jirachi.png", "center")

slide3 = impress.Slide(1000, 200, 90)
slide3.setRotation(0, 90, 180)
slide3.setScale(2)
p = impress.Paragraph()
p.addText("This is a test p", True, False)
p.addBreak()
p.addLink("OYOclass", "https://oyoclass.com/")
p.addText("   Another text", False, True)
slide3.addParagraph(p, "center")

x.addSlides([slide1, slide2, slide3])
x.present()
```
