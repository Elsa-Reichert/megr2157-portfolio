# A3 – Parametric and FEA

## Objective
My objective for this project is to design a bar using a circular cross section where the values of the criteria are given for the material, maximum deflection, and load. I then need to determine the bars minimum geometry through parametric design while under direct tension. Then verify the geometry through finite element analysis. 

The purpose of this assignment is to learn how to use parametric design to determine a beams geometry and learn how to use finite element analysis to verify that geomtry

## Analyze
### Parametrically Design
My first task was to parametricaly design a bar in CAD with an applied direcy load between 300-500lbs, a max axial deflexton of .009 in, and a E value between 8.5 x 10^6 - 11.5 x 10^6 psi.

To do this I used the equations feature in Solidworks and made a variable for the radius of the cross section, the area of the cross section, the force applied to the bar, the max selection, Young's Modulus of the material (Al), and the length of the bar. This allowed me to change any value very quickly, because now the CAD program is using that variable to calculate different values and variables for the geometry of the structure. This means if I needed to change the radius, instead of changing the values in my drawing and recalculating every equation, I just need to change the radius variable.

Because I am given a range for the force and Youngs Modulus, this approch allows me to change either of those values within that range to see what the structure will do. It also makes it more convieiont to change the gemotry if needed. This helped me a lot because I ended up changing the radius 3 times.  

My first set of variables written out in Solidworks. Here the length of the bar is parametrically determined and area is calculated. 

![Equations in solidworks](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Solidworks%20eqations%20screenshot.jpg)

The equauation for the axial deformation is: 
![axial deformation equation](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/axial%20deformation%20eq.jpg)

Which can be rearanged to find the length:

![solved for L](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/solved%20for%20L.jpg)

I did not put enought thought into the radius. This was a mistake I made twice. You can see my first r value was 1 in. Which would make L equal about 400-1000inin depending on the Force value and Young's Modulus Value. I descided to change it to .05 to make it more practical. Here is a photo of the oringal r value strucutre.

![r=1,l=800](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Lmax%20400%2B%20in.jpg)

Here are my revised values.

![revised values 1](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/New%20equations%201.jpg)

My new struture. I was happy with how this one turned out and to change it all I had to do was go into the equations menu and change that r value.

![new strutue one](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/New%20length%20pic.jpg)

Using this radius value; r = .05. I expiramented with the force and Young's Modulus values to get the longest and shortest bar. The bar's length is this longest when the force is at its maximum value and Young's Modulus is at its minimum value. This makes sense if you look at the axial defomration equation. After solving for L, F is at the bottom and E is at the top, which means when F gets bigger, L gets smaller and when E gets larger, L gets larger. 

![longest L, at r = .05](docs/assignments/A03/Longest.jpg) 
![shortest L, at r = .05](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/smallest%20L.jpg) 

### FEA
After I was happy with my design, I needed to use this drawing to conduct a FEA bar using the same force load used to calculate the bars geometry. To do this, I ran a simulation on my drawing in Solidworks with the material set as 6061-T6 alummanium. 

The values of 6061-T6 given by solidworks. 

![values of 6061-T6](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Values%20of%206061-T6.jpg)

Next I created fixed gemortry one one face. 

![fixed geomtry](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Fixed%20geo.jpg)

Then added a 300 lb normal force in tension on the opposite face as such. 

![normal 300lb simulation](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/-300.jpg) 

After this, I added mesh to the structure

![mesh](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/%2Bmesh.jpg)

Then generated a von Mises stress map, deflection map, and Strain. Please note the graphs are in SI still. I did not change them because I realized something was wrong. 

![first von Mises](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Sim%20ran%20von%20mises.jpg)
![first deflection](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Sim%20ran%20URES.jpg)
![first strain](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Sim%20Ran%20ESTRN.jpg)

After looking at these maps, I realized the force was causing stress greater then the materials yield strength. This will cause permanent deformation in the structure. The yield strength in SI for aluminum is 2.750e+08 N/m^2, but the simulation is reading values up to 2.769e+08 N/m^2. I realized the issue was the area of the structure. I did not calculate an area and radius based on the yield strength and a safety factor. Thankfully it was a quick fix.

First I had to calculate the minimium requred area using the stress equation. I rounded the yield strength value given by solid works to 40x10^3. I also added a safety factor of 3.

![Finding A min.](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/New%20equations%201.jpg)

I then used the calculated minimum area value to find the minimium r value. 

![finding r min.](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/finding%20r%20min.jpg)

Because the bar was parametrically designed, all I had to do was go into the equations tab and change r to .09in. It was rounded to .09 because Solidworks is set to 2 decimals by default. I did not feel the need to change it because .085 was a minimum value and I felt the values were precise enough.  

New values at r = .09in

![table r = .09in](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Ever%20newer%20equations.jpg)

New bar

![Bar r= .09in](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/Final%20bar.jpg)

Now with these new values I just needed to run a simulation again. 

![Final van mises stress](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/NEw%20von%20mises.jpg)
![Final delection map](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/New%20URES.jpg)
![Final Strain](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/New%20ESTRN.jpg)

The simulation found the maximum stress in the bar was about 1.238e+04 psi. The yield strength of 6061-T6 is about 4e+04 psi. I am under the yield strength. 
Using this equation, I find the safety factor is about 3.25. This is about what I calculated. It is a little higher which makes sense because the radius and area are a little higher which lowered the strain. 

![eq for sf](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/eq%20for%20safety%20factor.jpg)

### Modify Design Parameters
While keeping the fixture and material the same, I changed the force to 15,000llb and radius to 20in. I think the length will decrease because the force is changes more and is at the bottom of the equation. 

![design modify](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/changing%20values.jpg)

My guess was wrong. The length value ended up a lot bigger. The radius changed the area and that got multiplied by Young's Modulus. 

## Decide
I needed to design a bar with a circular cross sectional area. I needed an area big enough to keep the stress under the yield strength. I added a safety factory of 3 because it is standard and to reduce the chances of my structure failing. Using this, I find the minimum radius needed, r = .09in. The material, 1601 t6 aluminum, was chosen because it has a relatively high yield strength while still being light weight. 

## Communicate
### Design Reflection
The axial deflection from my parametric hand-calculations is about .009in. The FEA map caluclated the max axial deflection value as .008989 in. This is a .122% different.

I did expect these values to be the same. Axial deflection is related to the geomtry and axial deflection is used to calculate the length. All these values effected the FEA map. The stresses inside the bar are also very even.

I trust the results more from the FEA map. The axial deflection calculated by hand is related to stress and we can only use average stess. The FEA map can show different magnitudes of stresses throughout the bar. So I beilive it would end up being more accurate. Uneven stress throughout the bar could lead to more axial deflection in one area too. 

### Small Pin Hole?
Next I need to imagine a pin hole at the side of the bar. 

![Graph of kt](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/kt.jpg)
The graph and information is from: https://www.slideshare.net/slideshow/2-axial-loading-54457126/54457126 

Using the equation given the maximum value at the pin hole would be about k*1.2e+4 = 37,140psi. Which is below the yield strength of aluminum (40,000 psi) but it does not pass my safety factory.

This assignment took me about 5-6 hours to finish. 

### CAD Files
[Drawing file](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/A3.SLDPRT)
[Displacement map](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/A3-Tenstile-Results-Displacement1.analysis.eprt)
[Strain map](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/A3-Tenstile-Results-Strain1.analysis.eprt)
[stress map](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A03/A3-Tenstile-Results-Stress1.analysis.eprt)
