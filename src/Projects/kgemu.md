This is my updated attempt at making an assembly compiler and emulator, but this time with new knowledge, much more ambition, and in rust.

Very work in progress.

The plan is to have a compiler and emulator that are independent of processor and language, and use json files to define how the processor and language work.  Right now It can parse code into commands, labels, comments, etc... and can parse commands into opcodes, and operands.  Next is converting the parsed commands into binary.

I am also reading lots of documents on micro controllers, hardware interaction, drivers, etc.. to learn more about low level systems to make a more accurate simulator.

[Github source code](https://github.com/Kaden-Ven-Gryphon/kgemu)