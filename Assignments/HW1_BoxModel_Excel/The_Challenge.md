# Box Model- Excel Exercise

An excel sheet is supplied that can model steady state saturated flow through a layered (or homogeneous) 1D vertical column with constant head top and bottom boundary conditions.   

## Model Description
​- The model that you have been provided is set up for a homogeneous medium.  You will be asked to modify the K distribution to form a layered medium to answer some of the questions.  
- Remember that the focus of this course is primarily to use models to improve your hydrogeologic understanding.  In other words, getting the model to run correctly is step one,
then The Challenge begins!

## The Challenge
1. Show, based on the flux with depth, that the model is steady state.  Repeat this for a homogeneous and for a heterogeneous column.
1. Show that the steady state flux agrees with the direct calculation based on the harmonic mean average K.  Write the equation defining the direct calculation of the flux.
1. Show the steady state head profile for a column with approximately equal-thickness layers that have different K values.  
1. Use the head profile to explain WHY the equivalent hydraulic conductivity, Keq, is closer to the lower of the two K values.


## Correct Key Figures
In this case, your model really should work.  One thing that might hang you up is - you have to have iterative solutions activated in Excel.  If you get a 'circular reference' error, search online for how to fix this.  If your model just bombs, shut it down without saving and reopen it.

Just to be sure that you have the right figures upon which to base your answers to The Challenge, I have included screenshots of the model with a homogeneous solution and another with a heterogeneous solution.  You do not need to use the same boundary condition or K values that I used.  In fact, I would encourage you to play around with the model a bit!

![](assets/The_Challenge-e7287a98.JPG)
*Figure 1: Spreadsheet with a solution for a homogeneous column.*

![](HW1_heterogeneous.jpg)
![](assets/The_Challenge-261d7adc.JPG)

*Figure 2: Spreadsheet with a solution for a two-layer heterogeneous column.*


## Discussion Points
*In addition to The Challenge, start thinking about the following ideas:*
1. What are boundary conditions?  Answer this both conceptually and mathematically.
1. What are model parameters?  How do they (and don't they) represent the actual subsurface?
1. What are steady state conditions and how can they be identified from the Excel model results?
1. Can you imagine how the model inputs could be stored in separate files rather than other spreadsheet cells?  Describe the flow of information from a file that describes the other files that contain model-specific information about the system.
1. What is an iterative solution?  Can you explain it to a hydrologist who is not a modeler?  Can you describe (or imagine) how Excel finds the solution?
1. What is a direct solution?  What are its (dis)advantages compared to an iterative (numerical) solution?
   
## Glossary Questions: 
To be added to our class notes glossary (see the link in the course readme). Each questions should have a 1-2 paragraph answer. Feel free to add links to references or helpful graphics. 
1.  What is a model?  What is a ground water model?  How are ground water models used?
2.  What are model parameters?  How do they (and don't they) represent the actual subsurface?
3.  What does it mean for a model to be in steady state? Discuss your answer with respect to both heads and fluxes. What is the utility of steady state solutions in the practice of groundwater modeling (i.e. when and why do we use steady state solutions)?