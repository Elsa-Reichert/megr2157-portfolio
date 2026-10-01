# A6 - Bracket Drawing

## Objective
My assignment this week is create a parametric model and a detailed engineering drawing of the bracket from A5, the previous project. I need to create a comprehensive solid model and a multi-view engineering drawing that represesnts the previously designed dracket. 

## Analyze
#### Parametrically desinged model 
I will use Solidworks to design each feature.

Here is the sketch I hand drew last project. It needs to have these dementioned that I found priously. These dimentinos meet the strenght and stiffness requirements for the choosen material, Ti-6Al-4V. 

<img width="366" height="397" alt="image" src="https://github.com/user-attachments/assets/f0aa1407-3107-497a-a065-c4ab79e40640" />

First step is to add all equations to generate a parametric model

<img width="743" height="368" alt="image" src="https://github.com/user-attachments/assets/365c4c0d-374d-4bb4-bf7c-4dddb94052a9" />

I draw a little sketch to map each dimisino to the model.
[Photo of that]


<img width="543" height="548" alt="image" src="https://github.com/user-attachments/assets/0b91eb01-99b9-46ba-bf66-e3575b937a55" />

I created features A,B,C just using boss extrudes. features D and E were on both sides and symetrical. I first created the right sides using boss extrudes off the previous features. Then after that, I created a plane right in the center and reflected features D and E.


<img width="1025" height="596" alt="Screenshot 2026-09-30 174932" src="https://github.com/user-attachments/assets/774d3c2c-7385-44fd-91fc-3c8b825fdc7b" />


After building it I realized the dimentions I picked were not practicl. The equaution I used to find the cross section gives me a minimium value, while the bending equation gives me a maxium length value. This means I can lower the lengths of my featues without having to worry. This will make my structure deflect less and use less materials. I jsut needed to make sure that the a,b, and c measurements were still right because that was a given. 

<img width="908" height="553" alt="Screenshot 2026-09-30 175837" src="https://github.com/user-attachments/assets/556bc37c-80cf-4258-b2e3-5d981a012223" />

The final values I used.

<img width="750" height="377" alt="Screenshot 2026-09-30 181254" src="https://github.com/user-attachments/assets/8b2238b5-b718-4b27-b490-186a3610805a" />

Last, I needed to create a drawing of the model in third angle projection with a tolerance block. I kept most values at 2 decimal places because I did not need a high tolerence. The T shaped portion of the bracket is designed with specfici fliding fits. It needs a higher tolerence bceause of its perpuse. 

<img width="1664" height="914" alt="A6" src="https://github.com/user-attachments/assets/89fea917-5423-47f3-98be-0f29ddeba61b" />

## Decide


## Communicate
#### Reflectinos
I did not use the stiffness or strenth equations explicitly in the parametric equations used on my CAD model. This is because the strenth equation gives me a minimium area and the stiffness equation gives me a maximium length. This gives me a range to work with. I choose to use a very strong material, whcih gave me small minimium values and relativly large lengths. Manully lowering the length values or increasing the minimium value will also cause my bracket to be stronger or deflect less. Going under the minimium length will also cost less in materials. I did use parametric varaibles for each feature to quickly change the dimentions of the model. I did change a few of the dimestional varaibles to make the model smaller.

Most of the outside features of the struture had a .01 tolerence. This is because the outside area does not need to fit or slide into anything and therefor does not need a high tolerence. It is harder to meet smaller tolerances and using a larger tolerence when I can saves money on manufacturing. However the inside dimensions of the model do have higher tolerences. This is beacsue it is made to slide other strutures into it. It is a mating/functional surface.

