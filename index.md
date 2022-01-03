# Genuary challenges!


## Genurary 1 - Draw 10,000 of something. 

What could be the worst way to draw a cube?  With 10,000 dodecahedrons of course!  BuildBee MakeCode has automatic loop protection to protect you from going too crazy with shape generation and burning your browser to the ground.  What a great way to test that.

![Genuary 1](./genuary-1.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-9saTYL)


## Genurary 2 - Dithering.

Dithering.  Well this was a bit of a challenge to pull in image data, but I've always been amazed how MakeCode Arcade encodes 8 bit color for devices using a special string that goes 0-f for each bit.  Every row is it's own row of image data.  Pretty clever design.  

So I hopped over to arcade.makecode.com and grabbed their background image, then used the JavaScript (actually TypeScript but sshhh) editor to place in my string from MakeCode Arcade. 

Cause the challenge was dithering - I skipped every second pixel and used greyscale by using hex values like `#FFF` (for white), `#000` (for black) 

![Genuary 2](./genuary-2.png?raw=true)

[Try it in BuildBee MakeCode!](https://makecode.buildbee.com/proj-gNhnPD)
