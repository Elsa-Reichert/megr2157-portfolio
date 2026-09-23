# A5 – [Topic]

## Objective
My project is to design a bracket using the concept design below to hold a horizontial force applied symmetrically by a strap outline in figure 1. I will ned to use funfamental strength of materials analysis 

The dimensinos of T is part of the fit:
  a - intention for use where accuracy is not essential
  b - is about the cloest fits that can be expected to run freely
  c - is where accurate location and minimium play is desired

The design have a safety factor of 4

The applied load F is between 500lb - 800lb

I need to choose between aluminium 6061 T6, steel (ASTM A36), or Titanium (Ti-6Al-V4). I am going to use aluminium 6061 T6 whitch has a yield strenght of 240- 280 MPa and a shear strenght of 186 -217 MPa. [source](https://www.modulusmetal.com/aluminum-6061-t6-mechanical-properties/)

<img width="798" height="727" alt="image" src="https://github.com/user-attachments/assets/8495fac4-51e7-43fc-96c1-35799ef7f015" />

<img width="580" height="307" alt="image" src="https://github.com/user-attachments/assets/458dd644-bec2-4a84-a60d-927ee412084c" />



## Analyze
### Calculating Dimensions from Stress Analysis 
I need to analyis each dimensino and feature for stress analysis. I need to start with feature A. This is were the given force is, whcih lets us use shear stress to find the necesary cross sectin

I am using the reacton forces from one dimension(s) as an applied load for the next dimension. There will be 5 diffreent analyses

#### Figure A
There is a polyester strap applying a symetric horizontal force along this feature. We can treat this as a distrubuted load with total load, W, equal to 2F. We can also treat this feature as a cantilever beam because it is fixed to a feature at one end and has a force applied to it. 

Knowns: F = 500 - 800lb, SF = 4, W = 2F,
Unknowns: Cross sectinoal area, length
Assumptions: We can treat figure A as a cantilever beam, no failure due to dircet shear stress
  
<img width="493" height="122" alt="image" src="https://github.com/user-attachments/assets/4c5080e4-5578-49cc-bf3e-469d5adbdc10" />
I am using the max. stress formula from the Mechinery handbook ed. 29

<img width="493" height="38" alt="image" src="https://github.com/user-attachments/assets/8373b18e-54e4-4d16-a37d-22f5e6823aae" />
Definition of Z provided from the mechinery handbook ed. 29. The distnace from the nutural axis to the end is just the radius. 

[work]
Using the stress equation I was able to find the minimium area in terms of L. I will need to use bending analyis to find another equation to relate r and L.

#### Figure B
Knowns: F = 500 - 800lb, SF = 4, w = 2r
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, figure b can be treated as a axial loaded bar

Figure B has a reaction force caused by figure A going in the opposite direct at the end where both figures are connected. Because the forced cancel out, there will be an equal but opposite force in the other direct. This is what lets me treat it as an axial loaded bar. 

I solved for the reaction force at that end by solving for the moment about the other end. 
[work 2]

The width of the feature needs to be the same as feature A. This means w = 2r. 

Solving for t 
[work 2]

#### Figure C
Knowns: F = 500 - 800lb, SF = 4, Lc = 2a + b
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, figure c can be treated as a simply supported beam with a concentrated load at the center

I can treat it as a simply supported beam because it is supported at the end of the feature. There are also no forces acting in the x direction. The feature is concentric with feature B which is why F is at that center. 

Solving for the reation forces
[photo 3]

Using this equation from the merchery textbook for the shear stress
<img width="526" height="193" alt="image" src="https://github.com/user-attachments/assets/0c977eae-bcbb-47c4-91f2-c719407ce954" />

I can solve for the width. We do not have enough infromation to find the thickness with just this equation, but the thickness of feature C, D, and E are the same. 
[photo 3]

#### Figure D
Knowns: F = 500 - 800lb, SF = 4
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, Feature D can be treated as a axial loaded bar

Solving for D
[photo 4]

#### feature E
Knowns: F = 500 - 800lb, SF = 4, W = b = .9992 in
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, Feature E can be treated as a axial loaded bar

<img width="436" height="122" alt="image" src="https://github.com/user-attachments/assets/29514e0e-4de9-4261-859f-af842c1360c2" />
feature E is right above the b measurement given to us. 

I can solve for t.
[photo E]

## Decide


## Communicate

