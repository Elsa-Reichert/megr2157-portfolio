# A4 – [Topic]

## Objective
The objective for this project is to deisgn a motor mount for this motor that attaches to a rigid wall: [link to motor](https://www.omc-stepperonline.com/brushed-24v-dc-gear-motor-3-6kg-cm-46rpm-w-99-5-1-planetary-gearbox-pa28-28245800-g100). After researching motor mounts, I will deisn for yield strenth then for a maximium deflect at the free end. I am allowed to select betweem ABS, PETG, or PLA for the material. 

## Analyze
### Reseaerch
A motor moment is designed to keep a motor place, hold the motors weightm and absorb vibartions. There are four common types solid rubber, hydraulic (fluid filled rubber), polyurethane, and electronic/active. Solid rubber is the simplest, cheapest and standard for most vehicles. For that reason my design will be a solid rubber motor mount.
[Source](https://autobuffy.com/newsroom/what-is-a-motor-mount-engine-mounts-explained)

<img width="952" height="776" alt="image" src="https://github.com/user-attachments/assets/db40c7f5-0476-43ba-b00f-5d42527e499a" />
Here is a simple motor mount from [gimsonrobotics.co.uk](https://gimsonrobotics.co.uk/products/stainless-steel-motor-mounting-bracket-for-45mm-gearboxes?_pos=1&_sid=e3835547a&_ss=r) made of 304 stainless steel. 

<img width="600" height="425" alt="image" src="https://github.com/user-attachments/assets/f6ce1c7b-a546-40de-a827-4a2939be6e33" />
Another simple design form [pololu.com](https://www.pololu.com/product/2266) made of aluminum. 

### Givens
We are designing for the Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox attached to a ridid wall A. Maximium deflection is .30mm at the free end. The materials can be either ABS, PETG, or PLA. I need to account for a safety factory of 3. Weight of the motor can be ignored.

ABS: yeild strength = 32-45MPA, E (ypungs Modulus) = 1.7 - 2.6 Gpa [source](https://matmake.com/materials-data/acrylonitrile-butadiene-styrene-properties.html)
PETG: yeild strenth = 46.2 MPa, E = 1939 MPA. [source](https://um-support-files.ultimaker.com/materials/2.85mm/tds/PETG/Ultimaker-PETG-TDS-v1.00.pdf)
PLA: yield strenth = 52.5 MPa, E = 3250 Mpa. [Source](https://um-support-files.ultimaker.com/materials/2.85mm/tds/PLA/Ultimaker-PLA-TDS-v5.00.pdf)

Imagie of the motor, the rigid wall, and the force p. P=300N
<img width="153" height="113" alt="image" src="https://github.com/user-attachments/assets/ecc51106-ddf0-48af-ba1d-226a9c079dca" />

### Feature 1
My first task is to design a feature of the mount that is attached to the motor. The deflection of the feature is zero and the derivative with respect to x is also zero, which means I can treat the feature as a cantilever beam while solving for cross sectional area. The safety factory accounts for the holes and skrews in the motor mount. I need to determind the cross sectional area gemotry using the equations for both stress and deflection. 

Givens: P=300, Yeild stress = 51.6 MPa, E = 3131 MPa, Max. deflection = .30 mm, Safety factor = 3

I decided to use PLA for the building matrial. The source I used gave a range for both the yeild strength and Youngs Modulus. I am using the lowest posible value just to be safe. 

Bending

We are given a force p that is applied to the shaft of the motor. My first step is to figure out the momentum on the end of feature one. Force P is the only force acting because we are neglecting the weight of the motor. I need to find the vertical distance of E and the force vector P. Looking at the diagram given on the motors manicfactoring webside, the shaft is about 18mm. 

My first thought was to have the shaft stick out intirly and add half the height of the beam. The issue with this was I would have an unknown verrible in my moment eqution and a lot of the motor mounts have space for the shaft to stick into and stay in place. 

<img width="353" height="257" alt="image" src="https://github.com/user-attachments/assets/67ad6c12-2967-4fac-8731-b8e8b320ea9d" />


I then desided on something like this to find the moment and vertical distance from P. I drew a faint dotted outline of the motor. The manufactorer gave a value with a 1 mm tolenernce. I decied to use 18mm as the distance value beacuse it was close, there is a tolenernce so I wouldnt be able to get an exact value, and the body of the motor rests above the center of the beam my calulated moment value would most likely end up being higher then the actual value at that point. This is good because the motor shaft could end up a different size, and using a higher momentum will make it safer. 

<img width="630" height="445" alt="image" src="https://github.com/user-attachments/assets/aea22497-3008-426e-8566-9f7cbcb7fc59" />
<img width="292" height="118" alt="image" src="https://github.com/user-attachments/assets/9f1875b0-48b8-4edb-9f6f-03ecbfdc6b4e" />



This gives us a M = 5400 N * mm appliedat the end of the beam going clock wise.

I realized the moment at the top end of the beam would be the highest. So I went back and changed the vertical distance from P value to 22mm. This extra height gives more space for the motor to sit into this feature, as while as gives me the largest postible moment calulation. 

<img width="575" height="461" alt="image" src="https://github.com/user-attachments/assets/b11de8bc-db0f-4e57-bd73-6398b5cf907b" />


This gives us a M = 6600 N * mm at point e moving clock wise. Now I can use the bending equation to find the cross sectional area

I first started using the max. stress. I used a rectange cross section the first time I tried to solve it and realized I would need a third equaction. Here was the math the setech for that.

<img width="393" height="512" alt="image" src="https://github.com/user-attachments/assets/4bf78aab-5f89-44d5-802a-b4797dd79975" />


I solved it again using a square cross sectinoal area. 
<img width="618" height="122" alt="image" src="https://github.com/user-attachments/assets/d3d1ce9d-37e0-4038-b38f-5fa3c189a141" />

<img width="322" height="410" alt="image" src="https://github.com/user-attachments/assets/b1471172-6a20-45a8-a9d9-8861d40e95a4" />
<img width="430" height="416" alt="image" src="https://github.com/user-attachments/assets/a9a324f4-512a-4e1f-b10c-10cf6c6a2305" />

Next I need to find the minimium length using the bending deflection equation

I need to use a safety factor of 3 for this feature. The equation given for deflection uses youngs modulus. I have only ever used a safety factor to calculate the allowble stress or strain. I still Think it is important to have a safety factor. I decided dividing the E value by 3 for the safety factor would fuctino the same, because youngs modulus is related to both stress and strain. My other itea was to divid the max. deflection by the safety factor, whcih wouldve had the same result but dividing the E value is more simular to what i have seen. 

<img width="2156" height="2762" alt="image" src="https://github.com/user-attachments/assets/cf0d61b0-08ae-4b3e-be9a-562a5dd817c1" />
<img width="2182" height="1723" alt="image" src="https://github.com/user-attachments/assets/8ec9a114-6dea-4fe1-906b-967e9154048d" />

### Feature 2
I need to design a feature of the mount to be attached to the wall. I can assume the rigid wall A can support bolts. I will be determining the cross sectinoal gemoetry using the same method.

The moment for this feature is going to be different because it is at a different locatino realative to force p. My first step is to find the moment acting at the bottom corner. 

<img width="2078" height="1989" alt="IMG_8319" src="https://github.com/user-attachments/assets/e09dfff3-2c42-45f0-8b4f-c05e2439ff83" />

The moment ending up being the same value. I believe the gemoetry will end up the same because I will still be using a square cross section, the same materials, and the same givens. This will make the calculations quick.

<img width="2159" height="3049" alt="IMG_8320" src="https://github.com/user-attachments/assets/e40f46a6-55ff-4084-b1b8-0bca09b1473e" />
<img width="2239" height="2725" alt="IMG_8321" src="https://github.com/user-attachments/assets/a0687145-f210-4625-a2b5-b1356de29d7f" />

I did end up with the same a value.

Now the L calculation
<img width="2428" height="2757" alt="IMG_8322" src="https://github.com/user-attachments/assets/7bee841d-76db-4d13-8207-35cd33953197" />
<img width="2394" height="2365" alt="IMG_8323" src="https://github.com/user-attachments/assets/ef871f8a-f1fb-4ccc-9295-168e7f74a88c" />

I realized the square geometry would not work with the design. The found a value would be to small for the motor. I was going to go through and recalculate everything for a retange but the Area and a values found are minimiums. so I don't need to. Larger a values would give me a larger L max. I will recalculate that after choosing new values. 

The diamater of the motor is 22mm. I will choose 24 mm as my a value. This gives me 576 mm^2 for my area this is well above my calulated minimium area. 

Pluging in a = 24mm to my L max. equation from before I get L = 72.43mm.
### Isometric view sketch 
Using these values I came up with this design
<img width="3024" height="2066" alt="IMG_8324" src="https://github.com/user-attachments/assets/189abfc7-3eea-46b5-9211-f9a3214163e7" />

### 3D CAD mode;
I next needed to recreate my design on a CAD program I did this on Solidworks. 

First thing I did here was create equations for the variables to parametrically model it. 
<img width="822" height="300" alt="Screenshot 2026-09-16 224830" src="https://github.com/user-attachments/assets/b4961fb9-bab8-4b1f-b00f-c273514954fd" />

Used two bose extrudes
<img width="562" height="520" alt="Screenshot 2026-09-16 225007" src="https://github.com/user-attachments/assets/4c45e730-868b-4761-ab36-5eeb0a9e2baf" />

Added two more vararibles for the screw. 
<img width="717" height="41" alt="Screenshot 2026-09-16 235618" src="https://github.com/user-attachments/assets/85dce251-ea9a-4226-9999-7e9304d2afd6" />

Used a cut extrude to create the first screw hole than made a linear pattern.
<img width="570" height="626" alt="Screenshot 2026-09-16 233747" src="https://github.com/user-attachments/assets/a02e6690-1a9e-4ed0-8010-1a80b845e5a4" />

Then last I cut extruded the three holes for the motor to rest in. 
<img width="627" height="567" alt="Screenshot 2026-09-16 234044" src="https://github.com/user-attachments/assets/5ceb840b-0ad7-4cf6-8c62-71611d47a347" />
<img width="290" height="435" alt="image" src="https://github.com/user-attachments/assets/0381d3a2-0fab-4443-b23c-b18dc01bfe53" />

I did not give an clearance for the shaft holes.
<img width="940" height="315" alt="image" src="https://github.com/user-attachments/assets/d2d5f9a9-2309-4a29-8446-335050673766" />

### 3D Model Drawing
<img width="1999" height="1545" alt="image" src="https://github.com/user-attachments/assets/396b28c5-e924-460a-82c2-4b70ff05f78d" />
[CAD drawing PDF](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A04/a4%20drawing.pdf)


## Decide


## Communicate

