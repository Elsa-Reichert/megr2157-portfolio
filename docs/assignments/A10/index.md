# A10 – Lead Screw Translating System

## Objective
#### Elsa's section
The goal for this weeks assignment is to design a lead screw system for a Tensile Tester as a group. I will be designing the crosshead, modeling the crosshead in CAD, Then creating a assembly in CAD.

## Analyze
#### Elsa's Section
##### Designing the Crosshead
I need to design the crosshead by analyzing the minimium strength required for the load, the maximium deflection, and nut flange diameter.

I decided to use aluminium 6061 for the material of the Crosshead because I saw some example crossheads made from the same material and the crosshead needs a bigger crosssection to hold the nut flanges, so the yeild strength doesn't need to be as high. 

The Yield strength of aluminum 6061 is equal to 34,809-39,885. (Source)[https://guxiangjs.com/yield-strength-stress-chart] I will use the smaller end of this range to be safe. 

Young's Modulus (E) of aluminum is equal to 10.0 e+3 Ksi. (Source)[https://mechcodex.com/materials/6061-t6-aluminum]

Givens: Yield Stength = 34,809, E = 10.0e+6 Psi, Diameter of the nut flange = 2.625 in, F =1000N =224.809lb, Safety Factor = 4, Max. deflection of the crosshead = .1mm = .003937 in

##### Stress/Strenth anaylsis

<img width="779" height="434" alt="image" src="https://github.com/user-attachments/assets/dc09373c-d536-473f-95bb-02aa989ca313" />

The minimium cross sectional area is a lot smaller than what I would need to accomident the nut flangues. 

##### Simple beam deflection analysis

I used simple beam deflection analysis to find the minimium height of the crosshead and make sure we are under the max. deflection.

<img width="1060" height="177" alt="Screenshot 2026-11-11 104603" src="https://github.com/user-attachments/assets/6ac6fc41-ea7a-4adb-8186-3c8be092e25b" />

<img width="910" height="399" alt="Screenshot 2026-11-11 110156" src="https://github.com/user-attachments/assets/f946dda8-fa8a-405b-af8a-f6f3ae1a3c85" />

I used these equations from the Machinery's Handbook 29th Edition to solve.

My solution

<img width="694" height="523" alt="Screenshot 2026-11-11 173332" src="https://github.com/user-attachments/assets/4fac4af2-260c-4974-8212-5d5811127c4d" />

##### Sketch of crosshead design

<img width="2513" height="1671" alt="IMG_8592" src="https://github.com/user-attachments/assets/afdc6dd0-b74c-490e-8034-3aabf4f56c7d" />

##### Parametric Modeling
First I needed to create a parametric model of the Crosshead. Everything else needed I can find files online. 

Variables:
<img width="962" height="417" alt="Screenshot 2026-11-11 121558" src="https://github.com/user-attachments/assets/32468c53-2c25-42d0-9026-1ce4e19df1be" />

I created the Top of the crosshead like this:

<img width="1085" height="645" alt="Screenshot 2026-11-11 122013" src="https://github.com/user-attachments/assets/1e5a5227-7112-4d79-8783-4e11ff196b3a" />

Then used a boss extrude and changed the material to aluminum 6061 to get the final piece: 

<img width="1201" height="644" alt="Screenshot 2026-11-11 122050" src="https://github.com/user-attachments/assets/6a844aea-d3c7-4e91-8def-90701923b074" />

File: https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Crosshead.SLDPRT 

Once that was created, I downloaded CAD models for the leadscrew, nut flange and t slotted framing rails. All these files are from mcmaster.com

I created the assembly of the frame first:

<img width="1475" height="929" alt="image" src="https://github.com/user-attachments/assets/55f20ed1-448a-4ff1-b9c4-9fb4c7edf866" />

(File)[https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Frame.SLDASM]

Then I created a new assembly using the frame assmebly, crosshead, lead screw, and flange nut. 

<img width="1341" height="931" alt="image" src="https://github.com/user-attachments/assets/692babdc-0260-468f-999d-6b4a18b02c7f" />

(File)[https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Assem2.SLDASM]

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
(File for new peice)[https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Crosshead%20new.SLDPRT] 
New results:
<img width="721" height="451" alt="image" src="https://github.com/user-attachments/assets/754e7235-7740-4fff-8e69-5560638f54ca" />

<img width="625" height="426" alt="image" src="https://github.com/user-attachments/assets/e65354a6-86fc-4dd1-9330-def86154578c" />

<img width="646" height="443" alt="image" src="https://github.com/user-attachments/assets/ab002b82-d5ee-4767-bb41-c6d7986c6f0b" />

According to solidworks the mass of the new design is 4.33lbs. The old design is 3.46lbs. The max. stress went from 2.081e+3 psi down to 1.518e+03. The location of the max. stress is still at the same location, but it is not as high. The max. deflection went from  9.751e-4 in to 4.690e-4 in. That is almost half. The high deflection area is still towoard the edge of the center but less of it is at the maximium. The strain went from 1.254e-4 to 9.388e-05, still around the hole.

##### Drawing of crosshead

<img width="1394" height="914" alt="Crosshead" src="https://github.com/user-attachments/assets/b5875902-ae3e-43a3-9e1c-484048ef33d2" />

[File of Drawing](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A10/Crosshead.SLDDRW)

## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate
#### Elsa's Section
Engineering lesson: I learned how to design a crosshead using contraints and already determined pieces. This was also our first group project in this class and it tought me how to cordinate with another person to get work done in an efficent way. I also got more practice with making assemblies in Solidworks.
