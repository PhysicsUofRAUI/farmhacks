---
layout: post
project: hooter
---

A spin off project was created from this project in honour of halloween. It was made to create some spooky sounds that were triggered by the HC-SR04 proximity sensor. While creating this off shoot project I learned a lot of different things that will help this project along once I come back to it and this update will go into depth about it.

The first problem I had is that I had forgotten how to properly downsample the audio clips. Now I have made what I hope is clear instructions on the Hackaday Project page here: https://hackaday.io/project/193172-scary-sound-effect.

I then decided to solder one of the PCBs I ordered together to see how it would work and found a few significant problems which are described below:
- The ISCP header had no labels so the PCB layout is needed to know what goes to what.
- I tried programming it with the Arduino IDE and that would need the Rx and Tx pins broken out.
- Indicator lights could be added to aid in trouble shooting.
- The HC-SR04 pinout is such that I had to flip it around to the opposite side. It would be preferable if that was changed.

I then had some issues which I initially thought were power issues, but I think it may have been issues with the proximity sensor getting triggered to easily. I ended up decreasing the required distance and powering the Arduino separately from the speaker itself.

I was also having trouble with speakers burning out quickly, so after some googling I added a bypass capacitor to the circuit. This appeared to work, but it was also at the same time I was having the power issues and sensing issues (it would just play all the time).

Eventually I got it all working ok, but it would continually restart the playback when someone just stood in front of it. To combat this a check was added to see if the playback was started in the last 30s.

Some more work will be done on this project, but it is getting moved aside and the focus going forward will be the temperature puck.
