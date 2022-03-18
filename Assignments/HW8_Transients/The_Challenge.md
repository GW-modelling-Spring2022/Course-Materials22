# Transients<!-- omit in toc -->

This week we are going to branch out from steady state and start including the concept of time in our models! We are going to go back to a simple model with a well in the middle and use this to explore the response of an aquifer to time-varying pumping.       

## Table of Contents <!-- omit in toc -->
- [Model Description](#model-description)
- [The Challenge](#the-challenge)
- [Glossary questions:](#glossary-questions)
- [What to Submit](#what-to-submit)
- [Correct Key Figures](#correct-key-figures)

## Model Description
​The model that you have been provided is set up for a homogeneous medium with a K of 1 m/day in all directions.  The single-layer domain is 50x50 cells.  The cells are 10 m in lateral extent and 50 m in vertical. There is a well located at [0,20,20] (layer, row, column).  Recharge occurs at a rate of 5e-4 m/day.  The left and right boundaries have constant heads of 50 m and 30 m, respectively.  The well is pumped cyclically.  Water is withdrawn at 500 m3/day for 90 days and then it is turned off for 270 days.  (Pretend that a year is 360 days long.)  The simulation is set to run for 10 years.  

## The Challenge
1) Plot the heads (or WTD) of the initial steady state condition.  The gradient is not uniform for the initial steady state conditions - discuss the influences of recharge and the unconfined condition on this nonlinearity

2) Determine if the system has reached steady state afert 10 years - consider a point at the well and another at the center of the domain.  
   
3) Repeat your run this time for 100 years and reconsider question 2 again. 

4) Find the zone of influence of the well defined in two ways:
    - Based on the drawdown from the initial steady state to the end of simulation time (end of final no-pumping stress period).
    - Based on the drawdown from the end of the last pump-on stress period to the end of simulation time.

## Glossary questions:
1.  Explain the concept of stress periods in MODFLOW. How should you determine stress periods when setting up your model? How do they differ from timesteps? 
   
2.  What is the period length in MODFLOW? How does the meaning of the period length differ for a steady state vs non steady state solution?
   
3.  What does the nstep variable signify in MODFLOW and how does it relate to the stress periods and period lengths? List the pros and cons of taking large timesteps vs. small timesteps. Is there any limit to how large a time step you can take and if so what determines this limit?  


## What to Submit 
(1) Submit your figures in a single doc or pdf along with captions to D2L and your ipynb to github by Tuesday before class (2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 

**Minimum Figures and calcualtions to submit:** 

## Correct Key Figures

In my opinion, there are four key figures but I will leave it to you to generate all the figures you need.

a) left panel showing the head at the well and right panel showing the head at the midpint of the domain, both as functions of time over the entire simulation.

b)  The head along a transect between the constant head boundaries through the well at three times: the initial steady state; the final pump-on period; and the final pump-off period.

c) A contour map with flow vectors at three times: the initial steady state; the final pump-on period; and the final pump-off period.

d) A contour map of the drawdown calculated for two periods: between the initial steady state and the final  simulation time and between the final pump-on period and the final pump-off period.

