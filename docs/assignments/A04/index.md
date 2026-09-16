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


## Decide


## Communicate

