---
title: "3D-Printable-Laptop-Cooling-Pas"
author: "Enigma_124"
description: "This is a 3D printable Laptop Cooling Pad using Fan controlled by a custom RP2040 based devboard"
created_at: "2026-09-12"
---

So I had no idea that I had to both write devlogs and a lapse. I thought it was one or the other, so here is a condensed form of the devlogs. 

# 2026-08-18 to 2026-08-19
 I was building the voltage protection circuit, which would allow the fans to receive a stable current at 12v with overvoltage protection and prevent reverse polarity. For this, I used a Zener diode and a Fuse. The circuit used can be found [here](https://circuitdigest.com/electronic-circuits/overvoltage-protection-circuit). Then, to safely power the RP2040 chip and OLED, I created a step-down buck converter circuit for 12v to 3.3v using TPS62162DSG.
 ![image](./Assets/Journal%20Images/Day1.1.png)
 ![image](./Assets/Journal%20Images/Day1.2.png)
 ![image](./Assets/Journal%20Images/Day1.3.png)

 **Total time spent: 1.5 hours**

 **Lapse Links:**
 **[Lapse_1](https://lapse.hackclub.com/timelapse/X8WnYXYB8hOf)**
 **[Lapse_2](https://lapse.hackclub.com/timelapse/XAUpE_7vQV7K)**
 **[Lapse_3](https://lapse.hackclub.com/timelapse/_s1kYaglIDFs)**

# 2026-08-20 to 2026-08-21
 I focused on creating the circuit for the RP2040 microcontroller and connected the required pins to the 4-pin headers for the fans and the OLED screen. At first, I accidentally added the OLED and buttons directly into the schematic instead of adding the headers. I also connected the 3 2-pin headers for connecting various buttons. A separate USB-C port was added, which would receive CPU temperatures from the laptop. Then I also changed the barrel connector for power to a usb c port. I also worked on the PWM signals to make sure that they would work for the fans; I used a MOSFET with the source set to ground for this.
 
 ![image](./Assets/Schematic.png)
 ![image](./Assets/Journal%20Images/Day2.1.png)
 ![image](./Assets/Journal%20Images/Day2.2.png)

 **Total time spent: 2 hours**

 **Lapse Links:**
 **[Lapse_1](https://lapse.hackclub.com/timelapse/p1gNmqsvEsqF)**
 **[Lapse_2](https://lapse.hackclub.com/timelapse/HqhyyTd7N_Rm)**
 **[Lapse_3](https://lapse.hackclub.com/timelapse/nn88JlwNwpd7)**

# 2026-08-23 to 2026-08-26
 Today I worked on assigning the various footprints and placing components in the PCB editor. This required a lot of research to find the exact component that would best fit the criteria and was also available here. The components had to be placed in such a manner as to reduce the amount of space required while also keeping enough space in between for routing the traces. This took a lot of time, and I had to redo it once because KiCad crashed on me and my work wasn't saved. Here, KaiPereira's guide was very useful in deciding the footprints of various components and for placement of various components.

 ![image](./Assets/Journal%20Images/Day3.1.png)
 ![image](./Assets/Journal%20Images/Day3.2.png)
 ![image](./Assets/Journal%20Images/Day3.3.png)
 
 **Total time spent: 4 hours**

 **Lapse Links:**
 **[Lapse_1](https://lapse.hackclub.com/timelapse/kjDx_4C6q_NG)**
 **[Lapse_2](https://lapse.hackclub.com/timelapse/O5PsoE4yXPM5)**
 **[Lapse_3](https://lapse.hackclub.com/timelapse/LCT2zhc3__v9)**
 **[Lapse_4](https://lapse.hackclub.com/timelapse/-BpnBDAG_8Td)**
 **[Lapse_5](https://lapse.hackclub.com/timelapse/iVrlwJZ8b8de)**
 **[Lapse_6](https://lapse.hackclub.com/timelapse/inkQ6GUXbBT_)**

# 2026-08-26 to 2026-08-27
 I worked on the traces. At first, I made the board a 4-layer board because I thought the routing would require the extra space, but I was able to route it in 2 layers. While routing the differential pair on the USB-C port for supplying data, it took a lot of time to match the lengths. After the traces were done, I decreased the board size to match the space required.

![image](./Assets/PCB.png)
![image](./Assets/3D-PCB.png)
![image](./Assets/Journal%20Images/Day4.1.png)

 **Total time spent: 1.5 hours**

 **Lapse Link:**
  **[Lapse_1](https://lapse.hackclub.com/timelapse/Tel2IqWKVw8o)**

# 2026-09-03 to 2026-09-10
 I worked on the 3D Structure of the laptop Cooling Pad. This was my second time using Fusion, so the work was slow. To make it match the exact mounting pattern of the P12 Pro, I had to create a circle and cut it into the required shape. To make the design look polished and to make the edges curved, I added fillets- lots and lots of fillets. Also Worked on the README.
 
![image](./Assets/Cooling-Pad1.png)
![image](./Assets/Cooling-Pad2.png)
![image](./Assets/Cooling-Pad3.png)

 **Total time spent: 6 hours**

 **Lapse Links:** 
 **[Lapse_1](https://lapse.hackclub.com/timelapse/1DE9453hYrio)**
 **[Lapse_2](https://lapse.hackclub.com/timelapse/Irt6cRtAdCu3)**
 **[Lapse_3](https://lapse.hackclub.com/timelapse/qC81KXo_HgHI)**
 **[Lapse_4](https://lapse.hackclub.com/timelapse/JuN2IqyEEBJ9)**

# 2026-09-11 to 2026-09-12
 I worked on the code for the RP2040. The imports in the code kept throwing errors even after reinstalling CMake and all the C compilers. The errors were fixed when I opened the folder separately and reran the build instead of opening the parent folder in VS Code. Also completed the Journal.md. I didn't know that I had to create a journal.md until submission, which is why it has less detail and fewer images.
 ![image](./Assets/Journal%20Images/image.png)

 **Total time spent: 2.5 hours**

 **[Hackatime Link](https://hackatime.hackclub.com/@Enigma_124/project/Laptop+Cooling+Pad)**
