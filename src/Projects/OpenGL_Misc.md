# Misc. OpenGL School Projects

![image](../Resources/fish.gif)

I took a computer graphic class in my undergrad degree and it coved a lot of the math around computer graphic, matrix operations for translating, and rotating objects, light sim math for rendering etc.

It used OpenGL for its projects, I had a ton of fun making these, and went well beyond the homework requirements to add more features for the fun of it.  I don't have videos of most of them (I will have to dig up the source code and fight with setting up dependencies for who knows how long in order to get them running again.) but I do have a short clip of my final project.

This one was meant to teach about line culling, we pretend that the box is the borders of the screen and thus any world objects that have points outside of that bounds have to be adjusted to avoid buffer overflow errs.

The requirements was just to make the wire frame fish swim around, be able to feed them to increase their life, and move a box around that would act as the bounds that objects needed to be culled by.

I decieded to go all in and make an entire fish tank.  I added the plants that use sin waves to set their coordinates to animate waving, and made a boid swarm that danced in the back.

To get the whole thing to come together I made a gaussian blur filter to add depth.  We were only allowed to turn in one file and where not allowed or instructed to mess with shaders so I had to pull the frame buffer into memory and implement the blur in C, then render that output on a polygon that filled the screen.  Very inefficient, made the computer very unhappy to run it for long, but it was the only way I could figure out how apply the blur with out making a separate shader file.