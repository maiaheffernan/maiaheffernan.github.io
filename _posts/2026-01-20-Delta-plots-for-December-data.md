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

**Let's first look at the profiles themselves.**


<img alt="Figure 1. Salinity profiles in each lap and each section of the laps" src="https://github.com/user-attachments/assets/b5d51afb-4401-46c0-a9b7-dff191f900dd" />


Not much new here from what we've seen in the 3D plots from last week and from the profiles I included in the cruise report. The columns show the lap number, the rows show the transect section in the cove. 

Here are some **major takeaways:**
- In the entrance to Lap 1 we were getting our casting feet under us. We got better by lap 3.
- Generally, in all the profiles the fresh layer is primarily in the top 2-3 meters of water and the mixed layer begins at around 5 meters and continues on down to 10 meters below the surface.
- There is maybe some interesting high salinity values at depth in the third transect? This is suspect and is likely a QC issue.




**Now for the delta plots.** Here I show the percent difference between the salinity values between laps. The columns show the difference between lap 1 and lap 2 and lap 2 and lap 3, and the rows show the different locations.


<img alt="Figure 2. Percent difference in salinity between sequential laps" src="https://github.com/user-attachments/assets/bba21beb-4de2-41bc-9736-f8dccec908a9" />



I want to note here that there were some really suspect values in this data after I interpolated. I understand that this is a difference plot, but we need to be cautious when interpreting this one. I will fix this up for next week.

**Takeaways:**
- The largest percent difference in salinity comes at around 5 meters in the water column. This is where the fresh layer seems to be.
- The salinity increased by a large percent between the 1st and 2nd lap at this 5m mark. *remember: the first lap caught the weak flood and the slack/low and the second lap caught the flood*
- The southern end upper water column salinity almost all increased between laps 1 and 2. Can we see this in the profiles above?
- Between laps 2 and 3, however, the salinity decreased at this same 5m-ish mark. *the second lap caught the flood, the third lap caught the tail end of the flood, the high, and then the first part major ebb of the day*
- At the entrance between laps 2 and 3 (we were here at salck tide), the salinity increases at the surface and decreases right below the surface. It would be interested to compare this to velocity data. NEXT WEEK!



#### Temperature

**First the profiles.**

<img alt="Figure 3. Temperature profiles in each lap and each section of the laps" src="https://github.com/user-attachments/assets/0d230c38-2062-4f16-92fb-0d2a858c60bc" />


**Takeaways:**
- Water is colder at the surface than at depth. This makes sense for winter.
- Similar to salintiy, the fresh, cold layer tends to be in the top 2-3ish meters, then the mixed layer extends down to *around* 10 meters.
- The fresh, cold layer is a lot thinner in the second lap, during the flood. However the mixed layer stays relatively the same. Is there just more surface mixing at this time?

  


**Now for the delta plots.**


<img alt="Figure 4. Percent difference in temperature between sequential laps" src="https://github.com/user-attachments/assets/c81a8caa-830f-4829-a719-b74e6a8f4d59" />



**Takeaways:**
- Lots of interesting patterns here. It almost looks like 2-layer flow of temperature in difference between lap 1 and lap 2 at the entrance, back bay, and towards the end of the northern length of the cove (towards the mouth of the cove). Is it possible these could be fronts coming in/going out on the top layer??
- I am particularly intrigued by the mixed increasing and decreasing happeneing in the North End. Is this a real signal? HArd to say...
- Again, like salinity, in the difference between lap 1 and lap 2 the major change in temperature is at the surface. Either at the 5m depth mark or the mixed layer.
  
- ***The start of the entrance is an interesting place. This is where the most change happens for both temperature and salinity. Could this be a region of interest/focus of sampling? looking at Dakota's animations from a few weeks ago the water does come through this area first. I have a funny gut feeling about this spot.***

- Similar to salinity, the difference in temperature between the second and third laps is negative, meaning it decreases from the second lap to the third. Maybe the water is not mixed as much in the third lap?
- The exception to this is that we get the increasing difference in temperature at the surface at the entrance and towards the end of the northern length (which is, esentially, the northern part entrance). There is also a little bit of this in the end of the back bay. 


#### DO concentration

**First the profiles.**

<img alt="Figure 5. DO concentration profiles in each lap and each section of the laps" src="https://github.com/user-attachments/assets/5def6d2e-8c85-4b94-8c66-006c1dbdf47e" />


**Takeaways:**

- What pulls me the most from these plots is that it is clear there is a low-DO intrusion from 10-20m depth *in the bay*. Anything shallower than this has higher DO concentration and anything lower than this also has higher DO concentration. This is so odd!! Also this pattern is not found at the entrance in any of the laps.

- Generally, there is a lot more DO at the surface! Even so, the rest of the water column all throughout the cove is pretty poorly oxygenated.


**Now the delta plots.**

<img alt="Figure 6. Percent difference in DO concentrations between sequential laps" src="https://github.com/user-attachments/assets/150a01e1-be57-42e9-9a1f-964bd1f1c082" />



**Takeaways:**

- Most glaringly, the largest change in DO concentration is an increase from lap 1 to lap 2 at the end of the southern end of the cove at depth. Maybe the flood brought oxygenated water in at depth? Wouldn't we see this elsewhere in these plots, though?
- There is a lot of overall change in DO concentration between the 2nd and 3rd laps. For instance in the southern length almost the whole water column is changed, either increasing or decreasing.
- Interestingly, the decrease in DO concentration between laps 2 and 3 in the southern length occurs in the 10-20m band where we see the low DO intrusions.... The same this happens in the northern length. The increase and decrease in DO is strongest in the 10-20m below the surface.


## Overall thoughts

- Let's watch out for the northern end of the entrance to the cove! Things are happening there.
- The back bay is also an important place to watch.
- The 10-20m low DO thing is strange. Can we make sure to capture these depths with our future sampling?


