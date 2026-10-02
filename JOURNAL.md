---
title: "3D-Printable-Laptop-Cooling-Pas"
author: "Enigma_124"
description: "This is a 3D printable Laptop Cooling Pad using Fan controlled by a custom RP2040 based devboard"
created_at: "2026-09-12"
---

At first, I didn’t realize I needed to write devlogs and record timelapse videos. I thought it was one or the other, so I have written a summarized version of the devlogs.

# 2026-08-18 to 2026-08-19
I designed a voltage protection circuit to ensure that the fans receive a stable 12V supply. This circuit includes overvoltage protection and safeguards against reverse polarity. To achieve this, I used a Zener diode and a fuse. For guidance on the Zener circuit, I referred to a tutorial on CircuitDigest, which can be found [here](https://circuitdigest.com/electronic-circuits/overvoltage-protection-circuit). 

Additionally, to power the RP2040 chip and OLED safely, I created a step-down buck converter circuit to convert 12V to 3.3V using the TPS62162DSG.

 ![image](./Assets/Journal%20Images/Day1.1.png)
 ![image](./Assets/Journal%20Images/Day1.2.png)
 ![image](./Assets/Journal%20Images/Day1.3.png)

 **Total time spent: 1.5 hours**

 **Lapse Links:
  [Lapse_1](https://lapse.hackclub.com/timelapse/X8WnYXYB8hOf)
  [Lapse_2](https://lapse.hackclub.com/timelapse/XAUpE_7vQV7K)
  [Lapse_3](https://lapse.hackclub.com/timelapse/_s1kYaglIDFs)**

# 2026-08-20 to 2026-08-21
I focused on creating the circuit for the RP2040 microcontroller and connected the necessary pins to the 4-pin headers for the fans and the OLED screen. Initially, I mistakenly added the OLED and buttons directly to the schematic instead of including the headers. Additionally, I incorporated a separate USB-C port that would receive CPU temperature data from the laptop. I replaced the barrel connector for power with a USB-C port. Furthermore, I worked on the PWM signals to ensure they would properly operate the fans, using a MOSFET with the source connected to ground for this purpose.
 
 ![image](./Assets/Schematic.png)
 ![image](./Assets/Journal%20Images/Day2.1.png)
 ![image](./Assets/Journal%20Images/Day2.2.png)

 **Total time spent: 2 hours**

 **Lapse Links:
  [Lapse_1](https://lapse.hackclub.com/timelapse/p1gNmqsvEsqF)
  [Lapse_2](https://lapse.hackclub.com/timelapse/HqhyyTd7N_Rm)
  [Lapse_3](https://lapse.hackclub.com/timelapse/nn88JlwNwpd7)**

# 2026-08-23 to 2026-08-26
Today, I worked on assigning various footprints and placing components in the PCB editor. This involved extensive research to find the exact components that matched the criteria and were available. I had to arrange the components in a way that minimised the space required while still allowing enough room for routing the traces. This process took a significant amount of time, and I even had to redo it once when KiCad crashed and my work wasn’t saved. Kai Pereira's guide was very helpful in determining the footprints of the components and assisting with their placement.

 ![image](./Assets/Journal%20Images/Day3.1.png)
 ![image](./Assets/Journal%20Images/Day3.2.png)
 ![image](./Assets/Journal%20Images/Day3.3.png)
 
 **Total time spent: 4 hours**

 **Lapse Links:
  [Lapse_1](https://lapse.hackclub.com/timelapse/kjDx_4C6q_NG)
  [Lapse_2](https://lapse.hackclub.com/timelapse/O5PsoE4yXPM5)
  [Lapse_3](https://lapse.hackclub.com/timelapse/LCT2zhc3__v9)
  [Lapse_4](https://lapse.hackclub.com/timelapse/-BpnBDAG_8Td)
  [Lapse_5](https://lapse.hackclub.com/timelapse/iVrlwJZ8b8de)
  [Lapse_6](https://lapse.hackclub.com/timelapse/inkQ6GUXbBT_)**

# 2026-08-26 to 2026-08-27
I worked on the traces for the PCB. Initially, I designed it as a 4-layer board, thinking that the routing would need the extra space. However, I was able to successfully route it using just 2 layers. Routing the differential pair for the USB-C port, which supplies data, took a considerable amount of time to ensure the lengths were matched correctly. Once the traces were complete, I reduced the board size to fit the required space.

![image](./Assets/PCB.png)
![image](./Assets/3D-PCB.png)
![image](./Assets/Journal%20Images/Day4.1.png)

 **Total time spent: 1.5 hours**

 **Lapse Link: **
  [Lapse_1](https://lapse.hackclub.com/timelapse/Tel2IqWKVw8o)**

# 2026-09-03 to 2026-09-10
I worked on the 3D structure of the laptop cooling pad. This was my second time using Fusion, so the process was slow. To ensure it matched the exact mounting pattern of the P12 Pro, I had to create a circle and trim it into the required shape. To give the design a polished look and to curve the edges, I added many fillets. I also worked on the README document.
 
![image](./Assets/Cooling-Pad1.png)
![image](./Assets/Cooling-Pad2.png)
![image](./Assets/Cooling-Pad3.png)

 **Total time spent: 6 hours**

 **Lapse Links:
 [Lapse_1](https://lapse.hackclub.com/timelapse/1DE9453hYrio)
 [Lapse_2](https://lapse.hackclub.com/timelapse/Irt6cRtAdCu3)
 [Lapse_3](https://lapse.hackclub.com/timelapse/qC81KXo_HgHI)
 [Lapse_4](https://lapse.hackclub.com/timelapse/JuN2IqyEEBJ9)**

# 2026-09-11 to 2026-09-12
I worked on the code for the RP2040. I encountered errors with the imports, even after reinstalling CMake and all the C compilers. The issues were resolved when I opened the specific folder separately and reran the build, rather than opening the parent folder in VS Code. I also completed the Journal.md. I wasn't aware that I needed to create a journal.md until the submission deadline, which is why it contains less detail and fewer images.

 ![image](./Assets/Journal%20Images/image.png)

 **Total time spent: 2.5 hours**

 **[Hackatime Link](https://hackatime.hackclub.com/@Enigma_124/project/Laptop+Cooling+Pad)**
