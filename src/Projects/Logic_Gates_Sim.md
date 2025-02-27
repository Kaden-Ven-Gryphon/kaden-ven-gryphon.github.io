# Logic Gate Simulator (C)

![image](../Resources/logicgates.gif)

This was a project that I worked on off and on through out my masters degree.  I wanted to simulate a computer running at the gate level, and I wanted to do it in C.  That turned out a be a mess as I could not get an simple C image libraries to work so I ended up making my own.  I wanted to be able to save images to png format, but after a week of writing a zlib compressor and Huffman tree and was trying to decode a png by hand to try and error check.  I eventual had to give up on that and use a call to a python script to convert the raw binary image into a png.

This gif is a simple register being fed into an adder.  The register is missing a few gates to be proper registers as their outputs are not being fed back into the inputs.

I learned a lot as  did not realize that I needed three states for the wire when I stated and had to make a work around, and I had to figure out solutions to issues with the cycle in the graph created by the registers.

This is only two small components, a single 8-bit register, and an adder, and I would still like to make a full computer at some point.  I may try to revisit this project, but I think I might switch the rust.

(I will try to clean up the code and post in on GitHub eventual)