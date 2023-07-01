---
layout: post
project: hooter
---

As the title may suggest this is an update describing the development of the simple owl hooting prototype with the Arduino Uno. It is functionaly the same as the Arduino Base version except that instead of buzzing when something is close to the sensor a speaker will hoot.

The main parts of this solution is:
- PCM Library: https://github.com/damellis/PCM
  - also found here http://highlowtech.org/?p=1963
- Down at the bottom of that last [link](http://highlowtech.org/?p=1963) there is an audio encoder that was used to make the audio sound correct.
- I learned about this method looking at this post https://www.instructables.com/Talking-Arduino-Playing-a-MP3-With-Arduino-Without/

You can find the work and documentation of what was done here: https://github.com/PhysicsUofRAUI/hooting_owl. There is a KiCad schematic there that uses the ATMEGA328P in place of the Arduino Uno. Notice that the speaker is driven directly by one of the pins. This can be done since it is only a 200mW speaker (it is on the edge but seems to work) and for the final project a transistor of some sort will have to be used so that a larger speaker can be used.

I have a three pronged attack in mind to continue development.

1. Read up on the code made by highlowtech so that I can edit it to work on a chip at a lower clock speed, and to be programmed on the chip directly. This is mostly to be done so that I can make it lower power. A timer will likely have to be used to prevent the ultrasonic sensor from being powered all the time and to instead check only periodically.

2. Learn more about transistors and power management. I feel my foundational knowledge of the basic circuit components needed to make this project is lacking and henceforth need to improve it. The speaker will have to be powered separately from the chip instead of being driven directly by the chip and that will require a transistor. The power supply will have to be designed and it looks like a switching supplies combined with a linear regulator will probably be best (if using a 9V battery), so I should read up on all the components needed for that.

3. Finally I am going to start leaving the arduino prototype outside to see if it will actually scare any birds and maybe adjust parameters if it is not working properly.

Keep tuned for more updates.
