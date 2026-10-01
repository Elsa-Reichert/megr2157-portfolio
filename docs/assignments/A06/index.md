# A6 - Bracket Drawing

## Objective
My assignment this week is create a parametric model and a detailed engineering drawing of the bracket from A5, the previous project. I need to create a comprehensive solid model and a multi-view engineering drawing that represesnts the previously designed bracket. 

## Analyze
#### Parametrically designed bracket model 
I will use Solidworks to design each feature.

Here is the sketch I hand drew last project. It needs to have these dimensions that I found priously. These dimensions meet the strenght and stiffness requirements for the choosen material, Ti-6Al-4V. 

<img width="366" height="397" alt="image" src="https://github.com/user-attachments/assets/f0aa1407-3107-497a-a065-c4ab79e40640" />

First step is to add all equations to generate a parametric model

<img width="743" height="368" alt="image" src="https://github.com/user-attachments/assets/365c4c0d-374d-4bb4-bf7c-4dddb94052a9" />

Then I can create the model.

<img width="543" height="548" alt="image" src="https://github.com/user-attachments/assets/0b91eb01-99b9-46ba-bf66-e3575b937a55" />

I created features A,B,C using boss extrudes. features D and E were on both sides and symetrical. I first created the right sides using boss extrudes off the previous features. Then after that, I created a plane right in the center and reflected features D and E.


<img width="1025" height="596" alt="Screenshot 2026-09-30 174932" src="https://github.com/user-attachments/assets/774d3c2c-7385-44fd-91fc-3c8b825fdc7b" />


After building it I realized the dimensions I picked were not practical. The equations I used to find the cross section gives me a minimum value, while the bending equation gives me a maximum length value. This means I can lower the lengths of my features without having to worry. This will make my structure deflect less and use less materials too. I just needed to make sure that the a,b, and c measurements were still right because that was a given. 

<img width="908" height="553" alt="Screenshot 2026-09-30 175837" src="https://github.com/user-attachments/assets/556bc37c-80cf-4258-b2e3-5d981a012223" />

The final values I used.

<img width="750" height="377" alt="Screenshot 2026-09-30 181254" src="https://github.com/user-attachments/assets/8b2238b5-b718-4b27-b490-186a3610805a" />

#### Bracket drawing
Last, I needed to create a drawing of the model in third angle projection with a tolerance block. I kept most values at 2 decimal places because I did not need a high tolerance for those. The T shaped portion of the bracket is designed with specific sliding fits. It needs a higher tolerance because of its purpose. 

<img width="1664" height="914" alt="A6" src="https://github.com/user-attachments/assets/89fea917-5423-47f3-98be-0f29ddeba61b" />

#### Link CAD Design

First I created variables for the link.

<img width="762" height="257" alt="Screenshot 2026-09-30 220753" src="https://github.com/user-attachments/assets/ef0cbab2-16d7-4f21-8fb0-6c0e7502ff46" />

Started with this shape.
<img width="542" height="642" alt="Screenshot 2026-09-30 220119" src="https://github.com/user-attachments/assets/5a4f648e-cc8e-48e8-930f-756482593965" />

After created a bose extrude and cut the two holes I realized my model was not long enough. The calclated length for the ealier assignment was a maximium value, but it is related to the cross sectional area. I decieded to use a larger cross sectional area. I then had to recalculate the length value with the new cross sectional area and got 19in. 

<img width="597" height="638" alt="Screenshot 2026-09-30 220736" src="https://github.com/user-attachments/assets/ba68dee5-5bb5-4342-bbed-a5da6a1464d4" />

I went with 3 in because it was more practical, will cause less deflection, and cost less to manufacture. 

<img width="830" height="437" alt="Screenshot 2026-09-30 224411" src="https://github.com/user-attachments/assets/76c26380-b329-4c36-8277-a018c9f4bebc" />


THis is what the final model looked like.


<img width="1196" height="617" alt="image" src="https://github.com/user-attachments/assets/5dd62a3b-4d45-4fe9-917a-b7d8e9fdab80" />

I had to change the diamaters in the model because I misread the graphs I used on the last assignment. The tolerence values were given in thousands of an inch.

<img width="707" height="497" alt="image" src="https://github.com/user-attachments/assets/1341193e-f0f3-46a4-8e66-e657134caf16" />

<img width="652" height="596" alt="Screenshot 2026-09-30 224135" src="https://github.com/user-attachments/assets/c83f3813-7b07-4f8b-9ef6-87bfbab7efa0" />

[Tables from](https://www.cobanengineering.com/Tolerances/ANSIRunningSlidingFits.asp). These were used both for clearance limits and tolereance limts.

#### Link Drawing
Then I used this model to create an engineering drawing in Third-angle projection and tolerence blocks. 

<img width="432" height="904" alt="A6 link" src="https://github.com/user-attachments/assets/87aba7e2-fc41-42cb-b3f2-56b19d3987b3" />

## Communicate
#### Reflections part 1
I did not use the stiffness or strength equations explicitly in the parametric equations used on my CAD model. This is because the strength equation gives me a minimum area and the stiffness equation gives me a maximum length. This gives me a range to work with. I choose to use a very strong material, which gave me small minimum values and relatively large lengths. lowering the length values or increasing the minimum value will also cause my bracket to be stronger or deflect less. Going under the minimum length will also cost less in materials. I did use parametric varaibles for each feature to quickly change the dimentions of the model. I did change a few of the dimensional varaibles to make the model smaller.

Most of the outside features of the structure had a .01 tolerance. This is because the outside area does not need to fit or slide into anything and therefor does not need a high tolerance. It is harder to meet smaller tolerances and costs more to manufactor. However the inside dimensions of the model do have higher tolerances. This is because it is made to slide other structures into it. It is a mating/functional surface.

#### Reflections part 2
It is important to use the right tolerances for each feature/dimension. Different features have different functions. It is important for part to part compatibility for specific dimesions. While other areas can have a lower tolerence. It is still important to use lower tolerances when possible because it will save you on time and money.

The dimensioning and tolerancing can communicate which pieces are mating/fucntional and the type of fit needed. 

#### Files for models and drawings
[Bracket model](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A06/A6.SLDPRT) [Bracket drawing](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A06/A6.SLDDRW) [Link model](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A06/A6%20link.SLDPRT) [Link drawing](https://github.com/Elsa-Reichert/megr2157-portfolio/blob/main/docs/assignments/A06/A6%20link.SLDDRW) 
