# Transients<!-- omit in toc -->

This week we are going to branch out from steady state and start including the concept of time in our models! We are going to go back to a simple model with a well in the middle and use this to explore the response of an aquifer to time-varying pumping.       

## Table of Contents <!-- omit in toc -->
- [Model Description](#model-description)
- [The Challenges](#the-challenges)
- [Correct Key Figures](#correct-key-figures)
- [Glossary questions:](#glossary-questions)
- [What to Submit](#what-to-submit)

## Model Description
​The model that you have been provided is set up for a homogeneous medium with a K of 1 m/day in all directions.  The single-layer domain is 50x50 cells.  The cells are 10 m in lateral extent and 50 m in vertical. There is a well located at [0,20,20] (layer, row, column).  Recharge occurs at a rate of 5e-4 m/day.  The left and right boundaries have constant heads of 50 m and 30 m, respectively.  The well is pumped cyclically.  Water is withdrawn at 500 m3/day for 90 days and then it is turned off for 270 days.  (Pretend that a year is 360 days long.)  The simulation is set to run for 100 years.  

Anything written in these directions supercedes anything in the header of the starter code.  For anything that is not mentioned explicitly here, follow the description in the header of the starter code.


## The Challenges
a) The gradient is not uniform for the initial steady state conditions - discuss the influences of recharge and the unconfined condition on this nonlinearity

b) Determine if the system has reached steady state - consider a point at the well and another at the center of the domain.  

c) Find the zone of influence of the well defined in two ways:
    - Based on the drawdown from the initial steady state to the end of simulation time (end of final no-pumping stress period).
    - Based on the drawdown from the end of the last pump-on stress period to the end of simulation time.

d) How long does it take a point at the center of the domain to reach steady state.  At that point, explain how you could divide the domain into a steady and transient part and solve each separately.

e) Find a constant pumping rate (same throughout the year) that matches the head time series at the middle of the domain.  

f) Find a constant pumping rate (same throughout the year) that matches the head time series at the well, leaving only a regular, repeating seasonal residual.  Are the two pumping rates the same?

g) Discuss the sources of water captured by this well.  If you're up for a challenge, calculate them for the final pump-on period!

h) Discuss how you would define the capture zone of the well.  How is it different than our definitions of capture zone so far in the course?


## Correct Key Figures

In my opinion, there are four key figures.

a) left panel showing the head at the well and right panel showing the head at the midpint of the domain, both as functions of time over the entire simulation.

b)  The head along a transect between the constant head boundaries through the well at three times: the initial steady state; the final pump-on period; and the final pump-off period.

c) A contour map with flow vectors at three times: the initial steady state; the final pump-on period; and the final pump-off period.

d) A contour map of the drawdown calculated for two periods: between the initial steady state and the final  simulation time and between the final pump-on period and the final pump-off period.

## Glossary questions:
1. 

## What to Submit 
It's been a few weeks now so you know the drill. (1) Submit your figures in a single doc or pdf along with captions to D2L and your ipynb to github by Tuesday before class (2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 

**Minimum Figures and calcualtions to submit:** 