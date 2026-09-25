---
title: "3D-Printable-Laptop-Cooling-Pas"
author: "Enigma_124"
description: "This is a 3D printable Laptop Cooling Pad using Fan controlled by a custom RP2040 based devboard"
created_at: "2026-09-12"
---

So I had no idea that I had to both write devlogs and lapse. I thought it was one or the other, so here is a condensed form of the devlogs. 

# 2026-08-18 to 2026-08-19
 I was building the voltage protection circuit, which would allow the fans to receive a stable current at 12v and prevent reverse polarity. For this I used a zener diode and a Fuse. Then for safely powering the RP2040 chip and oled I created a step down convertor cicuit for 12v to 3.3v.
 ![image](./Journal%20Images/Day1.1.png)
 ![image](./Journal%20Images/Day1.2.png)


 **Total time spent: 1.5 hours**

# 2026-08-20 to 2026-08-21
 I focused on creating the circuit for the RP2040 microcontroller and connected the required pins to the 4-pin headers for the fans and the OLED screen. At first I accidently added the oled and buttons directly into schematic instead of adding the headers. I also connected the 3 2-pin headers for connecting various buttons. A separate USB-C port was added, which would receive CPU temperatures from the laptop. Then I also changed the barrel connector for power to a usb c port. I also worked on the pwm signals to make sure that they would work for the fans, I used a mofset with source set to gorund for this.
 
 ![image](./Assets/Schematic.png)
 ![image](./Journal%20Images/Day2.1.png)
 ![image](./Journal%20Images/Day2.2.png)

 **Total time spent: 2 hours**

# 2026-08-23 to 2026-08-26
 I worked on assigning the various footprints and placing components in the PCB editor. This tookk a lot of time as I had to decide the exact components while keeping the price down. Their avalibilty in India was also a problem. Here KaiPereira's guide was very useful in deciding footprints of various components.

 **Total time spent: 4 hours**

# 2026-08-26 to 2026-08-27
 I worked on the traces. At first, I made the board a 4-layer board as I thought the routing would require the extra space, but I was able to route it in 2 layers. While routing the differential pair on the USB-C port for supplying data, it took a lot of time in length matching. After the traces were done I decreased the board size to match the space required.

![image](./Assets/PCB.png)
![image](./Assets/3D-PCB.png)

 **Total time spent: 1.5 hours**

# 2026-09-03 to 2026-09-10
 I worked on the 3D Structure of the laptop Cooling Pad. This was my second time using Fusion, so the work was slow. To make it match the exact mounting pattern of the p12 pro I had to create a circle and cut it into the required shape. To make the design look polished and to make the edges curved I add fillet, lots and lots of fillets. Also Worked on Readme.
 
![image](./Assets/Cooling-Pad1.png)
![image](./Assets/Cooling-Pad2.png)
![image](./Assets/Cooling-Pad3.png)

 **Total time spent: 6 hours**

# 2026-09-11 to 2026-09-12
 I worked on the code for the RP2040. The imports in the code kept throwing errors even after reinstalling CMake and all the C compilers. The errors were fixed when I opened the folder separately and reran the build instead of opening the parent folder in VS Code. Also completed the Journal.md. I didn't know that I had to create a journal.md until submission which is why it has less detail and few images.

 **Total time spent: 2 hours**

