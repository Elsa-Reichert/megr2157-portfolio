# A7 – Bracket FEA

## Objective
The goals for this assignment are:
  -Use Finite Element Analysis (FEA) to improse the prevous bracket design
  -Ensure high stiffness, strength, and lightweight optimization through iterative design
  -Conduct multiple FEA simulations, refining gemometry based on results
  -Perform static stress analysis, including constraints, loading, and meshing selectino
  -Interpret data by identifying max stress, displacement, and safety factors
  -optimize the design by modifying geometry to enhance performance,
  -document the entire preosses
  -reflect

I was also given this table to use:
<img width="585" height="250" alt="image" src="https://github.com/user-attachments/assets/1db1894d-5a7e-4192-abcc-6721667ad61f" />

I need to create a high stiff, high strengthm and lightwight component using FEA analysis throguuut the design process.

Each step of the analysis and before making geometric changes, all components results must converge on a 7% difference. This can be achieved by modifying the number of elements.

<img width="487" height="457" alt="image" src="https://github.com/user-attachments/assets/f48d4fe3-166e-40b2-89d3-abfcfadbfae4" />

## Analyze
### Givens
From the pervious assignemnts we know
  -Max. Deflection = 0.005 in
  -Yield strength of Ti-6AI-4V = 120000 Psi (given by solidworks)
  -Safety factor = 4
  -Max. stress = 30,000 psi

I needed to proform a static stress analysis for each design, to dinf the safety factor, maximium stress and its location, and maximium displacement and its location. Then i need to validate the model by repeating unitil my converge results are within 7% or it is the third attempt to converge. 

I will use Solidworks for the stress analysis. 

I used the same file from the last two weeks. I changed the material to Ti-6AI-4V on the model. This material was chosen previously and all my dimensions are based off of that. We know the location and force from the previous assignements. The equiventlant force is equal to 2(500-800)lbs at the center of feature A

<img width="1281" height="651" alt="image" src="https://github.com/user-attachments/assets/fcb124d3-5577-461b-a75c-6c59a6b66d28" />

Created a mesh
<img width="262" height="430" alt="image" src="https://github.com/user-attachments/assets/1ceabd65-7f06-433f-a166-93a0bb6337fe" />

I used 2(800)lbs because 800 was the largest in teh range and I wanted to test it at the hightest possible force to prevent failulte.

<img width="1308" height="718" alt="image" src="https://github.com/user-attachments/assets/b86128cb-85d6-471a-b493-c492ac74baa3" />

Applied fixtures/constrants here because it is where the part connects to another item. 
<img width="1152" height="562" alt="image" src="https://github.com/user-attachments/assets/17b07b10-95a3-4616-bb31-ae654849cdf6" />

Results
<img width="1102" height="671" alt="image" src="https://github.com/user-attachments/assets/65d44825-d956-4022-a6d6-a3e5b3c2a395" />
<img width="1086" height="617" alt="image" src="https://github.com/user-attachments/assets/1df07bf9-f44c-49b4-974e-b12652b6afc2" />
<img width="1097" height="590" alt="image" src="https://github.com/user-attachments/assets/45004d1b-500e-4886-92f3-ec56b9a6862e" />

The max. stress and max. displacement from the study were higher than what I caluclated previously. I went back and recalculated the length of feature A. Using this equation from the mechinarys handbook 29th edition. I found a smaller maximium length. 

<img width="748" height="190" alt="image" src="https://github.com/user-attachments/assets/4d71951d-8863-45c8-bc53-c76a5be49b56" />

{photo from notebook}

When calculating the geometry for the bracket, I treated feature A as being fixed to a wall. The forces used to claculate each feature was based off of that force on feature A being transfered. So I added another fixture to my study. This give me values a lot closer to what I calculated. 

New Fixed geometry
<img width="1083" height="606" alt="image" src="https://github.com/user-attachments/assets/fee7088b-22e9-413c-819b-c9bae7ffb885" />

New study results
<img width="1317" height="677" alt="image" src="https://github.com/user-attachments/assets/c2274907-ec1e-436e-bf5f-9fcd352029bf" />
<img width="1443" height="668" alt="image" src="https://github.com/user-attachments/assets/9042b517-946e-43c4-9e3a-dd2ec6556f8d" />
<img width="1310" height="652" alt="image" src="https://github.com/user-attachments/assets/62549e9d-2a4a-4020-ab8e-9eda6aff9aac" />

Max. Stress = 1.174e+04 psi at the top and bottom of the cross section of the front portion of feature A.
Max. Deflection = 4.768e-03 at the end of feature A
Mass = 2.65 lb (given by solidworks)
Safety Factor = 10
Number of elements = 

Now I need to validate the model by changing the mesh and checking for convergence.

Formula for convergence
<img width="161" height="108" alt="image" src="https://github.com/user-attachments/assets/6605bf60-f1a4-4c96-a8d0-da324f6908ea" />

Using medium Mesh
<img width="652" height="501" alt="image" src="https://github.com/user-attachments/assets/b2ab8412-3818-4e95-813e-c6229ed4231d" />

New Values

<img width="667" height="528" alt="image" src="https://github.com/user-attachments/assets/adc484be-3ea2-4442-abbb-9502b8ec9cca" />

<img width="672" height="533" alt="image" src="https://github.com/user-attachments/assets/5ffdb4bb-1266-4053-9d36-b64c617ed989" />



## Decide


## Communicate

