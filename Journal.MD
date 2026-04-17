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

![image](attachments/image5.png)

Here is the schematic and I added some short notes regarding some components or the integrated circuit.

![image](attachments/image6.png)

### Time Spent: 2 Hours

## April 6th, 2026 - PCB editing!

As I move onto the next step, and I don't have really much I can do for the schematic for now, I need to think of an accessible but distinct PCB edge cut. Having sharp obtuse corners are not cool and can hurt. I would love create a light sensor PCB keychain to hang. With a case obviously if it is going to be hung. The little components can get stuck on something and break! I wanted to do an owl but then when there is light the LEDs would be on so probably not.

I also thought of chemistry themed PCB design... I am taking chemistry right now and I'm going to go with something simple like the LEDs for the eyes in general. I thought about a crow after looking through my art gallery because I drew one. So maybe I'll stick with a crow? For now I'll go to Proceate and sketch it out. Ooh! A cockatiel with a knife! Parrots are silly and sassy creatures. i remember drawing a cockatiel with a knife as a sticker... Or a crow with a knife would work. Just a bird in general. With flaming red LEDs hehe.

Some of the crow pictures I tried drawing and it was too hard. I prefer side profile view though and that means having to a single LED only. Decided to scrap the idea of two LEDs because I persisted and didn't given in to the single LED!

![image](attachments/image7.png)

Here is the inspiration

![image](attachments/image8.png)

Now I will start to trace a vector graphics outline to insert into KiCad. This is my vector graphic that is also scaled in pixels!

![image](attachments/image9.png)

I forgot to add footprints. Let me assign it right now. I also changed the schematic to be consistent in orientation so it is readable.

![image](attachments/image10.png)

Why it seems small, but it is within the 100x100mm constraint though.

![image](attachments/image11.png)

It's okay! I can manage it. I have created the edge cuts layer and traced it over. I'll stop here probably and come back when I'm available, free from school obviously.

### Time Spent: 1.5 Hours

## April 8th, 2026 - PCB layout and design

I recorded this process on lapse. Ugh this was so annoying with the shape I came up with. Had to do a lot of arranging to try to get it within some borders but I don't think the PCB would be readable at all if I did this. It finally worked and then I wanted to add silkscreen details :/

![image](attachments/image12.png)

Well I ended up changing the edge outline to be more smooth but then my lines were of random degrees and not 45, 135, whatever degree in fourths. I ended up doing fillet lines manually. I also couldn't draw the beak on the silkscreen with the snap thing going on. I actually wanted to keep it that way because I think it'll be easier on the manufacturers.

![image](attachments/image13.png)

I also made the silkscreens overlap one another for the decorations. This was were I left off for today, adding a github link to myself. Basically I made a lot of changes trying to adjust the USB connector and the feet. The feet I completely reworked because it'd be very sharp and a bad thing so no-no. Used ground fill for my ground connections. Everything managed to fit one the top layer which was great though.

![image](attachments/image14.png)

### Time spent: 1.5 hours

## April 10, 2026 - Final Changes Hopefully?

For today I changed some of the orientation for example R6 on the beak. Just makes it more legible to read. Checking again with DRC I left a few loose tracks so I'll just reconnect them. Additionally in R2 and R1 I slightly changed the routing so they don't go over the silkscreen rendering the text illegible.

![image](attachments/image15.png)

I think I'm good with these changes because if I wanted to make more, I'd probably have to do hours again to overhaul the layout which is fine but this one works with short tracks.

![image](attachments/image16.png)

Last few checks and I moved the LDR to be more aligned because it looked off putting.

![image](attachments/image17.png)

Then I moved the LDR again because it was blocking the R5 designator and the edge cuts as it was a little bigger than I intended to drew in the reference, the knife part doesn't align with the handle length. Oh and RV1 solder mask conflict with silkscreen so I slightly moved it away from the R3. I would want to move R3 because the solder mask is close to the silkscreen. I also wanted to add the head silkscreen deco for depth according to my reference but it overlaps with RV1 soldermask so I cut the circle into a third of a quarter. In addition I removed the circles around the LEDs, originally it was going to be the eyes but I already have the LEDs as eyes and it takes up too much space on the PCB. Moved R3 closer to R4 to minimize tracks and it is connected to each other on the schematic. The LEDs changed orientation so the signal trace is on the bottom for the resistor to go to. Finally I fillet the edges I just changed. I believe this should be finally be the final product. I don't want to add any text besides my Github or anything since I have nothing to say LOL

![image](attachments/image18.png)

3D view

![image](attachments/image19.png)
![image](attachments/image20.png)

Final Schematic
![image](attachments/image22.png)

Attempted to create Hero image in Fusion 360. Onshape didn't work for me so I used Fusion 300

### Time Spent: 1.5 Hour

## April 11, 2026 - Hero Image

I opened up Fusion 360 but silkscreen cannot be imported. Searched it up and I would need to export the geometry which would lag my tiny little Macbook so I didn't do it.

Thus I left it as it is and most people won't think of the hero image once they get the kit. I wanted to label the LDR since it is what makes the PCB distinctive from other components.

![image](attachments/Bird%20with%20Knife%20PCB.png)

### Time Spent: 0.5 Hour

## April 17, 2026 - Revisions

After reading feedback on the project, I changed the GitHub to this repository directly. It makes sense for people to be linked directly to this project instead of a confusing profile. I moved the link to somewhere over the top because the name was too long on the bottom.

![image](attachments/image23.png)

New Back view

![image](attachments/image24.png)

I am also considering updating the Hero Image to link to this repo as well so I did. Then once I finish it I reupdated the project and production fies. The image got overwritten, and the original was initally linked to profile.

Final PCB image hopefully

![image](attachments/image25.png)

### Time Spent: maybe 30 minutes?