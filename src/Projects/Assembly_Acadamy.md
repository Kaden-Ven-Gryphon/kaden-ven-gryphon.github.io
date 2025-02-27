# Assembly Academy

![image](../Resources/aa.gif)

This was my honors capstone project that I eventually turned into a publish paper.  It is a assembly programing tutorial made in the Unity game engine using C#.  The assembly language used is based of the arm thumb mode, though many instructions (push, pop, etc.) where not implemented.


The user is given simple tutorials that introduce an assembly instruction and then are given a puzzle to solve using that instruction and previously learned instructions.  The puzzle have the user program a virtual robot that can move left and right, pick up and put down blocks, and read the value of the block.

### Example:

- Tutorial on the branch instruction "b"
- Puzzle: "Use a loop to run the robot off the right side of the shelf."
- Solution: 

```
.text
loop:
	mov r1, #1
	botmove
	b loop
```

### Implementation

I made a compiler that can take the arm thumb assembly and compile it to a binary, using the ARM7TDMI Data Sheet.  The compiler can create error message that give line numbers and suggests possibly solutions like, "Invalid Register", "Expected ,", etc.

The emulator loads the binary into memory and then preforms the fetch execute cycles.  It displays the current state of the registers, the CCR flags, and attempts to decode the current instruction binary back into an instruction.

The code for this was pretty rough, both in terms of structure and not knowing about key C# string functions that would have made it cleaner.  The design of the emulator is pretty limited too, and is not a great representation of how the processor works.  I have since gotten a better understanding of microcontrollers and how hardware works and revisiting the idea of a compiler and emulator but this time made in rust you can see how that is going here [kgemu (wip)](./kgemu.md) 

![image](../Resources/UIfig(1).PNG)
