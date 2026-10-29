# A8 – Gears

## Objective
The goal of this assignment is too:
  -Design a gearbox that can be assembled and disassembled.
  -Analyze and size input and output shafts for strength.
  -Design journal bearings to support shafts.
  -Create a gearbox housing with proper clearance and fastening.
  -Use parametric CAD modeling to generate a final design.
  -Document calculations, sketches, and lessons learned.

Spur Gears: Gear ratio = 24:9 
Output gear: torque = 1.25 in-lb, speed = 1100 rpm, shaft diameter = .25 in, length = 1 in, short shaft
input gear: shaft diameter = .125in, length 1 in, power transmission

Assumptions: 
  -assume approprate strenth of shaft given from Machinery's handbook: 4000 psi
  -Gear train is ideal
  -the moment of the radial force from the gear train can be ignored

Note:
  -The shafts are press fit through the hubs of the gears
  -make sure threre is enough clearance between gears and gearbox
  -use a running sliding fit for the size of the hole for the shafts
## Analyze

### Design of the shafts
Use the equations for stress to determine if the input and output shafts' diameters are sufficient

Force analysis equations from slideshow:
<img width="511" height="277" alt="image" src="https://github.com/user-attachments/assets/761dcae0-52a4-44e1-bf72-67c5292d7df8" />

#### Input Shaft diameter
Knowns: shaft diameter = .125 in, length = 1in, power transmission, Gear ratio = 24/9 , torque of the output gear is = 1.25 in-lb, speed from output gear = 1100 rpm, shear tield strengh = 4000 psi

Unknowns: torque, speed, power

First I need to find the torque of the input shaft using the gear ratio and torque of the output gear.I will use the equations below.

<img width="690" height="311" alt="image" src="https://github.com/user-attachments/assets/aad0e4f4-ce11-49ca-a4e1-6ddad2d8e8aa" />

Solving for the torque, speed, and power in the input shaft

<img width="1844" height="2480" alt="CamScanner 10-28-26 23 59-1" src="https://github.com/user-attachments/assets/5c761e52-3261-4e9d-a782-32adf9acff8d" />


Now we can plug in these numbers to the design shaft equation for the diameter in inches. The input gear is a main power transmiting shaft so I will use that equation.

<img width="1596" height="2064" alt="CamScanner 10-28-26 23 59-2" src="https://github.com/user-attachments/assets/d453dbea-b8b3-427d-9445-c7db9f70e384" />

The diameter found using the stress equations is smaller than the given diameter. Because it is based on stress, it is okay to be under.

#### output Shaft diameter
Knowns: Torque for the output shaft = 1.25in-lb, Gear ratio = 24:9, Speed of the output shaft = 1100 rpm, given shaft diameter of output shaft = .25 in, length = 1 in, and it is a short shaft

Unknowns: Power in the output shaft

First we need to calculate the power in the output shaft: 

<img width="382" height="206" alt="image" src="https://github.com/user-attachments/assets/01544bb9-0ba3-4ecf-bf6a-eb357f9e8f12" />


Now we can use the power found and rotational speed to find the diameter needed. This gear is a short shaft:

<img width="198" height="167" alt="image" src="https://github.com/user-attachments/assets/348ea572-1487-458f-829b-feceb24aaa4f" />


The calculated diameter is smaller again, which means the given .25 in is sufficient.

#### Design journal bearings


## Decide


## Communicate

