# Genuary challenges!

Hi I'm JFo, one of the authors of BuildBee MakeCode, a 3d printing coding editor based on the Microsoft MakeCode platform.  Heavily inspired from OpenSCAD and JSCad, BuildBee MakeCode is a Constructive Scene Geometry (CSG) editor that can be coded in blocks, TypeScript (JavaScript) or a subset of python (Static Python).

I thought I'd celebrate Genuary by show some of the more crazier things you can do with [BuildBee MakeCode](https://makecode.buildbee.com).

BuildBee MakeCode is a free, open source code editor provided as a service to the 3d printing community by the team at [BuildBee](https://buildbee.com)

Special thanks to [Genuary](https://genuary.art) for the [#Genuary2022 prompts](http://genuary.art/prompts)

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

```
On a wall surface, any
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


*just random points*

![Genuary 7](./genuary-7.png?raw=true)

*evenly random points*

![Genuary 7](./genuary-7-evenly-distributed.png?raw=true)

The other neat thing about this one is the use of "parameters" instead of variables.  These show up in the little form inside the simulator - and lets the user choose settings - maybe 50 points is not enough - or the wall should be bigger.  Dont do what I just did and set the `wallSize` to `0`, you'll be scratching your head why there's nothing there. 

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-Oyub_P)


## Genuary 8 - Single Curve Only

This one was actually made by James, who I said to last year - hey can you make me a really cool function with hexagons?

I am glad to have the chance to show this one off.

![Genuary 8](./genuary-8.png?raw=true)

This one was so cool I also had the guys make up a [T-shirt / Laptop sticker](https://www.redbubble.com/i/sticker/BuildBee-MakeCode-Hex-Wave-by-BuildBee/65210252.EJUG5) - which his high praise for a mathematical function!

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-ISz_jK)

## Genuary 9 - Architecture

I went with a simplified model of the iconic Sydney Harbour Bridge.  Completed in 1932, "the coathanger" like design connects North Sydney to the rest of the city, and features an amusement park at its base on the northern side.  You can walk across the bridge, and on top of the arch of bridge - both of which are great fun.

![Genuary 9](./genuary-9.png?raw=true)

To model the vertical posts, I used cube shapes, and then intersected them with an arc to cut them at the correct height.  Intersection in CSG means to only leave behind the overlapping parts of the shape. 

*using intersect to cut the posts at the right height*

![Genuary 9](./genuary-9-intersect.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-84IfP-)


## Genuary 12 - Packing

Whenever we finish a big project, the team celebrates with donuts. But there is so much inter internal fragmentation (wasted space) inside a box of donuts.  I vote that all donuts should be packed concentrically.

![Genuary 12](./genuary-12.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-fDyFFT)

## Genuary 13 - 80x800

This was a challenge, because unless you've got a belt printer, the largest you should really make something is probably around 220mm. So I thought I hadn't shown off rotate extrude.  I rotated these 2d shapes 800 degrees and gave them all 80 faces.  It's a bit contrived, but what I've learned is that the editor doesn't like it if you dont rotate at least 360 degrees.  Sounds like something to look at in the future(!)

*rotate extrude rotates flat shapes profiles to form a 3d shape*

![Genuary 13](./genuary-13-blocks.png?raw=true)

![Genuary 13](./genuary-13.png?raw=true)

*what it looks like before rotate extrude*

![Genuary 13](./genuary-13-2d-shape.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-9MCIq1)



## Genuary 14 - Something you'd never make

Matt made a version of the [Utah teapot in BuildBee MakeCode](https://makecode.buildbee.com/proj-officialUtahTeapot) by cleverly using the wrap shapes block to create more organic looking shapes.  This algorithm is based upon the quick hull algorithm - which is normally used in collision detection in video games to quickly see if an object has been "hit". 

I have remixed his project here to create a design inspired by the book [The Design of Everyday Things](https://en.wikipedia.org/wiki/The_Design_of_Everyday_Things) by Donald Norman.  This is one of my favourite reads about the importance of user centered design.  It is where I first learned that if something is hard to work out how to use, then the problem is the design, not the user.  (:: [totally not looking at you at Blender](https://www.giudansky.com/illustration/infographics/blender-map) ::) :rofl:

![Genuary 14](./genuary-14.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-fDyFFT)


## Genuary 15 - Sand

One of my pet features in BuildBee MakeCode is the ability to cut standard size threads.  We have even included the thread for a 2 liter soda bottle, which means you can easily make a double sided connector to build your own sand timer.  

I haven't had the time to print this one yet but [here is just the double soda bottle connector](https://makecode.buildbee.com/proj-aK4Fn4) which should be 3d printable.  I used a similar concept to make a mentos loader for a diet-cola nucleation fountain, which I can't wait to show off at some point too.

The idea with threads is that you take a cylinder (or any other shape) and you subtract a thread cutting tap from it.  

If you want to add standard size threads to something use the thread version of the block instead!  What I really am excited about is the idea of easily making functional 3D printed parts that work with other household objects.

![Genuary 15](./genuary-15.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-lpQqUA)





