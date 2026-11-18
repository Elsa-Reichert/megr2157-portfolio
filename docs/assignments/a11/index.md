# A11 - Motor Selection Design Part 2

## Objective

Maxwell's Section

My task was to pick and select key components for the frame and motor mount of the tensile tester we created last week using Grainger as a resource tab and other various sources of information to collect data to formulate various reasonings why each selected component was chosen and the purpose they serve for the tensile tester. I selected the motor, motor type, a coupler/connector, and finally the brackets for the frame of the machine.

<img width="715" height="176" alt="image" src="https://github.com/user-attachments/assets/35d6ea28-9742-4508-a27f-82df7a958ebf" />

<img width="674" height="123" alt="image" src="https://github.com/user-attachments/assets/4ee72d7a-7ea7-4b3b-b7fc-607df6569034" />

<img width="695" height="149" alt="image" src="https://github.com/user-attachments/assets/97e577f1-998e-41e7-905e-8aec5d83b69b" />

## Analyze
### Maxwell's Motor Analysis
Firstly, I started with selecting the appropriate motors for the machine. I had a choice to pick between DC, stepper, and gearmotor motors. I selected gearmotor as per my reasonings and analysis below, along with the specifications and data of the selected motor:

[MP24-DataSheet-US.pdf](https://github.com/user-attachments/files/34981738/MP24-DataSheet-US.pdf)

<img width="684" height="812" alt="IMG_3111" src="https://github.com/user-attachments/assets/7ac331ce-9a14-4c6f-ab3d-8dbc67fa44fc" />

<img width="536" height="364" alt="MP24 estimated continuous torque-speed curve" src="https://github.com/user-attachments/assets/8971bed1-009d-44ba-b0d2-4eb98dd58440" />

I chose the selected motor and generated the Speed-torque curve chart using ChatGPT by plugging in the data supplied by the Datasheet for the selected motor.

### Elsa's motor mount bracket or housing section

I needed to design a bracket to attact the motor to the frame. This frame needs to have four hole patterns to secure the mount. 

The width, high, and location of holes where based on the drawing of the motor being used.

<img width="1078" height="695" alt="image" src="https://github.com/user-attachments/assets/bfe8386d-7bea-4784-a7dc-c00631707919" />

The equation for max. deflection, stress, moment of inertia, and the section modulus are all from the 29th edition of the mechinary's handbook are are listed below. 

<img width="1138" height="195" alt="Screenshot 2026-11-18 150850" src="https://github.com/user-attachments/assets/d575ec1d-65c6-4e54-a8ff-8078b6c857db" />

<img width="497" height="260" alt="Screenshot 2026-11-18 165359" src="https://github.com/user-attachments/assets/396fe143-c06d-481e-b57a-51f5fb8beb4e" />

I choice alloinium alloy 6061 T6 for the material. Sources for the properties are from this website: https://mechcodex.com/materials/6061-t6-aluminum. 

Work for finding the minimium thickness:

<img width="2701" height="3326" alt="IMG_8633" src="https://github.com/user-attachments/assets/bc58dd86-914c-465c-b228-232b7239b0ff" />

I first found the minimium thickness using the bending equation. I chose .1mm as the max. deflection, because that has been used frequanlty in past assignemts.

<img width="2110" height="1568" alt="IMG_8634" src="https://github.com/user-attachments/assets/5666f6b4-3765-467b-9b66-98a32e75b6ab" />

<img width="2143" height="1128" alt="IMG_8635" src="https://github.com/user-attachments/assets/1ac8fcb0-9594-45ce-8410-356b7e12f3b4" />

Then I needed to check the minimium thickness using the stress equation. The found t value here was larger.

<img width="2286" height="2543" alt="IMG_8636" src="https://github.com/user-attachments/assets/7c33d4b7-c196-4050-8719-ff47495482dc" />


### Maxwell's Coupling Analysis
With the aid of various internet sources and AI, I researched various types of connectors and couplers on Grainer to find which would be the most ethical and appropriate for the tensile tester. One thing that caught my attention was for Flexible Jaw-Couplers, which were marketed as easy to install, long lasting, and perfect for axial forces supplied by the leadscrews. The other info that caught my attention was how it was also marketed to accomodate small misalingments should there be any.

With more research and data, as shown below, I discovered a Jaw-Coupler is 3 parts, 2 couplers and a center spider to catch the shocks caused by vibrations. One coupler would be attached to the leadscrews, the other to the motors with the center spider in the middle.

<img width="684" height="812" alt="IMG_3112" src="https://github.com/user-attachments/assets/361298bd-fc6a-4bdf-8b5a-fb99d225e7c6" />

### Maxwell's Analysis on Brackets

My last objective was to select a bracket that would support/aid the frame from the torsion the motors would afflict onto the frame during operation. This meant I had to select something sturdy and ethical that isn't too bulky and unnecessary while also not being too small and fragile.

<img width="684" height="812" alt="IMG_3113" src="https://github.com/user-attachments/assets/b5e2133d-7a00-4613-bca7-6500cd8c4424" />

### Elsa's analysis of the top frame

I need to verify that a heavy 40 series will provie the strength to hold the load and torque. I will do this using FEA analysis on solidworks. 

### 
## Decide
### Motor
<img width="558" height="340" alt="Screenshot 2026-11-17 102508" src="https://github.com/user-attachments/assets/1e117e1f-fce1-4bed-a103-0b965cbcf970" />

Total for 2 motors: Varies from 600-800 dollars each depending on gear ratio.
### Coupling/Connectors
Motor Side hub X 2 = $418.74

<img width="650" height="240" alt="Screenshot 2026-11-17 105522" src="https://github.com/user-attachments/assets/d1be82fc-6fc2-4a87-8214-3fad75e488d1" />

<img width="566" height="362" alt="Screenshot 2026-11-17 105533" src="https://github.com/user-attachments/assets/2c95000f-c702-4e23-9b87-74cb76c2f49c" />

Leadscrew Side hub X 2 = $418.74

<img width="678" height="236" alt="Screenshot 2026-11-17 105639" src="https://github.com/user-attachments/assets/25c8aa61-273a-4226-9e9c-a07bd5fd53ca" />

<img width="546" height="362" alt="Screenshot 2026-11-17 105652" src="https://github.com/user-attachments/assets/877af276-8e2e-4e95-aff8-f335aca17551" />

Center Spider X 2 = $104.98

<img width="680" height="208" alt="Screenshot 2026-11-17 105905" src="https://github.com/user-attachments/assets/337aaaf7-1783-4ef5-a3db-c471486063cd" />

<img width="556" height="264" alt="Screenshot 2026-11-17 105920" src="https://github.com/user-attachments/assets/7484d44b-818e-4f0d-9e9f-164ff5435e38" />

All of this was found on Grainger.com

### Bracket
<img width="568" height="190" alt="Screenshot 2026-11-17 112042" src="https://github.com/user-attachments/assets/5b124e91-8409-47a0-8550-f421774e0a67" />

<img width="632" height="218" alt="Screenshot 2026-11-17 112005" src="https://github.com/user-attachments/assets/b12ff212-4f2f-4e68-a8bb-75d4afc2c62e" />

4 brackets = $79.96

## Communicate

Lesson Learned: The big lesson in this whole project was having to use every single tool at my disposal; calculators, equations, formulas, books, AI, the internet, resource tabs, everything, to find and select various parts to put together and create something. It's a good representation of what some engineers go through daily with various jobs that have unique parameters every job. Maybe some of it is a little easier, but the same level of critical thinking and experience are what separates this project from full fledge professional engineers who have had a much longer time to get used to these kinds of assignments and have built tolerances to the stress and mistakes one can make along the way.

Total time: 4.5 hours X $35 per hour for labor costs = $157.5
