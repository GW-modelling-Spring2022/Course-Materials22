# Streams<!-- omit in toc -->

This week we will are going to be adding a stream to our model and exploring the packages available in Modflow to simulate stream aquifer interactions.  We are done with dicussion leads so our assignment will look a little different this week. Pay close attention to what is due when. 

## Table of Contents <!-- omit in toc -->
- [Part 1: Example using the stream package (str) in MODFLOW (Due Tuesday)](#part-1-example-using-the-stream-package-str-in-modflow-due-tuesday)
  - [Model Description](#model-description)
  - [The Challenge](#the-challenge)
  - [Correct Key Figures](#correct-key-figures)
- [Part 2: Exploring other stream-aquifer packages in MODFLOW (Due Thursday)](#part-2-exploring-other-stream-aquifer-packages-in-modflow-due-thursday)
  - [Resources:](#resources)

## Part 1: Example using the stream package (str) in MODFLOW (Due Tuesday)
This part is due **Tuesday**. Please turn in your correct figures along with discussion all at one time. Come to class prepared to diccuss your results and explain how the str package works. 

### Model Description
A flopy code is provided to you that simulates flow in a single layer model including a stream that runs along the center column.  There is uniformly distributed recharge over part of the domain.  There is no ET.  The aquifer is unconfined.  You will use this to explore stream-aquifer exchange.       
​
The model that you have been provided is set up for a homogeneous medium.  However, the streambed conductivity changes within three zones along the stream.  The single-layer domain is 51x51 cells.  The cells are 10 m in lateral and vertical extent. Recharge occurs at a rate of 5e-5 m/day in the first 26 rows.  The left and right boundaries have defined heads to represent a lake and a river, respectively.    

### The Challenge
1) Read the paper that summarizes the stream flow packages in Modflow and look at the [flopy documentation](https://flopy.readthedocs.io/en/3.3.5/source/flopy.modflow.mfstr.html) for the str package to understand how we have implemented this in our code. Write a short explanation for how the str package works and what assumptions it is making. 
 
2) The code is provided to produce the first set of 'correct' figures.  Use these figures to describe the nature (direction/magnitude) of stream/aquifer exchange along the stream.  In particular, explain why the leakage changes magnitude or direction where these values change.

3) Use the head distribution to describe the movement of water across the boundaries and into/out of the stream.    

4) Choose two things to explore (e.g. impact of streambed K or inflow into the river or recharge rate).  Produce a plot for each to compare to the base plots and use the plots to explain the impact of the hydrologic change.


### Correct Key Figures

The correct base figures are provided. Include in your report any variations that are needed to discuss your findings. Remeber that every figure must have a caption and don't include any figures in your report that you don't discuss. 



## Part 2: Exploring other stream-aquifer packages in MODFLOW (Due Thursday)
On Thursday we will be discussing the other stream-aquifer packages available in MODFLOW. We are going to split into two groups. 
1. If your **first name starts with A-H** you will be looking into the RIV package
2. If your **first name starts with J-z** you will be looking into the SFR package

Your assignment is to review the information for your package in (1) the description in the paper I've provided (2) the flopy documenation (3) the example jupyter notebook. For thursday please submit 3 pointpoint slides that expalin: 
- How the package works -- i.e. the general theoretical approach 
- How it differs in assumptions and approach from the str package 
- How you implement it in Python including some relevant code snippets of the parameters you need to set. 

### Resources: 
1. River (riv) package: 
    - [Flopy documenation](https://flopy.readthedocs.io/en/3.3.5/source/flopy.modflow.mfriv.html) 
    - Example code in the `riv_example` folder
1. Streamflow routing (sfr) package:
    - [Streamflow rounting (SFR) documentation](https://flopy.readthedocs.io/en/3.3.5/source/flopy.modflow.mfsfr2.html)
    - [Notebook example](https://github.com/modflowpy/flopy/blob/develop/examples/Notebooks/flopy3_sfrpackage_example.ipynb)
