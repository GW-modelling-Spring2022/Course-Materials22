# Traspired <!-- omit in toc -->

This is the last week in our series of adding modules to our box model and its dedicated to evapotranspiration! 

## Table of Contents <!-- omit in toc -->
- [Model Description](#model-description)
- [The Challenge](#the-challenge)
- [Glossary questions:](#glossary-questions)
- [What to Submit](#what-to-submit)
   

## Model Description
​The model that you have been provided is set up for a homogeneous medium and is now 15 m thick.  There is a well located at [0,10,15], but it is not being pumped.  The background recharge rate is zero.  There is a region of localized recharge in [6:10, 6:10] with a recharge rate of 5e-4 m/day.  ET occurs over the entire domain at a rate of 5e-5 m/day and an extinction depth of 3 m.  The left and right boundaries have constant heads of 15 and 5, respectively.      

## The Challenge
1.  For the initial boundary head values and recharge and ET rates:
   - plot the flow across the left and right bounaries. Explain what you see and why it makes sense. 
   - Plot the equipotentials and flow vectors in plan view and outline (hand draw) the area that would be affected by recharge (i.e. if it were contaminated).  Explain what you are seeing and why. 
   - Plot ET,Recharge and Water Table depth and explain why we see the patterns we do. 
  
2. Calculate the water balance for the model
    - Report all of the inflows and outflows with units and show that mass is being balanced. 
    - Explain what controls each term in your water balance. 

3. Change the extinction depth in your model.
   - Report the new water blance numbers 
   - Provide a plot of the new head countours and fluxes
   - Explain what changed and why. 

4. Now start the well pumping, extracting 20 m3/day.  
   - Plot the equipotentials and flow vectors in plan view and outline (hand draw) the area that would be affected by recharge (i.e. if it were contaminated).  
   - Plot ET,Recharge and Water Table depth and explain why we see the patterns we do. 
   - How does the well change the zone that is affected by the recharge area?  
   - How does it affect the ET map?  

5. Write a mass balance for the well. 
    - How much water is coming from a boundary?  How much is originating as recharge?  How do you account for the impact of ET on this mass balance?  
    - At steady state, what are the effects of 'capture' by the well?

## Glossary questions:
1. Define Evapotranspiration. Explain in the real world (1) the components of evapotranspiration (2) where this water is pulled from and (3) the physical drivers and controls that determine evapotranspiration rates.
   
2. Describe how the `evt` package in MODFLOW models evapotranspiration. List the assumptions and simplifications that this package is making.
   
3. What is a land surface model? What are the differences between groundwater models like MODFLOW and land surface models that also simulate the shallow subsurface?  When is each preferred over the other?

## What to Submit 
It's been a few weeks now so you know the drill. (1) Submit your figures in a single doc or pdf along with captions to D2L and your ipynb to github by Tuesday before class (2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 

**Minimum Figures and calcualtions to submit:** 
Challenge 1
   - plot the flow across the left and right bounaries. 
   - Plot the equipotentials and flow vectors in plan view and outline (hand draw) the area that would be affected by recharge (i.e. if it were contaminated).  
   - Plot ET,Recharge and Water Table depth.

Challenge 2
    - Report all of the inflows and outflows with units and show that mass is being balanced. 

Challenge 3
   - Water blance numbers 
   - Plot of the new head countours and fluxes

Challenge 4
   - Plot the equipotentials and flow vectors in plan view and outline (hand draw) the area that would be affected by recharge (i.e. if it were contaminated).  
   - Plot ET,Recharge and Water Table depth 

Challenge 5
    - Report the water balance numbers for the well.





