# LED Light Sensor Circuit

I'm going to be building an LED light sensor circuit because I found it online. I plan on having two LED that detects darkness. Referencing schematics from various sources.

## April 5th, 2026 - Researching

Today I worked on finding schematic ideas. From this website https://www.555-timer-circuits.com/light-detector.html I found a light detector circuit using speakers. I don't want speakers so I'm going to replace it with a resistor and LED. I will also observe Pin 3 and see if it would work.

![image](attachments/LightDetector.gif)

Orginally I wanted to go with one LED because it was simple. Now that I think about it I could just add another LED in parallel. If I had a breadboard I can test it but I am only going to test through theory for now.

I followed the diagram but I ran to a problem, my pins are not in the same orientation as it is in the picture so I had to reroute my wiring so that it can match the pinouts. Pin 3 is output so it should be ok!

I don't like how my schematic looks in my opinion and I really want to clean it up, but the LDR photo resistor should stay between pin 4 and 8 so that's why I designed it that way. Maybe it would be ok but I'll check the datasheet. I want my photo resistor between two pins and then led to anothe resistor in order for it to properly work.

![image](attachments/image1.png)

I put my resistor for LED at 330 ohms so they're bright. I decided that I needed to change where the pins are located because I don't like how it is uneven on the top and I figured it out through the tutorial.

![image](attachments/image2.png)

I ended up changing the pin locations of the 555 timer, and when I tested with DRC, it didn't like that. However it is just a warning and it won't affect the functionally as much so it is totally okay! I initally wanted R3 and RV1 on the top but it didn't look good with a long wire with nothing in between pin 8 and 3. I had to adjust it so the text doesn't overlap on the 555 timer but there was nothing I can do about it to be honest for clean straight lines. That's why Discharge and VCC are close because I wanted R1 and R4 to be connected cleanly. In addition I moved the power flags.

![image](attachments/image3.png)

I also keep running into this error "Error input power pin not driven by output power pins" for my VCC on the top, it only works if I connect it like this...

![image](attachments/image4.png)

I fixed it by adding powerflags.

1[image](attachments/image5.png)
### Time Spent: 1.5 Hours