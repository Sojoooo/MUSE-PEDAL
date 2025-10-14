---
title: "MUSE Pedal"
author: "Juan Pablo Sojo"
description: "A DIY pedalboard inspired by Chris Wolstenholme’s bass effects"
created_at: "2025-09-10"
time_spent: ~116 Hours
---

# September 10: Inspiration

I've been woking with electronics in music a lot recently, and i fell into the rabbit hole of DIY PEDALS. I've watched lots of videos of people making their own pedals through kits, or schematics, and i've been really curious about analog signaling recently, so i wanted to give it a try.

I didnt want to just put together a kit, i want to make it from the start. And i don't want to just make one, i've desided to make a full on pedal board of different pedals with different effects in just one PCB. I think a project like this might be quite fun and i might learn more in depth about this analog signals, since in my last and first proyect i was learning quite in a rush while making it.

As a reference, i've decided to make a pedal board based on the main gear used by Muse bassits Chris Wolstenholme, since a really dear person of mine bought a bass a bit recently, she loves Muse and chris, and i though a give like this might make her happy while helping me understand more about this topic.

From [equipboard](https://equipboard.com/pros/chris-wolstenholme), i've decided to use:

- "Black Russian" Big Muff Pi V8  
- ZVEX Woolly Mammoth Fuzz  
- Human Gear Animato  
- Boss OS-2 OverDrive/Distortion

![alt text](/assets/equipboard.png)

**Time Spent:** 2h

# September 4: Big Muff Pi

I started making the big muff pi black russian. It was difficult to understand at first what i was doing, since i was also not acostumed to easyeda, but making it was actually quite relaxing. When looking for the pots and the footswitch on lcsc i realized they dont sell them. Specially not pots with does high resistances. Also, i realized how teadious it would be to somehow mount the switched and pots to the board and tracing all that stuff, so i decided to resolve that next day. Another thing is that i decided on using film caps on coupling and filters as they have a low tolerance.

![alt text](/assets/blackrussian_sch.png)

**Time Spent:** 7h

# September 5: Woolly Mammoth

In this day i made the woolly mammoth fuzz. It was actually easier to make. Its really simple. For the footswitches and pots problem, i have decided to mount them to the case. I would get them from somewhere else. Maybe temu, or maybe i could look on some local electronics store. The problem is that, although foot switches for bypass are more standard, pots have more specific resistances and even the taper matters. I looked for options and found affordable footswitches on temu and pots, but they are all linear, while most of the ones i need are log taper. I will keep looking for a solution to this. Either way, i will put screw terminals as the pots and bypass switches so that they can connect the pcb to the mounted pots and switches. I will also add them all to the other side of the pcb so that they dont occupy that much space on it, and any film cap or electrolitic ends up covering the cable hole.

![alt text](/assets/woolly_sch.png)

**Time Spent:** 6h

# September 8: Animato

Today it was the turn of the animato pedal. It took me a while to first understand what the footswitch made. After some extensive research, i found out that it was a layout to half bypass the pedal that was commonly used by pedals, since in that time, 9 pin foot switches werent as common as they are now. Though i say half bypass because it acutally doesnt fully bypass the pedal, it just bypasses the distortion. Because of this, i decided to change it to a full bypass since the pedal board will be all in one pcb, i prefer it so that the user can fully jump over a pedal. After that, i encountered another problem and that was the NTE102/NTE103 transistor pairing. The problem about this transistors are that they are germanium transistors, which stop been mass made a while ago, and they are quite difficult to find. I will just make the schematic without them and resolve that problem next day.

![alt text](/assets/animato_sch.png)

**Time Spent:** 9h

# September 9: Transistor Search

Today i just researched for solutions for the transistors. I found that in the pdf of the schematic, in previous versions a 2N5087/2N5088 paring was used insted of the ones mentioned. Although they arent selling them any more in lcsc, they still have the symbol and footprint. I also found them in mouser. Looking more into mouser i found they sell the log taper or audio taper pots i was needing, so that could be a viable solution to that problem.

**Time Spent:** 3h

![alt text](/assets/transistor.png)

# September 10: Octaver Plan

I was searching into boss pedals, and after seing how more complex the schematics where compared to the previous ones i made, ive started meditating if i actually needed a distortion/overdrive when having a black russian and animato. I decided it was not worth it. Although, when searching more in chris's equipment, i found he also used an boss octaver, which altough it was as difficult to make as the distortion, i think it was more worth it. I couldnt complete this one one day. I got into a bit of a problem, because of the need for a germanium diode, but i found out that schotty diodes with a resistnce have a simmilar funtionality, so i used that. Also, im seeing some ics i dont really get, and something about 4V i dont really understand, but i managed to do a lot.

![alt text](/assets/schotty.png)

**Time Spent:** 9h

# September 11: Octaver Flip-Flops

I found out those ics where some kind of flip flops. After checking the schematic and asking my teacher, i think the 4v should be conected between each other but im not sure. Im going to add some terminals in case they do need to get connected and connect them if the pedal doesnt work. I finished the pedal.

![alt text](/assets/octaver_sch.png)

**Time Spent:** 6h

# September 13: I/O System

I made the output and input of the pedal. The jack will be the only interactve piece mounted to the pcb. I added a system bypass so that you can easily bypass all the active pedals easely. I also added a prebuffering, even before the bypass, so that the signal doesnt loses strenght.

![alt text](/assets/input_sch.png)

**Time Spent:** 6h

# September 15: Power Circuit

Today i just made the power. Im going to mount the dc jack to the case. I also added a schotty so you connect it incorrectly. I took way too long with this part since i wanted to use a mosfet insted of the schotty to reduce the voltage drop, but i finally decided i didnt actually understood what i was doing and gave up.

![alt text](/assets/power_sch.png)

**Time Spent:** 1h

# September 16: PCB Start

Start of the pcb. I decided to arrange the pedals as: Octaver, big muff, animato and woolly. I started with the black russian as i though it was the most satisfactory. I made it so it could be as compact as it could, trying to just use the top layer for sound traces, and bottom layer for power. I was succesfull.

![alt text](/assets/blackrussian_pcb.jpg)

**Time Spent:** 6h

# September 17: PCB Progress

I made the woolly mammoth next. It was a bit easier that the last one. quite fun and relaxing.

![alt text](/assets/woolly_pcb.jpg)

**Time Spent:** 5h

# September 18: Animato Layout

Next it was the animato. It was a a bit larger than the previous ones, but still quite simple. I actually started measuring the size of the different pedal seccions and was quite surprised by how small they where. I was actually a bit worried, since i hadnt seen pedals that small, and maybe they where ment to be large for a reason. I ended up discovering that it was probably because of the pots mounted on the pcb, which i had solved with the screw terminals, so there was probably no real threat.

![alt text](/assets/animato_pcb.jpg)

**Time Spent:** 8h

# September 19: Octaver Layout

Last pedal. I was a bit rushed today so i could finish it. It was even a bit more difficult since in previous ones i was able to mantain a more rectangular/square shape for the overall layout, but because of the amount of chips, it was getting a bit difficult to preimagine how to make it a pretty coherent shape. I think it might be possible next day.

**Time Spent:** 6h

# September 20: PCB Done

I finished the octaver. I was able to mantain a pretty shape.  
I layed out all the pedals as they would be connected. I put in order from left to right, since i will be probably flipping the board when i mount it to the cad. This is to make it so that the input and output goes from right to left, which i have seen in most of the pedals i have used. I think is something about most of them like been made in japan. I also made arranged the input and output and power and connected it all. Also, to diminish interference, i made the bottom and top layer gnd planes with stitching vias.

![alt text](/assets/pcb_finish.png)

**Time Spent:** 7h

# September 21: CAD Start

Today i started making the cad with the pcb as the model. I forgot to make the screw holes in the pcb so i added does. I decided on m3 screws. I was just able to make the top holes for the different things mounted and the screw holes to hold the pcb.

![alt text](/assets/case_cad.png)

**Time Spent:** 9h

# October 4: Case Work

After a short break for exams, i’m back. Im going to finish the cad. I added the bottom lid. I though about it i and prefered it that way since i dont want to see the screws on the top. Although it took me a while, i finally decided on a layout to maximize the space inside and includes the 8 screw holes i need for all the mounting. I added the the jack input and output holes. I was not quite sure how i would fit the pcb inside the case with does sticking out, but i think i did i wide enought and rounded the corners of the jack hole to make it wasier to fit inside. I also added the dc jack hole.

![alt text](/assets/case_holes.png)

**Time Spent:** 10h

# October 5: Final CAD + Silk

When adding the cad to jlccnc, i discovered somehow it was cheaper to add a silk screen to the cad, so i did that. I think i made a cool design. It also said that for threaded holes you needed a drawing telling the specifications, which led me into a rabbit hole of threaded holes, but at the end it wasnt that hard.

![alt text](/assets/case_thread.jpg)

**Time Spent:** 10h
