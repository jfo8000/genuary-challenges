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

Here's a little known twist option to the linear extrude - you can only use linear and rotate extrusions with 2d shapes. 


![Genuary 5](./genuary-5-rotate-extrude.png?raw=true)
![Genuary 5](./genuary-5-extrude-blocks.png?raw=true)

[Try it in BuildBee MakeCode!]https://makecode.buildbee.com/proj-Ul2uQl)




