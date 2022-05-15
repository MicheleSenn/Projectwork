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
This project aims at modelling the behavior or wild boars after scare-off measures. It is hypothesized that they will return rather quickly back to the scare-off location and this returning pattern will be analysed. Additionally, the individuals are expected to communicate with each other and influence their time of returning, which will also be conceptualized in this project.

## Research Questions
<!-- (50-60 words) --> 
<!--at least 2 research questions -->
Once a scare-off measure has proven to have an effect and cause the wild boars to relocate, it needs to be examined how long the effect lasts. Therefore, the two following research questions were formulated:
1. How can the long-term effects of scare-off measures be modelled?
2. Can a trend of returning to the scare-off location be detected or even conceptualized?

## Results / products

We have several expectations of behaviors that the wild boars will present.

1. We expect a quick return to the scare-off-location, e.g. withing a few days or maximum weeks if the measures are not repeated.
Result: It might be interesting to build a time series of returning animals after the measures, and also looking at what time of day the dare returning most.

2. We expect some kind of social behavior, e.g. meeting of and communication between individuals.
Result: Model meeting patterns, maybe followed by an analysis of lead-and-follow or flocking patterns.

Bonus:

3. We are interested if there are differences between the animals' natures such as very courageous vs. very fearful individuals.
Result: This information could be obtained when conceptualizing the time of return and their general movement radius compared between the individuals. Option 2: Relating biology to their behavior (influences such as mating season, etc.)

## Data
<!-- What data will you use? Will you require additional context data? Where do you get this data from? Do you already have all the data? --> 
- Long-term data for movement trajectories will be necessary (at least 6 weeks).
- Data should be of different times of day and of several individuals in a similar location --> we need to find these sources.
- Furthermore, mapdata will be needed, which can be aquired from open sources.
- Weather data would help to put the visualiziations into context and would help for a better interpretation. This could be acquired from open sources.
- Some background information on the boars social behavior and seasonal movements would also be interesting and help for a better understanding of the data. It could be difficult to get that data though.

## Analytical concepts
<!-- Which analytical concepts will you use? What conceptual movement spaces and respective modelling approaches of trajectories will you be using? What additional spatial analysis methods will you be using? -->
- "Classic" EDA (plotting data in various ways in order to get an idea and find unexpected patterns)
- Calculating distances to Scare-Off-Location over time (-> e.g. Visualisation as timecube)
- Segmentation with Euclidean distance
- Trajectories with Moving Window Method to remove static points
- Meetings between animals on temporally close observations
- (Small  multiples of) trajectories or locations comparing seasons, time of day or individuals

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