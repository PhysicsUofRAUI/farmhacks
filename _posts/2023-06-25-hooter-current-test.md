---
layout: post
project: hooter
---

After thinking about the ultrasonic sensor being used I was concerned that it may take too much energy/current for the application so I used my multimeter to test the current draw from the trigger pin, echo pin, and Vcc. The results are below.

- trigger pin: 0 mA
- echo pin: 0 mA
- Vcc: 3 to 4 mA

Given that 3 to 4 mA are being drawn by the sensor lets look at some common battery combinations.

- 9V Lithium: [1200mAh](https://www.microbattery.com/blog/post/battery-bios:-everything-you-need-to-know-about-the-9v-battery/)
- alakaline AA : [2500mAh](https://www.microbattery.com/blog/post/battery-bios:-everything-you-need-to-know-about-the-aa-battery/)
- CR2032 : [220mAh](https://www.microbattery.com/lithium-coin-cell-batteries-cr/cr2032/atomic-cr2032-battery-3v-lithium-1-premium-battery.html#tab-product5)

Doing a very rough calculation (not entirely sure if it is even valid) stepping down the 9V battery to 5V would result in 2160mAh. Assuming that we will lose some energy in the conversion and operating other aspects of the design lets use 2000mAh and the Vcc current to figure out how long it will last.

t = time in hours
  = 2000mAh / 4 mA
  = 500 hours
  =~ 20 days

That is far below what our goal battery life is. I have some ideas to possibly extend the battery life.

1. Instead of checking continuosly check once every second or so. Since the entire cycle of checking takes roughly 38ms so if we assume it is on for about 50ms that means our device would be off about 95% of the time. I think checking that often would still give enough responsiveness. If it worked out perfectly (probably won't) that may up the battery life to 1 year which is the goal.

2. Use a different sensor or style of sensor. This sensor says that it [could use up to 15mA](https://howtomechatronics.com/tutorials/arduino/ultrasonic-sensor-hc-sr04/) so perhaps there is a lower current sensor of the same style (ultrasonic) or the project could be changed to use a motion sensor of some sort instead (might hoot more often).

3. Maybe just have it hoot every so often instead of relying on external input.

I like the ideas in the order listed and will try them in that order.

Note: Multiple AA's and CR2032 batteries would be needed to get to the required 5V. I wasn't really thinking at the start and that is why I checked the trigger and echo even though I now think that was not really necessary. I was also having trouble with buzzer and it turned out one of my jumper wires were broken.
