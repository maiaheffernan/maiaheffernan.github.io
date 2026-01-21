# Delta plots for December data

The main thrust of my work this week was creating the delta plots and sectioned-out profiles of salinity, temperature, and DO concnetration from the December field work. The point of all this was to complement Dakota's variance data from the model and look at variance at difference points in the cove to see if there are any locations that stand out to us as being "separate." To be honest I am not sure how helpful the plots I have below are, but they are at least a start on my end with the December data!

### Some caveats with these plots
Before I jump into the plots here, I want to note a few things that need to be considered when looking at these plots/my plans for adding things for next week:
1) I will add the ADCP bottom track data for these profiles so we can actually see how far down we got! I got deep in interpolation land with this and ran out of time.
2) My interpolation and/or for the percent differences, **especially salinity**, are suspect. I used linear interpolation. Is this the best method for the non-linear profile data I have? Would pchip be better? I am still a novice at interpolation and am not sure. **Also** it is very possible that there is a QC issue in the salinity data. I am still working through this.
3) I am not 100% convinced these breaks into the different sections of the transects are correct. We did not write down our turning timing in the deck notes for the second lap very consistently so I had to guess some of the timings. I will look more into this.
4) Is this format helpful for viewing this data?


### The plots

#### Salinity

Let's first look at the profiles themselves:

![Figure 1. Salinity profiles in each lap and each section of the laps](../_figures/Salinity_allLaps_allSections.png)




Now for the delta plots. Here I show the percent difference between the salinity values between laps. The columns show the difference between lap 1 and lap 2 and lap 2 and lap 3, and the rows show the different locations.

![Figure 2. Percent difference in salinity between sequential laps](../_figures/Salinity_deltaPlots.png)






#### Temperature

First the profiles.

![Figure 3. Temperature profiles in each lap and each section of the laps](../_figures/Temperature_allLaps_allSections.png)



Now for the delta plots.


![Figure 4. Percent difference in temperature between sequential laps](../_figures/Temperature_deltaPlots.png)





#### DO concentration

First the profiles.

![Figure 5. DO concentration profiles in each lap and each section of the laps](../_figures/DO_allLaps_allSections.png)



Now the delta plots.

![Figure 6. Percent difference in DO concentrations between sequential laps](../_figures/DO_deltaPlots.png)




