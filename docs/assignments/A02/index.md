# A2 – Truss Stress Analysis

## Objective
My assignment was to design a truss using A500 structural steel, given force, and geometric constraints. After designing the truss, I needed to analyze each joint in the truss by creating free body diagrams to figure out every internal force. Once I found each internal force, I was able to use the largest force to find the minimum cross sectional area needed to support the truss. Using my found values, I calculated an estimated weight of the pins and truss. Once I was done designing and calculating, I modeled everything on a CAD program and compared the values given by the program to the ones I calculated.

Here is a photo of the given forces and geometric constraints

<img width="393" height="217" alt="image" src="https://github.com/user-attachments/assets/9b04e24a-c683-41a7-8daf-a00782f3397e" />

Where a = .4m, b = .3m , Point A is a pin, Point B is a roller, and force P = 27.1 KN

## Analyze
Here is the truss I sketched.

<img width="317" height="175" alt="image" src="https://github.com/user-attachments/assets/92a2b63c-383e-4f16-bb6f-5994da15d698" />

I created a new pin in between B and A for extra support. 
Because E is right in the center we can find its length in relation to a.

<img width="97" height="37" alt="image" src="https://github.com/user-attachments/assets/90de84da-741a-4003-9f3b-741f1111c95d" />

Before I can analyze each joint individually we need to solve for the unknowns of the whole structure. I need to find Ay, Ax, and B. A has both a Ay and Ax component because it is a pin, while B only has one reaction because it is a roller. 

<img width="438" height="335" alt="image" src="https://github.com/user-attachments/assets/c1a3c9dc-8534-4a5f-b592-765a75ca307a" />

We also know the structure is in equilibrium so therefore:

<img width="232" height="52" alt="image" src="https://github.com/user-attachments/assets/f287a984-fcb1-4b85-9fac-69331217eecc" />

Using the equations of equilibrium and the free body diagram I created and solved these equations for Ay, Ax, and B.

<img width="443" height="527" alt="image" src="https://github.com/user-attachments/assets/a4eeec04-656f-4137-aeab-4433b636b89d" />

Next I sketched a free body diagram for every joint in the truss, solving for each internal force.

The first joint I choose to analyze was joint B. Joint B had two unknown forced I needed to solve for which means I only needed two equations.

<img width="437" height="547" alt="image" src="https://github.com/user-attachments/assets/aaca92ca-5b52-4a66-bea8-bd5487d88aba" />

The next joint I analyzed was joint C, because we had already found the force BC in the pervious free body diagram.

<img width="435" height="522" alt="image" src="https://github.com/user-attachments/assets/5641847d-fa4a-4374-b7e2-392ef25e62a4" />

I know CE is in compression rather than tension because of the negative answer. The free body diagram has CE drawn as a tension force so in this case the negative just means that force is in the opposite direction. 

<img width="398" height="177" alt="image" src="https://github.com/user-attachments/assets/f60a07aa-0b4e-4970-8ca8-ecef7396156a" />

<img width="437" height="537" alt="image" src="https://github.com/user-attachments/assets/4b2e0bda-392b-444a-ac81-c8ebc924eb00" />

<img width="452" height="442" alt="image" src="https://github.com/user-attachments/assets/aa57e312-63b1-4975-8f68-84f1a31946a6" />

<img width="442" height="262" alt="image" src="https://github.com/user-attachments/assets/c20e8c47-dd89-4512-961d-e1ae598c9d00" />


Next step was to find the required crosssectional area using a safety factory of 3.5. For this step I needed to use the largest internal force because the largest force will cause stress first. This is beacuse Stress = Force/Area

The yield strength for A500 steel was force this source: https://www.beamdimensions.com/materials/Steel/ASTM/ASTM_A500/

<img width="358" height="500" alt="image" src="https://github.com/user-attachments/assets/83053597-04af-4f43-9696-4edbb7ed9d16" />

The next step was to find the approximate weight of the truss. To do this I used the crosssectional area and multipled it by the length of the intire structure to get the volume. Then I used the density of A500 steel to find the mass of the structure. The density value was found on the same beamdimesnsions.com website as the yield strength. After that All I had to do was multiple the mass by gravity.

<img width="475" height="302" alt="image" src="https://github.com/user-attachments/assets/cc51beea-933e-466f-af30-0b97e224a8a4" />
<img width="627" height="326" alt="image" src="https://github.com/user-attachments/assets/c14f4f1b-65e1-45b1-ac08-5524498dd275" />


I then needed to find the minimum area of the pin using shear strain.
<img width="568" height="420" alt="image" src="https://github.com/user-attachments/assets/3b0f83a5-77e8-48d7-86d2-e3fb83df38f9" />
<img width="572" height="207" alt="image" src="https://github.com/user-attachments/assets/b4e54a35-8194-4d83-9dbd-42da4dd66aff" />




## Decide
The design for the truss was decided for stability. I made sure there was the right number of joints per member. This allows for the truss to be ridge, but still lets us solve for the all the interal forces or be statically determinate. The triangle shapes help keep the truss ridge too

https://engineeringstatics.org/Chapter_06-trusses.html

<img width="490" height="106" alt="image" src="https://github.com/user-attachments/assets/4524a375-fa92-4f0e-857b-b256f5041e5e" />


## Communicate
### Engineering lesson
I learned how to make a stable truss using triangulation and how give it the right ratio of joints and members 

### Failure Modes in Truss Comopnents
Likelihood of failure Modes in Truss Components

Truss Members
The expected 

