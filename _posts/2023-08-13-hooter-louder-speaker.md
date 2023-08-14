---
layout: post
project: hooter
---

So I ordered a selection of larger speakers to try and make my project louder, but it did not initially work out. I did not yet have the transistor recommended by the talking arduino tutorial ([TIP122](https://www.digikey.ca/en/products/detail/onsemi/TIP122G/920327)) and instead I used the more generic 2n3904.

If you check out the following YouTube video https://www.youtube.com/shorts/UxonB4UgZeo you'll see that the 2n3904 got only to about 150mA through the speaker and for some reason never fell to 0 (maybe it was wired wrong).

When I switched to the TIP122 I initially burnt out a speaker because I had it wired wrong, but I decided to put a small current limiting resistor of 10 ohms. That is the middle part of the video.

I eventually removed the current limiting resistor and it became even louder!

The next step is to review the schematic and then create a PCB to be ordered to start field testing.

During field testing hopefully battery life can be extended by utilizing the code well.

The CAD files can be found here: https://github.com/PhysicsUofRAUI/hooting_owl.
