# A7 – Bracket FEA

## Objective
The goals for this assignment are:
  -Use Finite Element Analysis (FEA) to improve the previous bracket design
  -Ensure high stiffness, strength, and lightweight optimization through iterative design
  -Conduct multiple FEA simulations, refining gemometry based on results
  -Perform static stress analysis, including constraints, loading, and meshing selection
  -Interpret data by identifying max stress, displacement, and safety factors
  -optimize the design by modifying geometry to enhance performance
  -document the entire preosses
  -reflect

I was also given this table to fill out after each design:

<img width="585" height="250" alt="image" src="https://github.com/user-attachments/assets/1db1894d-5a7e-4192-abcc-6721667ad61f" />

I need to create a high stiff, high strengthm and lightwight component using FEA analysis throughout the design process.

After each step of the analysis and before making geometric changes, all components results must converge on a 7% difference after changing the mesh size to validate the model.

Photo of the model:

<img width="487" height="457" alt="image" src="https://github.com/user-attachments/assets/f48d4fe3-166e-40b2-89d3-abfcfadbfae4" />

## Analyze
### Givens
From the pervious assignemnts we know
  -Max. Deflection = 0.005 in
  -Yield strength of Ti-6AI-4V = 120000 Psi (given by solidworks)
  -Safety factor = 4
  -Max. stress = 30,000 psi

The dimensions for the inside of the bracket were given as shown and cannot be changed

<img width="437" height="126" alt="image" src="https://github.com/user-attachments/assets/707407a5-3255-4c49-9d72-c4b2a111824b" />


I needed to preform a static stress analysis for each new design, to find the safety factor, maximum stress and its location, and maximum displacement and its location. Then i need to validate the model by repeating until my converge results are within 7% or it is the third attempt to converge. After preforming the analysis and validating, I need to use that information to create and new design that improves either strength, stiffness, or reduces weight. 

I will use Solidworks for the stress analysis. 

I used the same file from the last two weeks. I changed the material to Ti-6AI-4V on the model. This material was chosen previously and all my dimensions are based off of that. We know the location and force from the previous assignements. The equiventlant force is equal to 2(500-800)lbs at the center of feature A

<img width="1281" height="651" alt="image" src="https://github.com/user-attachments/assets/fcb124d3-5577-461b-a75c-6c59a6b66d28" />

### Design 

Created a mesh

<img width="262" height="430" alt="image" src="https://github.com/user-attachments/assets/1ceabd65-7f06-433f-a166-93a0bb6337fe" />

I used 2(800)lbs because 800 was the largest in teh range and I wanted to test it at the hightest possible force to prevent failure.

<img width="1308" height="718" alt="image" src="https://github.com/user-attachments/assets/b86128cb-85d6-471a-b493-c492ac74baa3" />

Applied fixtures/constrants here because it is where the part connects to another item. 

<img width="1152" height="562" alt="image" src="https://github.com/user-attachments/assets/17b07b10-95a3-4616-bb31-ae654849cdf6" />

Results

<img width="1102" height="671" alt="image" src="https://github.com/user-attachments/assets/65d44825-d956-4022-a6d6-a3e5b3c2a395" />

<img width="1086" height="617" alt="image" src="https://github.com/user-attachments/assets/1df07bf9-f44c-49b4-974e-b12652b6afc2" />

<img width="1097" height="590" alt="image" src="https://github.com/user-attachments/assets/45004d1b-500e-4886-92f3-ec56b9a6862e" />

The max. stress and max. displacement from the study were higher than what I caluclated previously. I went back and recalculated the length of feature A. Using this equation from the mechinarys handbook 29th edition. I found a smaller maximium length. 

<img width="748" height="190" alt="image" src="https://github.com/user-attachments/assets/4d71951d-8863-45c8-bc53-c76a5be49b56" />

<img width="457" height="227" alt="image" src="https://github.com/user-attachments/assets/dce1d40d-6e6c-410e-9f69-d5973205ebb8" />


When calculating the geometry for the bracket, I treated feature A as being fixed to a wall. The forces used to claculate each feature was based off of that force on feature A being transfered. So I added another fixture to my study. This give me values a lot closer to what I calculated. 

New Fixed geometry

<img width="1083" height="606" alt="image" src="https://github.com/user-attachments/assets/fee7088b-22e9-413c-819b-c9bae7ffb885" />

New study results

<img width="1317" height="677" alt="image" src="https://github.com/user-attachments/assets/c2274907-ec1e-436e-bf5f-9fcd352029bf" />

<img width="1443" height="668" alt="image" src="https://github.com/user-attachments/assets/9042b517-946e-43c4-9e3a-dd2ec6556f8d" />

<img width="1310" height="652" alt="image" src="https://github.com/user-attachments/assets/62549e9d-2a4a-4020-ab8e-9eda6aff9aac" />

New values:
  -Max. Stress = 1.174e+04 psi at the top and bottom of the cross section of the front portion of feature A.
  -Max. Deflection = 4.768e-03 in at the end of feature A
  -Mass = 2.65 lb (given by solidworks)
  -Safety Factor = 10
  -Number of elements = Course Mesh

#### Validate

Now I need to validate the model by changing the mesh size and checking for convergence.

Formula for convergence

<img width="161" height="108" alt="image" src="https://github.com/user-attachments/assets/6605bf60-f1a4-4c96-a8d0-da324f6908ea" />

Using medium Mesh

<img width="652" height="501" alt="image" src="https://github.com/user-attachments/assets/b2ab8412-3818-4e95-813e-c6229ed4231d" />

New Values

<img width="667" height="528" alt="image" src="https://github.com/user-attachments/assets/adc484be-3ea2-4442-abbb-9502b8ec9cca" />

<img width="672" height="533" alt="image" src="https://github.com/user-attachments/assets/5ffdb4bb-1266-4053-9d36-b64c617ed989" />

Convergence found using formula 
  -Stress: 2%
  -Displacement: .01%
  -Safety Factor: 0.14%

Convergence was achieved.

### Design 2

I reduced the length and width of some features. This was to reduce the weight and material needed to produce the model. I reduced the length and widths of features B-E because there was not a lot of stress or bending here, So we did not need high cross-sectional areas. 

<img width="715" height="535" alt="image" src="https://github.com/user-attachments/assets/d184562c-7b77-46ec-ba6a-095dcad58a3b" />

These are the new values

<img width="635" height="336" alt="image" src="https://github.com/user-attachments/assets/7412a8ea-ccac-4531-9499-7ebb8896691c" />

New study using coase mesh and 1,600lbs of force along feature A

<img width="793" height="542" alt="image" src="https://github.com/user-attachments/assets/be520a25-997e-48c4-9427-c16bc0292260" />

<img width="755" height="546" alt="image" src="https://github.com/user-attachments/assets/e30e970f-9758-4b8b-9ee9-7e0fa367a503" />

The values are still below/at the maxiumium, but we do have higher deflection and stress. The delection is right at that .005 in minimium. 

New values
  -Max Stress: 1.316e+04 PSI at the top and bottom of the cross section of the front portion of feature A.
  -Max. deflection: 5.319e-03 at the end of feature A
  -Mass: .82 lbs
  -safety factor: 9
  -Number of elements: Course mesh

#### Validate
I will run another study on the same model but with a medium mesh density.

New values
<img width="366" height="462" alt="image" src="https://github.com/user-attachments/assets/87931db2-24e4-4ab8-8477-45c34bc512ab" />

<img width="586" height="443" alt="image" src="https://github.com/user-attachments/assets/61ed7e24-3cf8-4075-93ae-23c433cdbc5b" />

Calculating for convergence using the same forumla as before 
  -Stress: .1%
  -Displacement: 0%
  -Safety Factor: 0%

The values converge
### Design 3

I wanted to reduce the stress in feature A because it was concentrated in that one area, so I increased to radius of the cross section of feature A. This increased area will also cause less bending because deflection is related to the inertia of the cross sectional area. 

I also slightly reduced the length of feature A to reduce bending. I did not want to make it to short thought because it was made to hold a strap there. 

new model

<img width="582" height="485" alt="image" src="https://github.com/user-attachments/assets/4a017897-22f1-4b45-b58b-1fbeae47df12" />

New dimensions

<img width="757" height="327" alt="image" src="https://github.com/user-attachments/assets/532057ab-0bb5-457b-ad6a-2e1aaebfbaa1" />

New study using course mesh and new model

<img width="933" height="510" alt="image" src="https://github.com/user-attachments/assets/0ad8c67b-5adc-4957-a2ca-4abe9b7d447e" />

<img width="875" height="558" alt="image" src="https://github.com/user-attachments/assets/50284f28-40bf-43a7-8123-040ad5e1a51f" />

New values
  -Max Stress: 3.102e+03 PSI at the top and bottom of the cross section of the front portion of feature A.
  -Max. deflection: 6.078e-04 at the end of feature A
  -Mass: 1.56 lbs
  -safety factor: 39
  -Number of elements: Course mesh

#### Validate 
New study with the same model and medium mesh

<img width="726" height="668" alt="image" src="https://github.com/user-attachments/assets/5b011e05-57da-4d24-b553-4d2be04e8314" />

<img width="710" height="672" alt="image" src="https://github.com/user-attachments/assets/b2eda4a1-f4a0-4687-894e-9cae0e081981" />

Calculating for convergence using the same forumla as before 
  -Stress: .2%
  -Displacement: 0%
  -Safety Factor: 0%

They converge.

#### Table filled out
<img width="550" height="255" alt="image" src="https://github.com/user-attachments/assets/a572d999-c979-47f3-a8d4-f54927df8df4" />


## Decide
Each design choice was made to either reduce stress, bending, or material use. There was not a lot of stress in the upper portion of the model, so it made since to reduce material use/weight there. While the max. bending and stress was located at feature A, so it is more important to use more material here. 

## Communicate
This assignment taught me how to use FEAs to analytically look out a model and make logical changes based on that to find the right balance between strength, stiffness, and weight. It is important to improve on your design. The found minimium and maximum values are also not the best ones to use. They give you a good starting point and allow you know what range you can have, but increasing a minimium or reducing a maxiumium found value can give you more strength, stiffness, allow for less material use or reduce the weight.

