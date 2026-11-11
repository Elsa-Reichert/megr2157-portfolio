# A10 – Lead Screw Translating System

## Objective
#### Elsa's section
The goal for this weeks assignment is to design a lead screw system for a Tensile Tester as a group. I will be designing the crosshead, modeling the crosshead in CAD, Then creating a assembly in CAD.

## Analyze
#### Elsa's Section
##### Designing the Crosshead
I need to design the crosshead by analyzing the minimium strength required for the load, the maximium deflection, and nut flange diameter.

I decided to use aluminium 6061 for the material of the Crosshead because I saw some example crossheads made from the same material and the crosshead needs a bigger crosssection to hold the nut flanges, so the yeild strength doesn't need to be as high. 

The Yield strength of aluminum 6061 is equal to 34,809-39,885. Source:https://guxiangjs.com/yield-strength-stress-chart/. I will use the smaller end of this range to be safe. 

Young's Modulus (E) of aluminum is equal to 10.0 e+3 Ksi. Source:https://mechcodex.com/materials/6061-t6-aluminum

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

File: 

Once that was created, I downloaded CAD models for the leadscrew, nut flange and t slotted framing rails. All these files are from mcmaster.com

I created the assembly of the frame first:

<img width="1475" height="929" alt="image" src="https://github.com/user-attachments/assets/55f20ed1-448a-4ff1-b9c4-9fb4c7edf866" />

File

Then I created a new assembly using the frame assmebly, crosshead, lead screw, and flange nut. 

<img width="1341" height="931" alt="image" src="https://github.com/user-attachments/assets/692babdc-0260-468f-999d-6b4a18b02c7f" />

File: 

## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate

