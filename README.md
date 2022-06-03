# Proposal for Semester Project

**Patterns & Trends in Environmental Data / Computational Movement
Analysis Geo 880**

| Semester:      | FS22                              |
|----------------|---------------------------------- |
| **Data:**      | Wild Boar Movement Data           |
| **Title:**     | Scare-off measures against wild boars         |
| **Student 1:** | Michèle Senn                 |
| **Student 2:** | Lia Baumann                 |

## Abstract 
<!-- (50-60 words) -->
This project aims at modelling the behavior or wild boars after scare-off measures. It is hypothesized that they will return within a few days back to the scare-off location and this returning pattern will be analysed. 

## Research Questions
<!-- (50-60 words) --> 
<!--at least 2 research questions -->
Once a scare-off measure has proven to have an effect and cause the wild boars to relocate, it needs to be examined how long the effect lasts. Therefore, the  following research question was formulated:

How can the returning of the boars be modelled?

## Results / products

We expect a quick return to the scare-off-location, e.g. withing a few days if the measures are not repeated.
Result: It might be interesting to build a time series of returning animals after the measures, and also looking at what time of day the dare returning most.

## Data
<!-- What data will you use? Will you require additional context data? Where do you get this data from? Do you already have all the data? --> 
- Long-term data for movement trajectories will be necessary (at least 6 weeks).
- Data should be of different times of day and of several individuals in a similar location.
- Furthermore, mapdata will be needed.
- Some background information on the boars social behavior and seasonal movements would also be interesting and help for a better understanding of the data. 

## Analytical concepts
<!-- Which analytical concepts will you use? What conceptual movement spaces and respective modelling approaches of trajectories will you be using? What additional spatial analysis methods will you be using? -->
- EDA: plotting data in order to get an idea of what the data looks like and finding patterns like which individual is Schrecked by what
- Calculating distances to Scare-Off-Location over time using the ST_Distance() function, which returns the shortest distance that separates two geometries
- Trajectories with Moving Window Method to remove static points
- Plot spatial and time overlaps between the tracked animals
- Find returning patterns by building a "In the Field / not in the Field" vs. distance to Schreck graph

## R concepts
<!-- Which R concepts, functions, packages will you mainly use. What additional spatial analysis methods will you be using? --> 
The modeling will be done using the following concepts and packages:
- Spatial objects will be created with the r-package "sf"
- raster data and background maps will be plotted and visuallized with these r-packages: "plotly", "ggplot2"
- For the reshaping and transforming of date the r-package "tidyverse" will be used

## Risk analysis
<!-- What could be the biggest challenges/problems you might face? What is your plan B? --> 
- We consider the scope a bit of a risk because of the amount of behaviors we could potentially analyse --> we need to be clear on what we really want to find out and stick to it.
- Interpretation of behaviors might be vague or non-causal because we assume that patterns can be detected when nothing is happening at all in reality (--> semantic annotations)
- Surprisingly, no differences between seasons / locations / individuals detected --> we can still focus on time series analysis
- Technical difficulties, e.g. when handling too much data, choosing irrelevant thresholds or interpretation issues.
- Possibly, the different measures don't show the same effects. We might need to distinguish between measures in order to draw inferences.

## Questions?
<!-- Which questions would you like to discuss at the coaching session? -->
- Long-term data for movement trajectories will be necessary (at least 6 weeks).
- Data should be of different times of day and of several individuals in a similar location.
- Where to get weather data / background data
