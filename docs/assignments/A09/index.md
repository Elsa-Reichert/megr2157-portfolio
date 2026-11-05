# A9 – Pulleys

## Objective
The goal for this weeks assignment is to design a pully system using friction, static analysis and dynamic analysis.

The pully system needs to transfer power between two parallel axes seprated by a center distance of 4-6 inches following these requirements:
  
    -pully diameter: 3 inches on both
    -roational speed: Between 1000-2000RPM
    -Belt Tension(static): Between 4-6 lbf 
    -Materials: aluminium, ABS, or Steel. 
    -May include a grove and shaft diameter of my choosing
    -Safety factor: minimum of 3

The belt is assumed to be made of polyurethane rubber, with a yeild strength of 3.25 MPA (471Psi) at 20% strain.

<img width="602" height="213" alt="image" src="https://github.com/user-attachments/assets/e19d6f9a-abaf-4d09-9f9d-e35deaf6df62" />

## Analyze
I will use Steel for the material. Steel alloy has a yield stregth of 89,984.6 Psi according to solidworks. 

I am going to use 1500RPM for the rotational speed, 5 in for the distance between centers, and 5lbf for the belt tension. These values are right in the center of the range given. 

The coffience of kenetic friction between rubber and steel is 0.70 according to: https://ficientdesign.com/friction-coefficient-lookup/ 

### Part one
For the first step I need to:  

    -Calculate the forces on both the tight and loose side with no slippage
    -Calculate the diameter of the belt using the normal stress equation and yield strenth.
    -Calculate the belt's outer circumference then select a suitable belt from: https://www.mcmaster.com/products/round-belts/

#### Knowns
    -Pully diameter = 3 in
    -Rotational Speed = 1500RPM
    -Belt Tension (static) = 5 lbf
    -Material of pully: Alloy Steel
    -Yield strength of pully = 89,984.6 Psi
    -Safety factor = 3
    -Belt material: Polyurethance rubber
    -Belt yield strength = 3.25Mpa/471 Psi at 20% strain. 
    -Coeffcient of kenetic friction = 0.70
    -Distance betweeen centers = 5in

#### Unknowns
    -Cross sectinoal area
    -Forces on both sides
    -Diameter of the belt
    -Belts outer circumference

<img width="580" height="462" alt="image" src="https://github.com/user-attachments/assets/6df3628a-b426-4038-879b-c0337f55c811" />

<img width="3024" height="4032" alt="IMG_8536" src="https://github.com/user-attachments/assets/14e3603c-7667-4a57-bc00-f6866961d092" />

<img width="2845" height="3530" alt="IMG_8537" src="https://github.com/user-attachments/assets/fb5a8198-ca21-42f9-8e16-e2c05d88feb0" />


#### Find a belt
5/16 in is the best option for a diameter. The calculated diameter, .270 in, is a minimium. 5/16 is the cloest to that value without going under. The only problem is they do not make a 5/16 diameter belt with a close circumference value. The next best option is 3/8. The website offers a 19 1/4 and a 19 1/2 in circumference. I will pick the 19 1/4 circumference because it needs to hold tension, so its better to round down a litte.

Link to the belt:
https://www.mcmaster.com/3044K608-1835T905/

### Part 2
I need to determine the minimum diameter of the shaft by calculating minimium area when torque it applied to a shaft with 1060 Harderned steel.

The yield strength of 1060 hardend steel is about 53.7ksi. Source: https://www.fabdigit.com/materials/steel-1060/

#### Knowns
    -Pully diameter = 3 in
    -Rotational Speed = 1500RPM
    -Belt Tension (static) = 5 lbf
    -Safety factor = 3
    -Material of the shaft = 1060 Hardened steel
    -Yield strength = 53.7 Ksi = 53,700 psi

#### Unknowns
    -Torque 
    -minimum diameter

<img width="2439" height="2960" alt="IMG_8538" src="https://github.com/user-attachments/assets/414030fe-5f56-4ae5-b874-e6b3ced457f9" />

### Part 3
Next step is to design the journal bearing out of sintered or non metallic using Table 4 on pg 2440 in the Machinery's Handbook. I need to determind the pressure, linear velocity, PV rating, then find a suitable material.

The belt choisen was 8/16 in, which means the thickness of the journal bearing has to be slightly bigger than that value. I will just round that value up to 1 in and use that for the width of the journal bearing. 

We also know the load from the pully system will transfer to the journal bearing. For earlier we know it is 10 lbs.
#### knowns
    -Load = 10 lbs
    -Roational Speed = 1500RPM

#### Unknowns
    -Linear velocity
    -PV rating
    -Material for journal bearing
  
<img width="2439" height="2960" alt="IMG_8538" src="https://github.com/user-attachments/assets/14205773-6312-4f04-8f1f-cef5896d48d2" />

<img width="532" height="351" alt="image" src="https://github.com/user-attachments/assets/6048684b-dbc0-4660-97db-0f2dcb878680" />    

This is from the Mechinary's Handbook. All the matierals can support the load capacities. I will choose acetal for the bearing material because I do not need to suportant any higher loads or speeds.

#### Part four

Part four is to use engineering analysis to design a frame whcih supports the pulley system.

I decided to create a frame simular to this. The belt needed to be at a 180degrees and the tension could not be affected because my calculations were based off of that. This means only the weight of the pully system will affect the frame

<img width="750" height="374" alt="image" src="https://github.com/user-attachments/assets/2a8fc208-2c06-4f67-b727-54e1db8f4350" />

Source: https://lyhsteel.com/steel-calculators/metal-density-chart/

Shear strength of steel alloy is about 42 psi. 
Source: https://www.engineersedge.com/materials/material_tensile_shear_and_yield_strength_15798.htm 

<img width="2333" height="3142" alt="IMG_8540" src="https://github.com/user-attachments/assets/359133a0-e950-4703-ba9d-a8a0c147f0ea" />

My first thought was to use the weight of the pullys pulling down on the frame. I only used the weight from the alloy steel because everything else would be negliable because of the size and material. The weight ended up being less than the shear stress caused by the tension in the system. So I used the shear force to calculate the minimum cross sectino.

<img width="472" height="242" alt="image" src="https://github.com/user-attachments/assets/a086f3f0-ce44-4eca-8207-a1858f084801" />

I ended up using a bigger area so it would have space to hold both pullys.

## Communicate
### Engineering lessons learned
I learned how to design a pully system, how the angles and friction effect the tension forces in the pully, use these values I found to design a journal bearing and shaft, then to finally design a frame for the system.
