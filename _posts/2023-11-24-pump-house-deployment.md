---
layout: post
project: temp-puck
---
Yesterday the pump house froze up once again, and because we did not catch it early enough it froze up and broke the pump. This prompted me to deploy what I have working for the temperature puck so that hopefully we can catch it earlier next time. The deployment is as follows.

The code can be found here: https://github.com/PhysicsUofRAUI/temperature-puck/tree/main/WiFiSimpleSender_mkr1010_temp_test.

The Arduino MKR 1010 is wired to a thermistor, so the actual temperature being read may be a bit inaccurate but it will work for this deployment.

The Arduino was then placed into a box and left in the pump house. The first time it was not able to connect to the WiFi network so it was then brought outside of the pump house to do the first connection and then placed back into the pump house. It has been working for the past few hours, so hopefully it will keep trucking.

On that same github you can read the project constraints I had mentioned earlier.

The next steps are as follows.

- Connect multiple publishing clients and figure out the best way to differentiate them (topics?)
- Figure out a way to only allow certain people to access the certain data.
- Create my own Android app to monitor the temperature.
