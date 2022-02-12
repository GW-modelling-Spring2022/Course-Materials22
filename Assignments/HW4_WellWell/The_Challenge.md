# Well, Well <!-- omit in toc -->

This week we will be adding a pumping well to our model. A flopy code is provided to you that recreates the 2D homogeneous box model with constant head boundary conditions.  

## Table of Contents <!-- omit in toc -->
- [Model Description](#model-description)
- [Notes to keep in mind](#notes-to-keep-in-mind)
- [The challenge](#the-challenge)
- [Glossary Questions](#glossary-questions)
- [What to Submit](#what-to-submit)

## Model Description
​The model that you have been provided is set up for a homogeneous medium with a well pumping at a constant rate.    You will be asked to modify the location of the domain and examine the impacts on flow across the boundaries and the steady state head and drawdown distributions. 

Remember that the focus of this course is primarily to use models to improve your hydrogeologic understanding.  In other words, getting the model to run correctly is step one, then The Challenge begins!

## Notes to keep in mind
*Note 1: If you need help getting the starter code going refer back to the instructions from last weeks homework. The general process is the same you will need to (1)Copy the assignment into your Homework Repo, (2)open the starter code and confirm that the notebook is using your `gwmod` python environment (3)update your the moddir path to match the location where your MODFLOW executable is (Note: you can grab this path from your HW3 notebook as it won't change from week to week*

*Note 2: Whenver locations are provide in `[]` this means that we are refering to the index in the python numpy array. Remember that the python ordering is `[z,y,x]` (i.e `[layer, row, column]`) for a 3D array and `[y,x]` (i.e. `[row, column]`) for a 2D array. Also remember that row numbering in python starts from the top (i.e. row0 is the top row in your arrary). This means that a row location of 0 will actulaly corespond to a y location of 2450 because our y axis in modflow starts at the bottom and increases moving north. You don't need to make any adjustments to the code to account for this you can input the locations in the homework exactly as they are given just note that if we put the well at `[0,5,5]` it is correct that it will end up in the top left portion of the domain and not the bottom left (refer to [this video](https://arizona.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5cca566d-65d9-4def-bd3b-ae3a011785e5) on Python indexing and the modflow grid for more info)*


## The challenge
1. The well is located at [0,10,15] in the starter code and it is withdrawing water at a rate of -8 m3/day (note, the rate is negative to indicate water being removed from the domain).  You need to move the well to the center of the domain [0,12,12] and change the rate to -10 m3/day.
   
   **Python Tip**
   ```
   - The well is setup in section 8.1
   - The pumping rate of the well is given by the variable Q_in 
   - The location is the well is specified in the fluxes array where the first three numbers are the location of the well in [z,y,x] and the fourth number is the pumping rate
   ```

2. For the initial well location, plot the total flow into the left (constant head = 20) and out of the right (constant head = 10) boundaries.  (The code, as provided, makes this plot for you.)  
   - Explain why the values are not constant along the boundary (relate to the definition of a Type I boundary).  
   - Explain the shapes of the flow distributions and why they are not the same for the left (inflow) and right (outflow) boundaries.
   -  You are still modeling stead state conditions?  So, what is supplying water to the well?

3. Plot series of the flow left-to-right along a vertical line that passes through the center of the well [:,12]
   - How do you interpret the flow along this transect?  (Hint, also look at the flow along a transect just upgradient from the well [:,11]).
  
     **Python Tip**
   ```
   - You can copy the block of code that creates the boundary flux lines as a starter for this plot
   - I'm asking for a vertical set of flow values(i.e. a line at one y location or column of the model)
   - Remember that the python convention is [y,x], therefore to get a vertical line  of fluxes out we will want to grab a single x location out of the flux_vals matrix like this [:,colpick] where column pick is whatever column number you are wanting to look at. 
   - to modify the graph you should modify the following line so that 'rightflux' is whatever you name the flux variable you calculated and you can change its legend title by changing the lable and change the color or marker if you like too 
   plt.plot(x,rightflux,marker='x', color='blue', markersize=4, linestyle='--',label="right boundary")
   ```

4. Then, look at the plot of equipotentials (i.e. the constant head lines, this is the last plot in the example) and flow vectors.  Describe how water flows through the domain.  To aid in your description, draw a line through all of the flow vectors that terminate in the well.  This approximates the capture zone of the well. Use this to refine your description of the flow system, being as specific as possible about where water that ends up being extracted by the well originates on the inflow boundary.  

5. Then, look at the plan view drawdown plot. 
   -  Why aren't the drawdown contours circles?  Either explain why this is correct, or fix the plot. 
   -  Why are the drawdown contours not equally spaced?    

6. Move the well to [0,5,5].  Use all plots necessary to describe fully how water is flowing through the domain with the well in this location.  Be sure to include the drawdown plot in your discussion - compare this plot to the equipotentials and flow vectors. 

**BONUS** 
Before running the model, predict what you would happen to the inflow/outflow boundary fluxes if you reduced the pumping rate to -5 with the well located at [0,12,12].  Were you correct?  If not, how were you wrong? Now predict what would happen if you increased the pumping rate to -20.  Still correct?  Now try -25.  Uh oh, what happened?? 

## Glossary Questions
1. What are equipotentials? How do we create them from MODFLOW Models? 
2. What are flowlines?  (BONUS thought experiment: How can you impose a no flow boundary based on symmetry?  Give it a shot to explain WHY this works in a couple of sentences.)
3. What are flownets? And how does a flonet vary from a map of equipotentials with flow lines drawn on it? 
4. Define the concept of 'capture' in a way that a non-expert might understand? (e.g. think about our homework problem, if the right boundary represented a stream, what would the impact of the well be on the stream?)

## What to Submit 
It's been a few weeks now so you know the drill. (1) Submit your figures in a single doc or pdf along with captions to D2L and your ipynb to github by Tuesday before class (2) submit your complete answer to the challenge discussion and glossary questions including figures and discussion to D2L by class on Thursday. 

**Minimum Figures to submit:** 
- Base case boundary flows 
- Base case flux through midline of domain.
- Base case equipotentials and flow vectors.
- Base case drawdown around centered well 
- Moved well drawdown plot
- Moved well equipotentials and flow vectors
- Additional plots to explain the moved well case

