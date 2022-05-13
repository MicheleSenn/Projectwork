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
<!-- (50-60 words) --> Lia

## Research Questions
<!-- (50-60 words) --> 
<!--at least 2 research questions -->
Once a scare-off measure has proven to have an effect and cause the wild boars to relocate, it needs to be examined how long the effect lasts. Therefore, the two following research questions were formulated:
1. How can the long-term effects of scare-off measures be modelled?
2. Can a trend of returning to the scare-off location be detected or even conceptualized?

## Results / products
<!-- Lia -->
We have several expectations of behaviors that the wild boars will present.

1. We expect a quick return to the scare-off-location, e.g. withing a few days or maximum weeks if the measures are not repeated.
Result: It might be interesting to build a time series of returning animals after the measures, and also looking at what time of day the dare returning most.

2. We expect some kind of social behavior, e.g. meeting of and communication between individuals.
Result: Model meeting patterns, maybe followed by an analysis of lead-and-follow or flocking patterns.

Bonus:
3. We are interested if there are differences between the animals' natures such as very courageous vs. very fearful individuals.
Result: This information could be obtained when conceptualizing the time of return and their general movement radius compared between the individuals. Option 2: Relating biology to their behavior (influences such as mating season, etc.)

## Data
<!-- What data will you use? Will you require additional context data? Where do you get this data from? Do you already have all the data? --> Michèle
Long-term data for movement trajectories will be necessary (at least 6 weeks), different times of day, several individuals in a similar location
+ mapdata
new idea: --> for interpretation and some context, what about weather data? or background info on their social behavior / seasonal movements etc.

## Analytical concepts
<!-- Which analytical concepts will you use? What conceptual movement spaces and respective modelling approaches of trajectories will you be using? What additional spatial analysis methods will you be using?  Lia -->
- "Classic" EDA (plotting data in various ways in order to get an idea and find unexpected patterns)
- Calculating distances to Scare-Off-Location over time (-> e.g. Visualisation as timecube)
- Segmentation with Euclidean distance
- Trajectories with Moving Window Method to remove static points
- Meetings between animals on temporally close observations
- (Small  multiples of) trajectories or locations comparing seasons, time of day or individuals

## R concepts
<!-- Which R concepts, functions, packages will you mainly use. What additional spatial analysis methods will you be using? --> Michèle
...Spatial objects with sf, raster data and background map, plotly, ggplot2, tidyverse

## Risk analysis
<!-- What could be the biggest challenges/problems you might face? What is your plan B? Lia --> 
- We consider the scope a bit of a risk because of the amount of behaviors we could potentially analyse --> we need to be clear on what we really want to find out and stick to it.
- Interpretation of behaviors might be vague or non-causal because we assume that patterns can be detected when nothing is happening at all in reality (--> semantic annotations)
- Surprisingly, no differences between seasons / locations / individuals detected --> we can still focus on time series analysis
- Technical difficulties, e.g. when handling too much data, choosing irrelevant thresholds or interpretation issues.

## Questions?
<!-- Which questions would you like to discuss at the coaching session? --> Both
