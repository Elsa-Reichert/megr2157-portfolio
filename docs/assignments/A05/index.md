# A5 – Bracket Design

## Objective
My project is to design a bracket using the concept design below to hold a horizontial force applied symmetrically by a strap outline in figure 1. I will ned to use funfamental strength of materials analysis 

The design have a safety factor of 4

The applied load F is between 500lb - 800lb

I need to choose between aluminium 6061 T6, steel (ASTM A36), or Titanium (Ti-6Al-V4). 

Aluminium 6061 = Yield Strength = 35 ksi
ASTM A36: Yield Strength = 36 ksi
Titanium: Yield Strength = 128 ksi
[Source](https://en.wikipedia.org/wiki/Ti-6Al-4V)

I will use Ti-6Al-4V for my bracket because of the high yield strenth. The shear strenth is 110 ksi and E = 16500 ksi. [Source](https://www.aerospacemetals.com/wp-content/uploads/2023/07/Titanium-Ti-6Al-4V-Grade-5-STA-Data-Sheet.pdf)

<img width="798" height="727" alt="image" src="https://github.com/user-attachments/assets/8495fac4-51e7-43fc-96c1-35799ef7f015" />

<img width="580" height="307" alt="image" src="https://github.com/user-attachments/assets/458dd644-bec2-4a84-a60d-927ee412084c" />


## Analyze
### Calculating Dimensions from Stress Analysis 
I need to analyis each dimension and feature for stress analysis. I need to start with feature A. This is were the given force is, whcih lets us use shear stress to find the necesary cross secton.

I am using the reacton forces from one dimension(s) as an applied load for the next dimension. There will be 5 diffreent analyses

#### Figure A
There is a polyester strap applying a symetric horizontal force along this feature. We can treat this as a distrubuted load with total load, W, equal to 2F. We can also treat this feature as a cantilever beam because it is fixed to a feature at one end and has a force applied to it. 

Knowns: F = 500 - 800lb, SF = 4, W = 2F, Yield Strength = 128 ksi 
Unknowns: Cross sectinoal area, length
Assumptions: We can treat figure A as a cantilever beam, no failure due to dircet shear stress
  
<img width="493" height="122" alt="image" src="https://github.com/user-attachments/assets/4c5080e4-5578-49cc-bf3e-469d5adbdc10" />

I am using the max. stress formula from the Mechinery handbook ed. 29

<img width="493" height="38" alt="image" src="https://github.com/user-attachments/assets/8373b18e-54e4-4d16-a37d-22f5e6823aae" />

Definition of Z provided from the mechinery handbook ed. 29. The distnace from the nutural axis to the end is just the radius. 


<img width="442" height="542" alt="image" src="https://github.com/user-attachments/assets/4272f8c8-56f6-4da4-924b-bce08be1dde1" />

Using the stress equation I was able to find the minimium area in terms of L. I will need to use bending analyis to find another equation to relate r and L.

#### Figure B
Knowns: F = 500 - 800lb, SF = 4, w = 2r, Yield Strength = 128 ksi
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, figure b can be treated as a axial loaded bar

Figure B has a reaction force caused by figure A going in the opposite direct at the end where both figures are connected. Because the forced cancel out, there will be an equal but opposite force in the other direct. This is what lets me treat it as an axial loaded bar. 

I solved for the reaction force at that end by solving for the moment about the other end. 

<img width="261" height="93" alt="image" src="https://github.com/user-attachments/assets/b1b90daf-0567-42b9-8c29-886304d602bb" />


The width of the feature needs to be the same as feature A. This means w = 2r. 

Solving for t 

<img width="382" height="407" alt="image" src="https://github.com/user-attachments/assets/519b186c-3b9c-4254-918a-7c4b8dcfcc4b" />

#### Figure C
Knowns: F = 500 - 800lb, SF = 4, Lc = 2a + b, Yield Strength = 128 ksi
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, figure c can be treated as a simply supported beam with a concentrated load at the center

I can treat it as a simply supported beam because it is supported at the end of the feature. There are also no forces acting in the x direction. The feature is concentric with feature B which is why F is at that center. 

Using this equation from the merchery textbook for the shear stress
<img width="526" height="193" alt="image" src="https://github.com/user-attachments/assets/0c977eae-bcbb-47c4-91f2-c719407ce954" />

I can solve for the width. We do not have enough infromation to find the thickness with just this equation, but the thickness of feature C, D, and E are the same. 

<img width="367" height="432" alt="image" src="https://github.com/user-attachments/assets/8c17d5c5-f25e-400c-899f-5386953c4a95" />


#### Figure D
Knowns: F = 500 - 800lb, SF = 4, Yield Strength = 128 ksi
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, Feature D can be treated as a axial loaded bar

Solving for D

<img width="373" height="522" alt="image" src="https://github.com/user-attachments/assets/324612b1-96d9-4847-9c4d-031371f67c74" />


#### feature E
Knowns: F = 500 - 800lb, SF = 4, W = b = .9992 in, Yield Strength = 128 ksi
Unknowns: Cross sectional area and total length
Assumptions: No failure due to direct shear stress, Feature E can be treated as a axial loaded bar

<img width="436" height="122" alt="image" src="https://github.com/user-attachments/assets/29514e0e-4de9-4261-859f-af842c1360c2" />
feature E is right above the b measurement given to us. 

I can solve for t.

<img width="397" height="430" alt="image" src="https://github.com/user-attachments/assets/9c8a7526-ad3d-4570-96da-94fc8e09247f" />


#### Plugging in values
For freatures C, D ,E I need to find the width of feature E first. Then I can plug that into the equations for C and D. Using F = 800lb and converting ksi to psi.

<img width="386" height="445" alt="image" src="https://github.com/user-attachments/assets/c91d0f90-2d0d-4053-8673-70efd60c3d44" />


### Stiffness Analysis
Now I need to conduct stiffness analysis on the same 5 features. Each has a given deflection of .004 in and shear deflections are negligible. 

#### Feature 1 
Knowns: F = 500 - 800lb, SF = 4, W = 2F, Yield Strength = 128 ksi 
Unknowns: Cross sectional area, length, Radius
Assumptions: Shear deflections are negligible

using this equation for max. dflection we can solve for L
<img width="838" height="192" alt="image" src="https://github.com/user-attachments/assets/7a3363e2-8538-45cb-b66f-85c1aa6b9327" />

<img width="402" height="507" alt="image" src="https://github.com/user-attachments/assets/5e05bb79-3384-4cae-bc15-7b4c4ff74eb6" />


#### Feature 2
Knowns: F = 500 - 800lb, SF = 4, W = 2F, Yield Strength = 128 ksi 
Unknowns: Cross sectional area, length, Radius
Assumptions: Shear deflections are negligible

<img width="386" height="477" alt="image" src="https://github.com/user-attachments/assets/7218df4c-83f5-4d70-901a-d404834ebe34" />


#### Feature 3
Knowns: F = 500 - 800lb, SF = 4, Yield Strength = 128 ksi 
Unknowns: Cross sectional area, length, Radius
Assumptions: Shear deflections are negligible
Using this equation from the mechninary handbook
<img width="802" height="157" alt="image" src="https://github.com/user-attachments/assets/0fd89c42-67b0-457d-9bb0-c863178f9b3f" />

<img width="386" height="493" alt="image" src="https://github.com/user-attachments/assets/b49ee72d-9f51-455f-b274-ae34029a52f2" />

Feature 3 has a given value, 2.4964in. The deflection equation gives us a minimum L value, which is under the given L value.

#### Feature D
Knowns: F = 500 - 800lb, SF = 4, Yield Strength = 128 ksi 
Unknowns: Cross sectional area, length, Radius
Assumptions: Shear deflections are negligible
<img width="362" height="312" alt="image" src="https://github.com/user-attachments/assets/03c560f9-0662-4728-9a8e-c06374d29241" />

#### Feature E
Knowns: F = 500 - 800lb, SF = 4, Yield Strength = 128 ksi 
Unknowns: Cross sectional area, length, Radius
Assumptions: Shear deflections are negligible
<img width="352" height="177" alt="image" src="https://github.com/user-attachments/assets/42138918-a2c4-47dc-9598-3ffb5e62c0ab" />

#### Plugging in numbers
<img width="396" height="512" alt="image" src="https://github.com/user-attachments/assets/73099424-9d57-4232-8e06-e693f83a0bef" />

<img width="337" height="428" alt="image" src="https://github.com/user-attachments/assets/04081020-99d4-4044-85fc-dcc6e6414522" />

### Multiview sketches

#### Stress analysis 
<img width="388" height="391" alt="image" src="https://github.com/user-attachments/assets/af858e17-4897-46d2-a99d-b3c82437b56b" />

#### Stiffness Analysis
<img width="366" height="397" alt="image" src="https://github.com/user-attachments/assets/70e33d99-3613-4ee5-af51-012b3fbae2d2" />




<img width="302" height="187" alt="image" src="https://github.com/user-attachments/assets/97e19a5d-7165-4b12-acbe-ccea78416e21" />
<img width="366" height="431" alt="image" src="https://github.com/user-attachments/assets/fb0d3e49-6ce0-4a00-9eac-728c9f104a9c" />


<img width="850" height="546" alt="Screenshot 2026-09-24 013318" src="https://github.com/user-attachments/assets/07d989e5-5216-4017-ad58-64424243c359" />

<img width="377" height="317" alt="image" src="https://github.com/user-attachments/assets/4a6578c2-12c7-436a-a636-50fbea5fc535" />

## Communicate
If my assumption about the material choice was wrong, it would change all of my found values because the yield stress and strain and based on that material. The material I choose to use had a very high strength, so I would probably need the whole struture bigger if the material changed to something less strong.
