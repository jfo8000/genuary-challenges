# Genuary challenges!

Hi I'm JFo, one of the authors of BuildBee MakeCode, a 3d printing coding editor based on the Microsoft MakeCode platform.  Heavily inspired from OpenSCAD and JSCad, BuildBee MakeCode is a Constructive Scene Geometry (CSG) editor that can be coded in blocks, TypeScript (JavaScript) or a subset of python (Static Python).

I thought I'd celebrate Genuary by show some of the more crazier things you can do with [BuildBee MakeCode](https://makecode.buildbee.com).

BuildBee MakeCode is a free, open source code editor provided as a service to the 3d printing community by the team at [BuildBee](https://buildbee.com)

## Genurary 1 - Draw 10,000 of something. 

What could be the worst way to draw a cube?  With 10,000 dodecahedrons of course!  BuildBee MakeCode has automatic loop protection to protect you from going too crazy with shape generation and burning your browser to the ground.  What a great way to test that.

![Genuary 1](./genuary-1.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-9saTYL)


## Genurary 2 - Dithering.

Dithering.  Well this was a bit of a challenge to pull in image data, but I've always been amazed how MakeCode Arcade encodes 8 bit color for devices using a special string that goes 0-f for each bit.  Every row is it's own row of image data.  Pretty clever design.  

So I hopped over to arcade.makecode.com and grabbed their background image, then used the JavaScript (actually TypeScript but sshhh) editor to place in my string from MakeCode Arcade. 

Cause the challenge was dithering - I skipped every second pixel and used greyscale by using hex values like `#FFF` (for white), `#000` (for black) 

![Genuary 2](./genuary-2-arcade.png?raw=true)
![Genuary 2](./genuary-2.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-gNhnPD)

## Genuary 3 - Space

Sometimes simple is better.  I took this one literally and made a simple rocket with three shapes.  The difference between BuildBee MakeCode and some of the other code-cad like programs is that handy layout utilities have been added - like `stack shapes`.  This saves you time when you just want things to sit on top of one another.  You can also change the axis so that you can stack in X, Y or Z (up).

![Genuary 3](./genuary-3-blocks.png?raw=true)
![Genuary 3](./genuary-3.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-4LcxjC)


## Genuary 4 - Flow fields

This one tested me a bit. I don't know much about flow fields so I decided to port this implementation to show off the Extra Math category of BuildBee MakeCode.  Extra Math has utilities for converting radians to degress, and lets you block code with sin/cos/and PI easily.

With the power of the MakeCode engine, it's straight forward to port over JavaScript examples.  I wrote some of this in the blocks editor, but dropped down to the JavaScript (TypeScript) editor to make a few handy edits.

[Thanks to Keith Peters for this flow fields tutorial](https://github.com/bit101/tutorials/blob/master/flow_fields/flow_fields_03.js)

Don't try to print this one unless you add in a base plate - otherwise you'll be just decorating your build plate with filament!

![Genuary 4](./genuary-4.png?raw=true)
![Genuary 4](./genuary-4-blocks.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-Ow3FEb)


## Genuary 5 - Destroy a square

Ok this one is not fair because there are SO many things you can do with squares and cubes in BuildBee MakeCode

Here's a little known twist option to the linear extrude! 

What is it all doing?  For 2D shapes you can extrude (give a third dimension, like thickness).  Typically there are two kinds of extrusions - linear (just give thickness to the thing) and rotation.  There is a little known "twist" option to the linear extrude - this will take a step and then twist - and connect your square to the previous square, then take a step and twist again.... until it gets to the total amount of degrees you specify. If you want more detail in your twists - specify more steps.


Note, you can only use linear and rotate extrusions with 2d shapes. 

![Genuary 5](./genuary-5-rotate-extrude.png?raw=true)
![Genuary 5](./genuary-5-extrude-blocks.png?raw=true)


[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-Ul2uQl)


How about destroying it by surrounding it with 12 sided polygons?

![Genuary 5](./genuary-5-destroy2.png?raw=true)

![Genuary 5](./genuary-5-destroy2-blocks.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-3v6Prt)


## Genuary 6 - Trade Styles - Chamfer and Fillet

One of the features usually left to more powerful CAD programs is the ability to round off the edges.  This is incredibly important for designing stress relief as well as removing any sharp corners that may cause injury when handling a 3d printed part.   Also adding a slight chamfer to the bottom of your part can make it easier to remove from the print bed after printing. 

So to trade styles with a friend, [I give you this example to play with](https://makecode.buildbee.com/proj-LIx9DN)!  To chamfer something cuts it off at a straight angle, but to fillet it - you give it a rounded edge. In BuildBee MakeCode, you can style the tops and bottoms of your part.  If you need to apply the style in another axis, simply rotate the part and add another style edges block.

![Genuary 6](./genuary-6-blocks.png?raw=true)

*example of chamfer*

![Genuary 6](./genuary-6-fillet.png?raw=true)

*example of fillet*

![Genuary 6](./genuary-6.png?raw=true)


[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-LIx9DN)


## Genuary 7 - Sol Lewitt Wall Painting
The rules for this one are very simple:

```On a wall surface, any
continuous stretch of wall,
using a hard pencil, place
fifty points at random.
The points should be evenly
distributed over the area
of the wall. All of the
points should be connected
by straight lines
```

Originally I messed this up by not evenly distributing my points.   The technique I went for in the end was to use the equation of a circle to distribute the points evenly across the screen.  But when I did that, I got a shape with no criss-crosses.  So I multiplied the end point by 1, 0, or -1 to get the points to flip at random.  Is it art?  Mine is definitely not.  But I was glad to have had the Extra Math category to help out with this one.  

Although perhaps we need exponents!


![Genuary 7](./genuary-7.png?raw=true)


[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-CUeGJB)


