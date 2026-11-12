# A10 – Lead Screw Translating System

## Objective
#### Maxwell's section
Me and a group member named Elsa from 2157 decided to pair up and split this group assignment. We both agreed that I would handle the necessary calculations surrounding the Leadscrews and the Nut/Flanges as well as the current estimated total of the parts and mechanisms while Elsa would handle the Crosshead and the CAD model as she preferred to use SolidWorks, which was compatible with the downloads unlike my preferred choice of Creo which isn't as compatible with McMaster downloads.

<img width="231" height="261" alt="image" src="https://github.com/user-attachments/assets/67f3735b-7259-4187-ab68-5c44c3a37eca" />

This was the basic summarization of part of my work involving finding the diameter of a selected Leadscrew and selecting a Nut/Flange to support the 2KN load the mechanism is designed for, as shown below in the figure.

<img width="444" height="768" alt="Screenshot 2026-11-11 123137" src="https://github.com/user-attachments/assets/ed4467b9-cdb9-4e41-bdd1-08b3d6b6bfed" />

#### Elsa's section
The goal for this weeks assignment is to design a lead screw system for a tensile tester as a group. I will be designing the crosshead, modeling the crosshead in CAD, Then creating an assembly in CAD.

## Analyze
#### Maxwell's section
Below are the calculations I did for my side of the assignment.

First, the diameter of the Leadscrews:

<img width="384" height="412" alt="IMG_2969" src="https://github.com/user-attachments/assets/05452980-0a3f-4df0-96c9-9a42039aa611" />

Then the Nut/Flange:

<img width="384" height="412" alt="IMG_2968" src="https://github.com/user-attachments/assets/90d9f8f3-58c3-47f5-9754-dbcef8a13837" />

#### Elsa's Section
##### Designing the Crosshead
I need to design the crosshead by analyzing the minimium strength required for the load, the maximium deflection, and nut flange diameter.

I decided to use aluminum 6061 for the material of the Crosshead because I saw some example crossheads made from the same material and the crosshead needs a bigger cross section to hold the nut flanges, so the yield strength doesn't need to be as high. 

The Yield strength of aluminum 6061 is equal to 34,809-39,885psi. [Source](https://guxiangjs.com/yield-strength-stress-chart). I will use the smaller end of this range to be safe. 

Young's Modulus (E) of aluminum is equal to 10.0 e+3 Ksi. [Source](https://mechcodex.com/materials/6061-t6-aluminum)

Givens: Yield Stength = 34,809, E = 10.0e+6 Psi, Diameter of the nut flange = 2.625 in, F =1000N =224.809lb, Safety Factor = 4, Max. deflection of the crosshead = .1mm = .003937 in

##### Stress/Strenth anaylsis

<img width="779" height="434" alt="image" src="https://github.com/user-attachments/assets/dc09373c-d536-473f-95bb-02aa989ca313" />

The minimium cross sectional area is a lot smaller than what I would need to accommodate the nut flanges. 

##### Simple beam deflection analysis

I used simple beam deflection analysis to find the minimium height of the crosshead and make sure we are under the max. deflection.

<img width="1060" height="177" alt="Screenshot 2026-11-11 104603" src="https://github.com/user-attachments/assets/6ac6fc41-ea7a-4adb-8186-3c8be092e25b" />

<img width="910" height="399" alt="Screenshot 2026-11-11 110156" src="https://github.com/user-attachments/assets/f946dda8-fa8a-405b-af8a-f6f3ae1a3c85" />

I used these equations from the Machinery's Handbook 29th Edition to solve.

My solution:

<img width="694" height="523" alt="Screenshot 2026-11-11 173332" src="https://github.com/user-attachments/assets/4fac4af2-260c-4974-8212-5d5811127c4d" />

##### Sketch of crosshead design

<img width="2513" height="1671" alt="IMG_8592" src="https://github.com/user-attachments/assets/afdc6dd0-b74c-490e-8034-3aabf4f56c7d" />

##### Parametric Modeling
First I needed to create a parametric model of the Crosshead. Everything else needed I can find CAD files online. 

Variables:
<img width="962" height="417" alt="Screenshot 2026-11-11 121558" src="https://github.com/user-attachments/assets/32468c53-2c25-42d0-9026-1ce4e19df1be" />

I created the top of the crosshead like this:

<img width="1085" height="645" alt="Screenshot 2026-11-11 122013" src="https://github.com/user-attachments/assets/1e5a5227-7112-4d79-8783-4e11ff196b3a" />

Then used a boss extrude and changed the material to aluminum 6061 to get the final piece: 

<img width="1201" height="644" alt="Screenshot 2026-11-11 122050" src="https://github.com/user-attachments/assets/6a844aea-d3c7-4e91-8def-90701923b074" />

[File](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Crosshead.SLDPRT)

Once that was created, I downloaded CAD models for the leadscrew, nut flange and t slotted framing rails. All these files are from mcmaster.com

I created the assembly of the frame first:

<img width="1475" height="929" alt="image" src="https://github.com/user-attachments/assets/55f20ed1-448a-4ff1-b9c4-9fb4c7edf866" />

[File](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Frame.SLDASM)

Then I created a new assembly using the frame assmebly, crosshead, lead screw, and flange nut. 

<img width="1341" height="931" alt="image" src="https://github.com/user-attachments/assets/692babdc-0260-468f-999d-6b4a18b02c7f" />

[File](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Assem2.SLDASM)

##### Finite Element analysis

I need to use Fininte Element Analysis on the crosshead to evalue stiffness and strength under a 2kN axial test load

I put two roller/sliders where the lead screw goes:

<img width="1587" height="566" alt="image" src="https://github.com/user-attachments/assets/7e13773c-cb28-412c-946d-5eca14f38ade" />

Then added a 449.6178lb force in the opposite direction:

<img width="1315" height="573" alt="image" src="https://github.com/user-attachments/assets/6eb28447-46a7-45ec-846b-95950210453d" />

First using a coarse mesh: 

<img width="906" height="619" alt="image" src="https://github.com/user-attachments/assets/d105de23-e56e-4510-931e-0675bbb2b2dc" />

Running the simulation with the roller/slider supports gave me an error that the deflection/stress was to high. I looked back at the fixture types and noticed a fixed hinge one. This is a lot closer to what is happening with the leadscrew. 

New fixture:
<img width="1545" height="704" alt="image" src="https://github.com/user-attachments/assets/d6aede68-cf67-497a-9815-884f814b7cf6" />

Results:
<img width="1322" height="565" alt="image" src="https://github.com/user-attachments/assets/b5576d91-6e77-4a77-b4f7-e011f592d2e4" />

<img width="1024" height="566" alt="image" src="https://github.com/user-attachments/assets/2c34d156-5eff-472f-a339-74f0d216c162" />

<img width="1018" height="548" alt="image" src="https://github.com/user-attachments/assets/376cee6f-3e0a-4c9a-b4c6-364672163af6" />

I need to check for convergence.

Running with a midium sized mesh:

<img width="1522" height="607" alt="image" src="https://github.com/user-attachments/assets/817b9282-56ea-4f60-9f89-d0089bd20680" />

<img width="1023" height="574" alt="image" src="https://github.com/user-attachments/assets/9d385509-5926-42bc-870b-0ae627e18db1" />

<img width="493" height="538" alt="image" src="https://github.com/user-attachments/assets/4e8e21d6-b7eb-4ea7-8829-e4acdcc18d8e" />

<img width="522" height="489" alt="image" src="https://github.com/user-attachments/assets/350d2038-ac76-4eaa-9139-dec2bfd9bcf0" />

Calculating the convergence using this equation:

<img width="209" height="108" alt="image" src="https://github.com/user-attachments/assets/ca3f9f10-9136-4e86-81fb-8939627e8d55" />

They do converge:

<img width="762" height="292" alt="image" src="https://github.com/user-attachments/assets/f51dbee1-03cc-44c5-b93b-47962f6ff9f3" />


Results:

  -Max. von Mises stress and location: The max. stress is 2.081e+03 on the side of the hole closest to the middle.
  
  -Max. vertical deflection: The max. deflection is 9.851e-04 in and it is toward the middle edges of the crosshead.
  
  -Factory of safety: 19
  
  -Load path or twisting/warping tendencies: The deflection is more at the side toward the middle of the crosshead which could cause some warping. The load path is at the middle.

To try and improve the stresses around that those ends of the holes and deflection toward the middle I am going to add a thicker layer of aluminium over part of the peice:

<img width="418" height="300" alt="image" src="https://github.com/user-attachments/assets/a103b02f-372b-4b7e-b03f-17bf845255af" />

<img width="735" height="511" alt="image" src="https://github.com/user-attachments/assets/9522cf35-6f25-471c-aab2-e7a507b93c39" />

I forgot to make space for the hole so I went back to the sketch, did a convert entites on the holes, then trimed entities:

<img width="440" height="301" alt="image" src="https://github.com/user-attachments/assets/6c6f91af-ae46-49ce-8515-bb39e5bcd564" />

Final peice:

<img width="357" height="208" alt="image" src="https://github.com/user-attachments/assets/4e8526c8-7ee0-4e3d-9928-d96b273fcf08" />

[File for new peice](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Crosshead%20new.SLDPRT)

New results:

<img width="721" height="451" alt="image" src="https://github.com/user-attachments/assets/754e7235-7740-4fff-8e69-5560638f54ca" />

<img width="625" height="426" alt="image" src="https://github.com/user-attachments/assets/e65354a6-86fc-4dd1-9330-def86154578c" />

<img width="646" height="443" alt="image" src="https://github.com/user-attachments/assets/ab002b82-d5ee-4767-bb41-c6d7986c6f0b" />

According to solidworks the mass of the new design is 4.33lbs. The old design is 3.46lbs. The max. stress went from 2.081e+3 psi down to 1.518e+03. The location of the max. stress is still at the same location, but it is not as high. The max. deflection went from  9.751e-4 in to 4.690e-4 in. That is almost half. The high deflection area is still towoard the edge of the center but less of it is at the maximium. The strain went from 1.254e-4 to 9.388e-05, still around the hole.

##### Drawing of crosshead

<img width="1394" height="914" alt="Crosshead" src="https://github.com/user-attachments/assets/b5875902-ae3e-43a3-9e1c-484048ef33d2" />

[File of Drawing](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Crosshead.SLDDRW)

## Decide
#### Maxwell's section
The final selected Leadscrews and Nut/Flanges were found using these two websites given by the professor along with their total value and data:

Leadscrew(s): Zinc-Plated Carbon Steel ACME Leadscrew. Amount: 2. Total: $35.49 X 2 = $70.98 before taxes. Serial Number: 93255A463

<img width="728" height="370" alt="image" src="https://github.com/user-attachments/assets/01f897fa-e156-4200-8f9e-1c9d37d7120c" />

Website: https://www.mcmaster.com/93255A463/

Nut/Flange(s): Precision ACME Flange Nut. Amount: 2. Total: $201.69 X 2 = $403.38 before taxes. Serial Number: 97790A130

<img width="733" height="373" alt="image" src="https://github.com/user-attachments/assets/c6dcbcce-69ed-430a-b26d-5bb69755f3c8" />

Website: https://www.mcmaster.com/97790A130/

Total Cost thus far: $474.36 for Leadscrews and Nut/Flanges
#### Elsa's section 
To create the frame I used 2 1ft T slotted framing rails and 2 1.5ft T-slotted framing rails. 
<img width="875" height="502" alt="image" src="https://github.com/user-attachments/assets/a8c3075d-88bd-42a0-b2b1-16c901da6ccf" />
[Link to the 1 link frame.](https://www.mcmaster.com/47065T103-47065T414/). The serial number is Serial number 47065T103.
[Link to the 1.5 inch frame.](https://www.mcmaster.com/47065T103-47065T576/) The serial number is Serial number 47065T103

The 1.5 inch frames cost $22.56 each and the 1 inch frames cost $17.15 each

We need 6061 aluminum for the cross head. I find those bars off the same website. The 1 ft option is $75.74
<img width="1172" height="506" alt="image" src="https://github.com/user-attachments/assets/9dd7281b-c7ee-412b-9352-07315148a2c2" />
[Link](https://www.mcmaster.com/8975K352-8975K351/) and the serial number is 8975K352.

Adding up my costs and Max's costs to get the total cost: 629.52 before tax.

## Communicate
#### Maxwell's section
Lessons Learned: I learned to collaborate with another student even despite the different learning styles and approaches towards an assignment. With good communication we were both able to get our parts done and on time and with that communication we were able to exchange the necessary info to one another to get our parts done on time and to the best of our abilities.

I would argue the biggest struggle/mistake for me in this assignment was initially getting the diameter of the Leadscrew wrong because I was using the wrong type of calculations and also was looking at the wrong website info entirely. The website on the assignment page did not lead to the "Leadscrew" tab, it led to the Nut/Flange tab and I was looking at the wrong set of data for the assignment until I realized the mistake 1 hour into the calculations and thus had to scrap my notes before attempting again. While I wish I remembered to take a picture of my faulty calculations, I had thrown them away out of frustration, but at least I remembered to mention them here in the lessons learned section.

Total Time: 3-4 hours
#### Elsa's Section
Engineering lesson: I learned how to design a crosshead using contraints and already determined pieces. This was also our first group project in this class and it tought me how to cordinate with another person to get work done in an efficent way. I also got more practice with making assemblies in Solidworks.
