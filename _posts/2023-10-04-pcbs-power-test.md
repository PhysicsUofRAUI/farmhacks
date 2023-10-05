---
layout: post
project: hooter
---

I ordered pcbs of the current design and they are in already. There are two different linear regulator circuits that can be used (one using the LM317 and the other using MCP1700), and an ATMEGA328 on the board for the control.

I have tested the MPC1700 power supply with 3 AA batteries (the version being used is the 5V power supply MCP1700-5002E/TO), and hooked it up so that it would have approximately 10mA draw. The time and voltage results are below.

| Time (minutes) | Voltage |
| -------------- | ------- |
| 0              | 4.763 V |
| 50             | 4.710 V |
| 140            | 4.635 V |
| 188            | 4.607 V |
| 368            | 4.528 V |
| 506            | 4.479 V |
| 600            | 4.455 V |
| 1320           | 4.322 V |
| 1394           | 4.313 V |
| 1844           | 4.268 V |

I am not overly sure why I took this data but there it is. It did bring up a question for me as to whether using this linear regulator below its rated voltage would effect performance but it appears not.

The next step to this project is to assemble one on a PCB and see how it works. I am also planning to use an ATMEGA168 since I have a few of those lying around and try to program it with MPLABx instead of just using the Arduino.

To program the ATMEGA168 I will first try and understand the code in the library PCM.h and then apply that to my own program.
