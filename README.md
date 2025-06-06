# LogicDesign

Purpose:

This controlled board goal is to map the switches to the LEDs according to a certain sequence that is determined by the user by the last switch being turned off. Initially, all the switches are mapped to the LEDs that are facing them, however, when turning all the switches then turning them off, a new sequence of LEDs turning on will be implemented. To achieve this working procedure, the design must be based on combinational and sequential circuits, memory elements, and a 555 timer which is a clock. To visualize the active sequence, we used a 7-segment display to display the sequence number.


Attached Files Description:

*Quartus Files: It contains all the blocks and designs and simulation for the project. It is what we implemented on Quartus.
*Documentation: It contains the report done for the project.
*Schematics: It includes the designs and the 555 timer design as long as other blocks for the project.
*Simulations: It contains test simulation cases for the Quartus compilation.
*Circuitous: It contains the circuitous file where you can see the shifting happening

Setup and usage instructions:
-First you must have Altera Quartus II running on your computer.
-Next you must open Quartus Files folder and then open TR1.qpf
-Then you will see the project design where you can either make a new simulation or just see the previous one
-To see the circuitous part, you must have downloaded Simulador Digital de protoboard and then open the file directly form Folder Circuitous.

Additional insights into the project’s design choices:
We will follow divide and conquer strategy to make this project. So, we are going to divide the tasks where each one is responsible for a part of the project. We first must start with four input switches and S1-S4 and four output LEDs red, blue, yellow, and green. Since we are dealing with multiples output combinations for only four switches, we will decode the inputs using a decoder. We must map each switch to the corresponding LED and that can only happen using memory registers which are the famous D-Flip-Flops. Then, we must-after finishing default sequence- proceed to the next state if all switches are turned off for a specific time denoted by 4sec from the 555 timer. This timer is implemented using capacitors and resisters to adjust the time to 4sec. The timer will be used to mark that we will enter the second sequence after portion of time when all switches are turned off. We will also use D Flip-Flops to save the last turned off switch to know which sequence we will be in next. If for example we turn SW3 off last, we will advance to a sequence where switches in any order will light LEDs 3, 4, 1 and 2 respectively. If we turn switch 4 lastly, the sequence will become 4-3-2-1. The sequence for switch 2 is 2-3-4-1 and if switch 1 is turned off last, we will stay in the same sequence as the default one. Moreover, we have a locked mode that when we enter it, switch one will light LED one, and switches two, three and four will light LEDs two, three and four, respectively. Locked mode is entered if we turn on switch two at first in the default state.


Demonstration Video :https://youtu.be/SofATgz4nbQ

