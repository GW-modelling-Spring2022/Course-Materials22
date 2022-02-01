# Box Model- FloPy Exercise <!-- omit in toc -->

This week we will be starting with the same model from last week but instead of running it manually we will be using FloPy.

## Table of Contents <!-- omit in toc -->
- [Starter Code and Model Description](#starter-code-and-model-description)
- [Instructions for running the starter code](#instructions-for-running-the-starter-code)
- [The Challenge](#the-challenge)
- [Discussion questions](#discussion-questions)
- [Glossary questions:](#glossary-questions)
- [What to Submit:](#what-to-submit)
  - [Tuesday:](#tuesday)
  - [Thursday:](#thursday)

## Starter Code and Model Description
**Starer Code (`BoxModel_flopy.ipynb`):** A Jupyter notebook is provided to you that recreates the 2D, heterogeneous model that you created manually in MODFLOW for the last exercise.  The code creates plots that show the grid, boundary conditions, 2D K distribution, steady state boundary fluxes, and steady state heads along a profile connecting the constant head boundaries.  It also includes a plan view map that shows both equipotentials and flow vectors.  Nice, right?  The code has some modules (commented out) that you will use later.

​**Model**: The model that you have been provided is set up for a heterogeneous medium:  a homogeneous medium with a centered, square low K inclusion.  You will be asked to modify the K value of the inclusion and discuss the impacts on the head and boundary flux distributions.  You will also be asked to assess how the domain-scale equivalent K depends on the background and inclusion K values.  

## Instructions for running the starter code
1. Before you get started I recommend you watch this video on the [basics of FloPy](https://arizona.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=b9563086-6209-42f4-acb1-ae2f00128f72) and how it is different from the manual approach we did last week. 
2. Remember to copy of the `HW3_BoxModel_FloPy` assignment into the `working` directory of your homework repo before you get started so that you can save your work in your homework repo. 
3.  Open up the starter code (`BoxModel_flopy.ipynb`) in VScode and walk through it to make sure you understand the general flow of how it works. It's okay if you don't understand every line of code here just read the narrative and get a sense for generally how its setup.  If you are new to jupyter notebooks you can also watch this video on [Jupyter notebook baics](https://arizona.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=13a9b4bb-4729-43e7-ac63-ae2f001adada).
4.  Find the cell where the `moddir` is set and make sure that is updated to point to the location of the `mf2005.exe` file on your computer. 
5.  Run every cell of the notebook to ensure that the model runs and generates the plots. 
6.  Look in the directory where you ran the jupyter notebook to see what files were created. (you can do this straight from VScode) open these files and compare them to the files you generated manually in your Homework last week. 
7. Now that you have your bearings you are ready to continue to the Challenge! Note that for the challenge questions you will want to make modifications to the K field. To do this you will want to make changes to the BCF package directly in the Jupyter notebook (No need to edit files manually anymore!).  

## The Challenge
1.  For the initial values of background and inclusion K, plot the flow into the left and out of the right boundary.  (The code, as provided, makes this plot for you.)  
       - Explain why the values are not constant along the boundary (relate to the definition of a Type I boundary).  
       - Explain why the flow distributions are the same for the left and right boundaries.

2. Add a plot of the left-to-right flow along a line that passes through the center of the inclusion.  What can you learn from comparing this distribution to that seen on the boundaries?

3. Calculate the total flow into (and out of) the domain.  Use this to calculate the Keq of the heterogeneous system with the K values as given in the starter code.  
   
4. Repeat this calculation for the following K values for the inclusion (keeping the background K as it is given):  0.01, 0.1, 1, 10, 100.  
   
5. Compare the Keq calculated based on the total flow into and out of the domain to the harmonic and arithmetic mean K values calculated based on the area occupied by each medium (rather than the length for a 1D system).  Can you draw any general conclusions about the impact of high or low K heterogeneities on the equivalent K for the flow system examined?

## Discussion questions 
1. Does the equipotential distribution depend on the absolute or relative K values for the background and the inclusion?  How would you use the model to test your answer?
   
2. Discuss what it means to say that, for steady state flow, there are equivalent Type I and Type II boundary conditions.  How might this be useful in practice?

3. What would you find if you altered your model to consider unconfined conditions??

## Glossary questions:
1. What is FloPy?  How is it different from MODFLOW and how does it interact with MODFLOW?  What are some advantages (easy) and disadvantages (harder) of using FloPy rather than building MODFLOW models manually?
   
2. Given that the distribution of K is always heterogeneous at the small scale, what does it mean to provide one K value per grid cell? What are the implications for the K values we use in models in general? How does this change if we are modeling with different spatial resolutions (i.e. grid cell sizes)?
   
3.  What does it mean for a groundwater model to be confined? How does this simplify calculations of groundwater flux? How do we specify this with cell types in MODFLOW?  


## What to Submit: 
###  Tuesday: 
- Submit your Jupyter notebook through your homework repo on GitHub in your submisison folder `HW3_model_lastname.ipynb`
- Submit **one pdf file*** which includes at least the following graphs/tables (don't forget to include a caption for each graph that notes explains the model configuration that it goes with):
1. Line plot figures of the flow on the left and right boundary
2. Line plot figure with an additional line added showing flow through the center of the domain
3. Table of the total flows for the baseline and differing inclusion K cases (Challenge 3 &4)
4. Plots or tables comparing the three K calculations from challenge 5

### Thursday: 
In your markdown discussion file for this week (`HW2_discussion_lastname.md) please provide:
1) A discussion of your answers to challenge. 
2) Answers to the glossary questions
