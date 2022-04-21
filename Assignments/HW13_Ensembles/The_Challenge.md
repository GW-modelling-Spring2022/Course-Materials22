# Final Project Part 1: Ensembles <!-- omit in toc -->


## Table of contents<!-- omit in toc -->
- [Group Information](#group-information)
- [Domain Description](#domain-description)
  - [Parameter uncertainty](#parameter-uncertainty)
  - [Advocacy models](#advocacy-models)
- [The Challenge:](#the-challenge)
  - [Part 1: Metrics](#part-1-metrics)
  - [Part 2: Baseline ensemble:](#part-2-baseline-ensemble)
  - [Part 3: Advocacy scenarios](#part-3-advocacy-scenarios)
- [What to submit](#what-to-submit)

## Group Information
You have been divided into three stakeholder groups:
1. **GroMore Industries**: Abigail, David, Hassan, John, Starlivia
2. **Friends of the Environment**: Adam, Devin, Jake, Jen, Xenia
3. **The Town of Aguaseca**: Connal, Diana, Jeffrey, Justin

You will perform two functions for your group.  First, you will try to put yourself in the minds of your stakeholder - to look at the proposed agricultural activity from their (biased) point of view.  Second, you will act as consulting hydrogeologists for your stakeholder - helping them to bring scientific analyses to their decision making process.

**GroMore** is proposing to start a new agricultural effort in the basin growing pistacios.  Their proposal is included in the base model as the rectangular irrigated area with the elevated ET and the shallow pumping well.  They are resistant to changing this plan (location of the farm, crop, location of pumping well, etc) because they have agreements with the current landowner and have done a market analysis based on the proposed pumping and the projected value of the pistacios.

**Friends of the Environment** is interested in preserving the Green River and its adjacent riparian area.  They are concerned that the added pumping proposed by GroMore may reduce flow in the river and/or contribute N to the river, threatening a sensitive local water strider.   They are also concerned that lowered water levels may impact the riparian ecosystem.

**The Town of Aguaseca** is concerned that the proposed GroMore activities will affect the cost of operating their supply well (located in the lower aquifer) and/or degrade the quality of the town's water supply.  On the other hand, the town generally supports agriculture in the basin.

I will serve as the **Environmental Protection Agency** which has just been notified of the GroMore proposal.  At this point, they do not have any specific concerns.  But, they are examining the application for any possible negative impacts of the proposed activities on the environment of the basin.  They have ultimate regulatory jurisdiction and must approve the new activity.

## Domain Description
Refer to the domain description provided in HW12 for this assignment. 

### Parameter uncertainty
A model is comprised of many elements: abstractions on different levels.  We will refer to a group of related models as a model ensemble.  There are many types of uncertainty that can be represented with an ensemble of models, including:
 - *Conceptualization* - deciding which processes should be considered and which can be ignored for your specific modeling objectives.  Further, deciding how to represent processes, at which scale, and with what level of resolution.  This may include boundary condition types;
 - *Parameter uncertainty* - deciding on a reasonable range of values for parameters, boundary conditions, and stresses applied to the system.  This may include the location of applied stresses (decision variables);
 - *Spatio-temporal complexity* - deciding how much spatial variability to include in defining processes, properties, boundary conditions, and applied stresses.  Also, deciding whether it is important to consider outcomes through time or if steady-state is sufficient for the questions at hand.


We will limit ourselves to considering parameter uncertainty for now.  We will also be sharing model results, so we will all work from a common base model.  What will change is the parameter values. Each group will consider the impact of the proposed agricultural facility on the post-agriculture water level in the town's well.  Consider the following settings:
1. K of the upper and lower layers (isotropic) and horizontal K of the middle layer (all of this is one value),
1. Vertical K of the middle layer
1. Specific yield,
1. Mountain recharge rate,
1. Valley ET rate,
1. Riparian ET rate,
1. Streambed K

 Think of each of these as having a high, medium, or low value (given below).  

 - K1 and K3 = [5, 25, 100]               # Kx=Ky=Kz value in all zones (m/day)
 - Kzratio_lowK = [1e-6, 1e-2, 1]          # ratio of Kz in low-K layer to baseline K (-)
 - Sy = [0.05, 0.1, 0.3]                                 # specific yield (-)
 - R_mountains = [1e-5, 3e-5, 5e-5]       # recharge rate in mountains (m/day)
 - ET_valley = [1e-6, 1e-5, 1e-4]               # ET rate in valley (m/day)
- ETratio_riparian = [1, 2, 3]                    # ratio of ET in riparian area to  ET rate in valley (m/day)
 - Kratio_streambed = [1e-2,1e-1, 1]       # ratio of K in streambed to baseline K (-)

To organize our thinking about different model scenarios we are going to use the concept of a model tree. If we define a set the number of elements (ne) to be varied (you are considering 7) and the number of different values (nv) for each element (in this case we have three values: 1 = lowest; 2 = middle; 3 = highest), we can define the total number of possible models as nv^ne.  You have 2187 models to choose from.  

To keep track of the models, you can name them based on its element values, in order.  For example, a model with low values for every variable but high value for riparian ET would be  named model_1111131 and a model with  average values for the two conductivity parameters but low values for the rest would be model_2211111.  Thus, the name directly defines the values of each parameter.  It also describes the relationship between that model and other models.   This requires that we define the elements to vary and THE ORDER that they are listed in the model tree.  We also have to determine the number of values and the specific values for each element.  The order of the parameters. Follow the  ordering above and the prescribed high medium and low values for your model.  Be sure to familiarize yourself with them and ask questions if anything is unclear.  

### Advocacy models
So far, we have been exploring the sensitivity of our model results to the model parameters. Now  will consider the design of the ag facility we are modeling.

Your goal is to come up with a better plan from the perspective of your client.  You have to balance the hydrologic impacts with the preferences of GroMore.  (Don't propose a farm in the mountains and a well on the right boundary, for example). You will come up with three possible designs to present to the class.

You can change any of the following:
- The location of the irrigation well.  But, the ag interest will fight it if the well is farther from the farm than in the proposed plan.  (They are concerned about permitting and cost of delivery.)
- The crop.  But, the ag interest will not be happy about being restricted to a potentially lower value crop.
- The location of the farm.  But, the ag interest has worked out a pretty good deal for the land, so they will resist this, too.

You can pick whatever values you would like but you need to justify why they are reasonable suggestions.  Think carefully about which design you think will cause less negative impact based on the considerations your group might have. Do this BEFORE you start modeling.  

## The Challenge:
Your assignment this week is to design your modeling plan. First you will come up with a set of 10 model parameter sets that you think will best represent the uncertainty of the model. Then you will design 3 sceanrios from the point of view of your client.

### Part 1: Metrics
1. As a team decide on 3 metrics that want to measure from your model simulations that you think will be most informative in understanding scenarios.  These should be single values that can be calculated not spatial things tha you would plot (for example the losses from the stream, the water level in the town well, the water level in one of the observation wells, the total ET from the model, the area where the water level falls below the ET extinction depth). Provide a list of your metrics with a short explanation of why you chose them. 

### Part 2: Baseline ensemble:
1. For each parameter that we are varying write a short description of (1) what this parameter is and (2) how you expect changing it will influence your results. 
   
2. As group propose 10 combinations of the parameters listed above that you think will lead to the 'most different set' of predicted outcomes relative to the baseline (baseline is when all parameters are at there middle level). Think of this as the set of 10 simultions you can do which will best sample the space of your model. Your goal is not to choose sets of parameter values that lead to the best or worst outcome for your client. Rather, you want to define models that are 'most different from each other' with respect to your metrics of interest.
   
3. Rank your parameter sets in terms of which will generate the largest differences from the baseline scenario with respect to the metrics you chose. Present your rankings and your reasoning. 

### Part 3: Advocacy scenarios
1. Based on the options provided in the advocay section above, design three scenarios that your group would like to propose that you think will best suit the needs of your client.  Summarize each scenario along with your logic for creating it. 

## What to submit
- Each group will submit a powerpoint presentation answering every point from the three parts above before the start of class on Tuesday. 
- Presentations should be submitted to the Final_Project folder on the [google drive](https://drive.google.com/drive/folders/1x8OZuTBGDEQmgel3HmAHWAg63kuNd-Vu?usp=sharing). 
- Groups will present their modelling plan design during class.
