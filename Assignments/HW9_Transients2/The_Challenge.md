# Transients<!-- omit in toc -->

This is a short week and we are going to be building off the transient model we assembled last week to include transient ET and recharge.     

## Table of Contents <!-- omit in toc -->
- [Model Description](#model-description)
- [The Challenge](#the-challenge)
- [Glossary questions:](#glossary-questions)
- [What to Submit](#what-to-submit)
- [Key Figures](#key-figures)

## Model Description
You will be starting from the same model as last week with one modifiction: now we have transient ET setup. The model that you have been provided is set up for a homogeneous medium with a K of 1 m/day in all directions.  The single-layer domain is 50x50 cells.  The cells are 10 m in lateral extent and 50 m in vertical. There is a well located at [0,20,20] (layer, row, column).  Recharge occurs at a rate of 5e-4 m/day.  The left and right boundaries have constant heads of 50 m and 30 m, respectively.  The well is pumped cyclically.  Water is withdrawn at 500 m3/day for 90 days and then it is turned off for 270 days.  (Pretend that a year is 360 days long.)  The simulation is set to run for 10 years.  In addition to pumping we now have cyclical ET turned on such that the ET rate is 1e-3m/day when the well is pumping and 0 for the rest of the year. 

## The Challenge
1) Compare your results for the case with no ET to the modified ET case and explain how your results differ. To do this I'm expecting you will create some plots as well as looking at the water balance

2) Modify the model so that the ET only occurs in a square area around the well that is 200m by 200m. Discuss how this changes your results using plots and water balance calculations. 
   
3) Modify the recharge in the model so that it is also transient. Its up to you how you want to modify it. Provide and explanation for the scenario you ran and explain how it impacts your results. 


## Glossary questions:
1. What are initial conditions? Describe various approaches to determining initial conditions for a groundwater model. 
   
2.  What does it mean for a groundwater model to be ‘spun up’?  How can we go about achieving this and how would we know if we are done?  What can happen if you run transient models on a groundwater model that is not spun up?
   
3.  Groundwater is generally the slowest moving component of the hydrologic cycle. Describe (1) the speeds at which groundwater flows compared to surface water (2) the time scales over which water tables and groundwater heads respond to changes in pumping vs recharge in both confined and unconfined systems?  What are the implications of these timescales for how we model groundwater systems? 


## What to Submit 
(1) Nothing is due on Tuesday but please take a first attempt at coding this up and we will work on it more in class(2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 


## Key Figures
This week is more open ended I am leaving it up to you to provide the plots to explain what you are seeing. 
