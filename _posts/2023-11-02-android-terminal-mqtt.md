---
layout: post
project: temp-puck
---
As a first step to creating the temperature puck I decided to make a simple app with MIT App Inventor and send it messages with an Arduino MKR 1010.

Currently I am at a location that does not have a micro-usb that is capable of programming an Arduino Wifi 1010, so I am going to just use the terminal first.

It ended up being much easier than I originally thought. Below is the terminal commands I sent:

```
sudo apt update
sudo apt-get install mosquitto mosquitto-clients
mosquitto_pub -t test.mosquitto.org -t "Tempdata"
mosquitto_sub -h test.mosquitto.org -t "#" -u wildcard -v
mosquitto_sub -h test.mosquitto.org -t
mosquitto_sub -h test.mosquitto.org -t 'test'
mosquitto_pub -h test.mosquitto.org -t 'Tempdata' -m 'Tenemp is 1'
mosquitto_pub -h test.mosquitto.org -t 'Tempdata' -m 'Temp is 1'
mosquitto_pub -h test.mosquitto.org -t 'Tempdata' -m 'Temp is 78'
```

For the app I used the following extension https://ullisroboterseite.de/android-AI2-MQTT-en.html, and watch this video to get all the internals set up correctly https://youtu.be/WAimZhU5phs?si=5bQxqndYbPV2jozP.

After I did that connected the Arduino MKR 1010 to the mosquitto server so that I can view actual temperature data. The code can be found at this GitHub https://github.com/PhysicsUofRAUI.

The next steps are:

1. Create a more constrained definition of the project.
2. Connect the Arduino MKR 1010 to a non-test cloud provider.
