# Recharge Me <!-- omit in toc -->

This week we will be adding recharge to our model and exploring unconfined conditions.  A flopy code is provided to you that recreates the 3D homogeneous box model with constant head boundary conditions.  

## Table of Contents <!-- omit in toc -->
- [Model Description](#model-description)
- [The Challenge](#the-challenge)
- [Glossary questions:](#glossary-questions)
- [What to Submit](#what-to-submit)

## Model Description
The model you are provided this week is simlar to the previous homeworks.  It is a homogeneousbox box domain with one layer. 

In the starter code the model is confined.  There is a well located at [0,10,15], but it is not being pumped.  The recharge rate is zero.  The left and right boundaries have constant heads of 20 and 10, respectively. 

For the challenge you are going to be exploring two things (1) what happens if this swaps from confined to unconfined conditions, (2) how recharge impacts your solution. 

## The Challenge
1. Change the boundary condition heads to make this an unconfined model. You can pick whatever heads you would like but I recommend keeping both of them above zero (*Hint:these are the variables H_left and H_right in the starter code*). Run two simulations with the same head gradient across the model (i.e. H_left minus H_right being the same between your confined and unconfined cases) but where one is confined and the other is unconfined. 
   - Plot the equipotentials and flow lines for both simulations 
   - Plot the head difference between the two simulations
   - Describe how the two head profiles differ and explain why this is the case. 
   - Would your  answer be different if you changed the overal head gradient (H_left-H_right), still keeping it the same between confined and unconfined cases though? 

2. For the two runs above (1) plot the flux across the left and right boundaries and (2) calculate the total flux. 
   - Compare these calculations and plots and provide an explanation for why you see the behavior you do. 
   - The overall gradient is the same, as is the K of the medium. Is the flow the same for both boundary conditions?  Why or why not? 

3.  Now add recharge at a constant rate of 1e-4 m/day over the entire land surface to an unconfined case with the left boundary set 7m and the right boundary set to a 2m.  
   - Explain the head transect and boundary flows.  
   - Is flow in this system 2D or 3D?  Is it represented as 2D or 3D?  Explain what you mean by your answers.

4. Update your model from #3 to model a system with zero recharge except for a farm located in [6:10, 6:10].   Recharge beneath the farm is 1e-4 m/day due to excess irrigation.  
   - Calculate the annual excess irrigation, in meters, that has been applied to the farm.  
   - Assuming that the crop is cotton, it is located in southern Arizona, and cotton is grown all year (for simplicity), calculate the total irrigation rate on the farm that would be associated with this amount of excess irrigation.  
   - Finally, use the flux diagram to identify the area within the domain that might be subject to contamination if the recharge water was somehow tainted (you can do this by saving the plot to powerpoint and annotating it there).    

5. Lastly, start the well located at [10,15] pumping at a rate of 8 m3/day.  Using one color, identify the capture zone of the well.  Using a second color, show the area that might be contaminated by the irrigated farm fields (see not above you can do your annotations in powerpoint if that is easier. ).  
   - Comment on the impact of the well on the pattern of potential contamination.   
   -  How will the steady state capture zone of a model with recharge differ from that in the same model without recharge?

## Glossary questions:
1. What does it mean for an aquifer to be unconfined?  How does this impact how we calculate flow and how do we expect it to impact head gradients and fluxes? 
   
2. List each layer type available in the LPF and BCF packages. Provide a brief summary explanation for each. Explain how approaches differ. 
   
3. How can MODFLOW, which does not model unsaturated flow, represent an unconfined aquifer? 

4. Define recharge. How do we represent recharge in a MODFLOW model? What package do we use and what are the assumptions of this package? Where exactly is the top boundary of the model? 
   

## What to Submit 
It's been a few weeks now so you know the drill. (1) Submit your figures in a single doc or pdf along with captions to D2L and your ipynb to github by Tuesday before class (2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 

**Minimum Figures and calcualtions to submit:** 
1. Challenge 1:
   - Equipotentials and flow lines for confined and unconfined simualtions
   - Head difference between the two simulations
2. Challenge 2: 
   - Report the total flux across the left and right boundaries for confined and unconfined simualtions
   - Plot the flux values for the left and right boundaries for both casese
3. Challenge 3: 
   - Head transect or equipotential lines for the recharge case
   - Plot the flux values for the left and right boundaries for both casese
4. Challenge 4: 
   - Report the total exess irrigigation applied per year in m
   - Report the total claculated irrigation per year and your assumed efficiency rate
   - Plot the flux values and equipotential lines and annotate it with the potential contamination zone
5. Challengge 5: 
   - Plot the annoated flux plot showing contamination and capture zones in different colors