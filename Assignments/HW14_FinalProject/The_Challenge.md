# Final Project Part 2: Advocacy modeling <!-- omit in toc -->

## Table of contents<!-- omit in toc -->
- [Your Challenge](#your-challenge)
- [What to submit](#what-to-submit)
- [Group Information](#group-information)
- [Domain Description](#domain-description)

## Your Challenge
This weeks asignment is open ended. You are going to work with you team to provide your best modeling analysis for your client and present your results in class next week. I have provided example notebooks which will run ensembles and load the outputs from those ensembles so that you can evaluate them. I strongly reccommend that you start from these notebooks but you are of course welcome to write your own too!

At a minimum you will need to: 
1. Modidify the ensembles notebook to run the 10 parameter cases your group came up with and the three scenarios you have decided to run in addition to your baseline scenario. This means you will be making 40 runs at a minimum (10 runs each for the baseline and your 3 scenarios).
2. Modify the analysis notebook to calculate the metrics of interest that you would like to evaluate. 
3. Create a presentation to summarize your findings

**Note: right now the model is setup to run for 20 years but nothin is changing from year to year. I set it up this way to make it easy to add seasonality if thats something your group wants to do.**

## What to submit 
You will be summarizing your findings in a powerpoint presentation. 
- Presentations should be submitted to the Final_Project folder on the [google drive](https://drive.google.com/drive/folders/1x8OZuTBGDEQmgel3HmAHWAg63kuNd-Vu?usp=sharing)
- Note that you are making this presentation as if you are a consulting firm hired to represent your client. You want to present your results in a scientifically defensible way but you also don't need to get into the details of flopy implementation. 
- Create any graphs needed to support your results but don't include graphs that you are not going to talk about.  One reason for creating the summary metrics is to make it easier to compare across simulations. 

Your presentation should discuss: 
- A brief overview of how you designed your scenarios 
- A dicussion of your scenarios and what you think they mean. What would you advocate for and why
- A discussion of parameter uncertaintiy and how this impacts your reults. You have already described your approach to designing your parameter sets in the last assignment so focus here on what your model simulations actually say aobut sensitivity and how this compares to what you expected
- A discussion of uncertainties and limitations of your approach. 
- A discussion of next steps. What additional measurements or simulations would you suggest your client invest in to better understand the system?  What additionl model simulations would you like to do if you had more time? 

## Group Information
You have been divided into three stakeholder groups:
1. **GroMore Industries**: Abigail, David, Hassan, John, Starlivia
2. **Friends of the Environment**: Adam, Devin, Jake, Jen, Xenia
3. **The Town of Aguaseca**: Connal, Diana, Jeffrey, Justin
Refer to last weeks assignment for more details on each groups interests

## Domain Description
Refer to the domain description provided in HW12 for this assignment. There are some minor modifications in the example python script I provided (i.e. using the river package and not including the town effluent recharge) you can assume that the setup I have in the example notebook is sufficient for this challenget. 


