# Layers<!-- omit in toc -->

This week we will start exploring models with multiple vertical layers and we will change the top surface of our model to follow topography. 

## Table of Contents <!-- omit in toc -->
- [The Challenge](#the-challenge)
- [Gloassary Questions](#gloassary-questions)
- [Correct Key Figures](#correct-key-figures)
- [What to Submit](#what-to-submit)


### Model Description
The starter code contains two models setups for you. 

1) A single layer model: 
   The model should have 50x50 cells, each 100 m in x and in y. There is one layer, 100 m thick. The medium is homogeneous with K = 1.0 m/day in x and y and 0.1 m/day in z. The porosity is 0.35, specific yield is 0.3, and storage coefficient is 0.001. The left boundary is a constant head of 85 m relative to the datum, which is located at the bottom of the domain. The right boundary is a fixed head of 70 m. All other boundaries are no flow.  Recharge is uniform over the entire domain and occurs at a rate of 5E-5. A well is located at (2500,2500) and is pumped at a rate of 500 m3/d. The land surface is 100 m above the datum on the left boundary and slopes linearly to an elevation of 85 m at the right boundary.

2) A three layer model:
   Add a low conductivity (Kx=Ky=Kz=0.0001 m/d) layer extending from 25 to 35 m above the base of the domain. The left boundary has a constant head of 85 m relative to the datum in all layers. The right boundary has a constant head of 70 m relative to the datum in the bottom layer and is no flow in the other two layers. The well is only completed in the lowest layer.


## The Challenge
1) Compare the impact of pumping on the signle layer model vs the multi layer model.  What physical explanation do you have for the differences? 

2) Repeat the three layer simulations putting the well in each layer (i.e. once in the bottom once in the middle and once in the top) provide plots and discussions comparing and contrasting your simulations. Provide at least one plot where you have all of your runs in the same figure. 

3) Change the properties of your three layer model so that it matches the 1 layer model (but still has 3 layers) put the pump in the bottom layer and compare and contrast with your one layer solution. How does your answer to this challenge compare with your answer to the first? 

4) Modify the topography of your domain so that it is no longer sloping left to right (you can make it a valley or have it sloping the other way, whatever you want). Re-run you 1 and 3 layer solutions and explain any differecens you do or don't see.    

## Gloassary Questions
1) Layers: 
Why do we want multiple layers in our groundwater models? Compare and contrast the different approaches to vertical discretization (briefly describe different approaches and discuss their strengths and weaknesses).  
 
2) Discretization: 
What are the pros and cons of adding more layers to a model? Are there considerations for vertical discretization that are different from horizontal discretization? 

3) Stream Aquifer Exchange: 
How is water exchanged between a stream and an underlying aquifer?  Include the following concepts: (dis)connected streams; streambed hydraulic conductivity; boundary condition type; and coupled models.


## Correct Key Figures
Once again I'm going to leave this up to you. Provide all of the figures that you think are necessary to support your answer. Note that I've included some additional figure types in the starter script this week. Feel free to pull in figures you liked from previous assignments too. 

Two notes: 
1. Make sure to include captions for all graphs that you includ
2. Don't just copy and past a 100 graphs into your report. Any graph that you include should be refereced and discussed in your answer for your Thursday report. 

## What to Submit 
Back to our usual schedule: (1) submit your graphs by Tuesday (2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 

