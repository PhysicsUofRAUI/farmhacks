---
layout: post
project: grain-monitor
---

It occurred to me that the reason niether of the far old cables were working might be that the pull up resistor being used may not be allowing good communication with the sensor and the Arduino. After reading it turns out that I was correct and I previously even wrote about it here, https://github.com/PhysicsUofRAUI/binTempSensor/blob/master/how_to_docs/assemble_pcb.md. The furthest one is still not quite working.

The furthest one is bouncing between -100 and 85 C. The 85 C is an error code/default value from the DS18B20, and the -100 is my own error value.

As can be shown by this code snippet here:

```
one_middle = binOneSensors.getTempC(one_middle_address);
if (one_middle == DEVICE_DISCONNECTED_C)
{
  Serial.println("Error");
  one_middle = -100;
}
```

After reading some more and just sort of guessing at the situation I am going to try lowering the pull-up resistor again to maybe as low as 220 Ohm.
