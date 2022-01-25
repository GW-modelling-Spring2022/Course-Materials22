# Box Model- Hand-Built MODFLOW <!-- omit in toc -->

This week we will be running a simple box model in MODFLOW using **manual** input files. MODFLOW files have been supplied that model steady state saturated flow through a homogenous 3D system.  The layers are flat lying.  The top and bottom faces and two opposite vertical boundaries are no-flow.  Each of the other two faces has a constant head applied to each.

## Table of Contents <!-- omit in toc -->
- [Steps for running the starter code](#steps-for-running-the-starter-code)
  - [Step 1: Look at the inputs](#step-1-look-at-the-inputs)
  - [Step 2: Run the example model](#step-2-run-the-example-model)
  - [Step 3: Explore the baseline model outputs](#step-3-explore-the-baseline-model-outputs)
  - [Step 4: Repeat steps 1-3 for the challenge making modifications to your model.](#step-4-repeat-steps-1-3-for-the-challenge-making-modifications-to-your-model)
- [The Challenge](#the-challenge)
- [Glossary Questions:](#glossary-questions)
- [What to Submit:](#what-to-submit)
  - [Tuesday:](#tuesday)
  - [Thursday:](#thursday)


## Steps for running the starter code
### Step 1: Look at the inputs 
- Watch the modflow input files [video](https://arizona.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5ea4fab8-9068-4d14-8fbe-ae2800f2924c) for more informaiton on the structure of the input files. 

- Copy the input files into your Homework repo and look through the files in conjunction with the  [user guide](https://water.usgs.gov/ogw/modflow/MODFLOW-2005-Guide/) to understand the model that is being created. I recommend going to the `Input Files Supported in Various Versions of MODFLOW` tab on the table of contents and using this to navigate to each of the input file formats. 
You should have the following files: 
  - `nam`: Master name file that lists all the other files that will be used
  - `bas`: The basic package where boundary condition types and initial heads are specified
  - `dis`: The discretization file that specifies the number of rows, columns. layers, their timesteps and time units.
  - `bcf`: Block centered flow file where the properties that control flow are entered (i.e hydraulic conductivity)
  - `oc`: Output control file specifying what outputs will be saved and printed
  - `pcg`: Preconditioned conjugate Gradient package -- this specifies the solver and the solver settings

### Step 2: Run the example model 
 run the MODFLOW model from command line using the following steps:

If you are PC: 
 - copy mf2005.exe into the directory with your MODFLOW input files.
 - Open a command window (you can do this by opening GitBash or just opening a new terminal window from inside vscode) 
 - If you are not already in the directory with the files navigate to the directory with your MODFLOW input files.  (cd is the command to change directories)
- Type `mf2005 BoxModel_Manual` in the command window and hit enter.  This should run MODFLOW and overwrite your output files.

If you are Mac: 
  - Make sure you have installed ModFlow following the setup instructions before you start 
  - Open a terminal window (either with the terminal application or within VScode)
  - Find the path to where you have your modflow application built and put it somewhere easy to find (e.g. `/Applications/MODFLOW/mf2005`)
  - Navigate to the directory with the model files and Type (assuming you put your MODFLOW in the same place as me if not replace this path with your path) `/Applications/MODFLOW/mf2005 BoxModel_Manual`

### Step 3: Explore the baseline model outputs
- When you run the file a `.list` file will be created that summarizes all of the model setup and outputs (`.hds` and `.cbc` files may also be created but we will not focus on these for now). 
- Use the `HW_02_visualization_example.xls` sheet to help you visualize your outputs (note that we are just manually copying the heads from the model that come out of the list file here and the k field from the bcf file)

### Step 4: Repeat steps 1-3 for the challenge making modifications to your model. 


## The Challenge 
1. Create a conceptual model of the homogenous MODFLOW model: This should be an illustration that shows the locations and values of constant head boundaries, the number of grid cells and their spacing as well as any other model properties. You should also include in here a cross section with your predicted head gradient and direction of flow.  You can draw this by hand if you would like. 

2. Show, based on the flux with horizontal distance from a constant head boundary, that the model is steady state.  Repeat this for a homogenous and a heterogenous cases where you place different K values in series in the direction of flow (Note: to modify the K values you should change the `.bcf` file, just be careful because spacing matters!  Note 2: see the excel sheet for an example calculating flux. Keep in mind that that heads are calculated at the center of a cell and the K values are defined across the entirety of a cell)

3. Show the steady state head contour in plan view for the homogenenous and heterogeneous (zones in series) condition.  Use this plot to defend a contention that flow is 1D.  Then, drawing on your first assignment, use the results to explain WHY the equivalent hydraulic conductivity, Keq, is closer to the lower of the two K values.

4. Build a model based on a homogeneous domain with a square region of lower K in the middle of the domain.  What can you learn based on your explanation of what controls the effective K for a 1D flow system now that you are applying it to a 2D system?  What do you think the Keq of this entire system would be compared to the high and low K values?  Explain why it is much more difficult to develop a direct solution for this 2D system than it was for a 1D system (including the zones placed in series). 
   
5. For steady state conditions, there are equivalent Type I and Type II boundary conditions.  What would the Type II boundary condition be that would result in the same equipotentials for the first model?  What is the value of the constant flux?  What about the second model?  What are the values of the constant flux on the left and right boundaries?  What is fundamentally different about the equivalent Type II boundary for the third model compared to the first two? 

## Glossary Questions:
1. What is MODFLOW?  What is a MODFLOW package (provide at least 2 examples)?  What are the inputs to a MODFLOW model?
   
2. What is the relationship between head gradients and hydraulic conductivity in steady state systems? 

3. What is a model node?  A model cell?  Use a simple diagram to show the relationship between heads defined at nodes and properties defined in cells.
   
4. What is the difference between TypeI and Type II boundary conditions and under what conditions might you use each? Provide at least 2 examples for locations where we might use Type I or Type II boundaries to represent a feature in the real world. 


## What to Submit: 
###  Tuesday: 
- No need to submit model files or excel workbooks this week. Just submit your graphs. Create **one pdf file named HW2_figures_lastname.pdf** which includes at least the following graphs (don't forget to include a caption for each graph that notes explains the model configuration that it goes with):
1. Your conceptual figure of the baseline model in both plan and cross section view
2. Plan view figures of the head distribution for at least 3 cases 
   1. Homogenous domain 
   2. Heterogenous domain where K varies in the direction of flow
   3. Heterogenous domain with a box of low K in the middle of the domain 

Optional figure you might want to add: 
1. Cross sections of hydraulic head 
2. Plan views of the hydraulic conductivity that goes with each output

### Thursday: 
In your markdown discussion file for this week (`HW2_discussion_lastname.md) please provide:
1) A discussion of your answers to challenge. 
2) Answers to the glossary questions


If you want to establish purely horizontal flow, what (specifically) should be defined as constant along the constant head boundaries?



