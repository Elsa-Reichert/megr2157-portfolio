# A9 – Pulleys

## Objective
The goal for this weeks assignment is to design a pully system using frictino, static analysis and dynamic analysis.

I decided to use 5lbf for the belt tension and 1500RPM for the rotational speed because those values were right in the middle of the given range. 

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

The coffience of kentic friction between rubber and steel is 0.70 according to: https://ficientdesign.com/friction-coefficient-lookup/ 
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


## Decide


## Communicate

