# Plots and analysis of velocity, salinity, temperature, and DO at each lap and mooring location

I pulled the velocity, temperature, salinity, and dissolved oxygen profiles that were nearest to each planning mooring location. To do this, I found the closest lat/lon position to each mooring location from the ADCP track. I found the closest CTD cast time to each ADCP ensemble time and assigned the corresponding ADCP lat/lon value to that CTD cast.

The main plots of velocity and the CTD profiles are given for each lap below. At the bottom of the document are the TS plots colored by dissolved oxygen. They have color maps from both the "thermal" pallette in cmocean as well as the hypoxia colormap so that we can see when they are hypoxic. 

The main reason for doing this analysis has been to determine what might be causing the dissolved oxygen minimum at 15-20 meters throughout the water column. The main plot that has inspired this was the one with the profiles that "walked" west ot east throughout Penn Cove.






**First the north length**


<figure>
  <img src="/_figures/TempSalDO_marchingProfiles_northlength.png" alt="Description of image">
  <figcaption>Figure 1. Dissolved oxygen, temperature, salinity profiles along northern length of Penn Cove.</figcaption>
</figure>




**South length**


<figure>
  <img src="/_figures/TempSalDO_marchingprofilesSouthLength.png" alt="Description of image">
  <figcaption>Figure 2. Dissolved oxygen, temperature, salinity profiles along southern length of Penn Cove.</figcaption>
</figure>

## New plots

I have pulled together the profiles of temperature, dissolved oxygen, salinity, and east/west and north/south velocities at the planned mooring locations for each lap. My hope is that this gives us some insight into how tidal processes might play into the trends we see.

First, I want to bring up the plot of the lap sampling intervals on the tide chart.

<figure>
  <img src="/_figures/DecemberCruise2025_tideLaps.png" alt="Description of image">
  <figcaption>Figure 3. Tidal stage predictions from the NOAA Penn Cove station for December 4, 2025. The high of 3.73m occurred at 05:12, the low of 2.40m occurred at 10:06, the second high of 3.76m occurred at 15:04, and the second low of -1.18m occurred at 22:20. Time stamps are in PST. Tide window 1, detailed below, is outlined in red, tide window 2 is outlined in gold, and tide window 3 is outlined in purple.</figcaption>
</figure>



### Lap 1 

A quick note on the velocities. I did some initial cleaning of the individual profiles by removing values that were outside one standard deviation from the mean velocity value for each ensemble. There was a lot of scatter in the bottom velocities that were most definitely from bed interference, so removing anamolously high values seemed like the logical thing to do. I started with removing points that were only two standard deviations away from the mean, but that made no change to the profiles so I then applied the stricter tolerance of one standard deviaiton after that. 




For the velocity plots below for the first lap, here are the tidal stages each measurement was taken at. Note that WWS, the bottom right corner panel, was measured first in the sampling track we took.

- Wire walker south: Ebb
- LoveJoy south: Ebb
- Back bay south: Ebb
- Back bay north: Slack (assuming slack occurs about 30 minutes before the high or low)
- LoveJoy north: Low
- Wire walker north: Slack, entering the flood



**East/West**

<figure>
  <img src="/_figures/lap1_EastWest_allmooringSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 4. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean. Positive values are east, negative values are west. Times are in UTC.</figcaption>
</figure>




**Here are the north/south velocities at the same times.**





<figure>
  <img src="/_figures/lap1_NorthSouth_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 5. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean. Positive it north, negative is south. Times are in UTC.</figcaption>
</figure>




Some initial takeaways:

During the ebb, which encompasses the bottom three panels, the east/west velocities in the southern part of Penn Cove are strong and show water leaving the cove at the surface and an opposite inflow into the cove at depth. This is interesting because this is the traditional estuarine exchange pattern but there is no river at the head of the bay forcing this mechanism. During the ebb, the north/south velocities are pretty stagnant. Thinking back to Dakota's plot of the velocity arrows overlayed on the DO heatmap in Penn Cove, I recall that the est/west component of velocity is particularly strong. I realize those are tidally-averaged velocities, but maybe we really see that pattern when the water is ebbing in the cove. 

Conversely, during the slack and low tides, the top three panels, the east/west velocities are very small and the north/south velocities are larger; water primarily flows north at the surface and south at depth. This does not make as much sense to me based on Dakota's plots and the general consensus of counter-clockwise flow in Penn Cove. There is strong southward flow, but it just occurs deeper in the water column. I am a bit confused here. 




I am going to break down the velocity, CTD, and TS plots for each mooring in lap 1 and provide the TS plot for each mooring location in lap 1.


**Dissolved oxygen in lap 1**

<figure>
  <img src="/_figures/DO_lap1_subplots.png" alt="Description of image"
    style="width: 80%;">
  <figcaption>Figure 6. Dissolved oxygen values at each mooring location in lap 1.</figcaption>
</figure>




One of the theories I have about the dissolved oxygen minimum is that the low DO from around 15-20 meters in the back bay gets advected out through the rest of the bay at the same depth, which causes this minimum. There is nothing in the east/west velocity signal that implies this process. In fact at that depth the east/west velocities are stagnant around zero or are heading west. Given that this lap encompassed the ebb and slack/low tide, I would think that this is when the eastward velocity signal would be strongest.

What is interesting to me though, is that the velocity at this depth generally heads south from the northern sites. This is particularly strong in the inner bay north site. Maybe that southward velocity brings low DO with it that then gets circulated aroung the south end of the cove. This is another process we have talked about as a plausible explanation for the hypoxic conditions present in the south part of the bay, so maybe this is a trace of that here.

Another thought related to the DO minimum related to the east/west velocities. During the ebb in lap 1 the velocities in the southrn length of the bay head west. If you look at the TS plot for WWS you can see that just around the 20ish isopycnal there is hypoxia at depth in the water column. In fact, there is hypoxia at depth for all the TS plots. Either this hypoxia has been persistent, which we would have no way of knowing, or the hypoxic mass gets moved around and does not necessarily stem from the back bay.


**Salinty in lap 1**


<figure>
  <img src="/_figures/salinity_lap1_subplots.png" alt="Description of image"
    style="width: 80%;">
  <figcaption>Figure 7. Salinity values at each mooring location in lap 1.</figcaption>
</figure>


**Temperature in lap 1**


<figure>
  <img src="/_figures/temperature_lap1_subplots.png" alt="Description of image"
    style="width: 80%;">
  <figcaption>Figure 8. Dissolved oxygen values at each mooring location in lap 1.</figcaption>
</figure>





### Lap 2

The tidal stages for this lap were
- Wire walker south: Flood
- LoveJoy south: Flood
- Back bay south: Flood
- Back bay north: Flood becoming slack
- LoveJoy north: Flood
- Wire walker north: Flood

#### First the velocities

**East/West**

<figure>
  <img src="/_figures/lap2_EastWest_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 9. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean.</figcaption>
</figure>

**North/South**


<figure>
  <img src="/_figures/lap2_NorthSouth_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 10. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean.</figcaption>
</figure>



#### Now the CTD profiles

**Dissolved oxygen in lap 2**

<figure>
  <img src="/_figures/DO_lap2_subplots.png" alt="Description of image">
  <figcaption>Figure 11. Dissolved oxygen values at each mooring location in lap 2.</figcaption>
</figure>


**Salinty in lap 2**


<figure>
  <img src="/_figures/salinity_lap2_subplots.png" alt="Description of image">
  <figcaption>Figure 12. Salinity values at each mooring location in lap 2.</figcaption>
</figure>


**Temperature in lap 2**


<figure>
  <img src="/_figures/temperature_lap2_subplots.png" alt="Description of image">
  <figcaption>Figure 13. Dissolved oxygen values at each mooring location in lap 2.</figcaption>
</figure>




### Lap 3

The tidal stages for this lap were :  
- Wire walker south: Ebb
- LoveJoy south: Low/slack
- Back bay south: Slack
- Back bay north: Ebb
- LoveJoy north: Ebb
- Wire walker north: Ebb

#### First the velocities

**East/West**

<figure>
  <img src="/_figures/lap3_EastWest_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 14. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean.</figcaption>
</figure>

**North/South**


<figure>
  <img src="/_figures/lap3_NorthSouth_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 15. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean.</figcaption>
</figure>




#### Now the CTD profiles

**Dissolved oxygen in lap 3**

<figure>
  <img src="/_figures/DO_lap3_subplots.png" alt="Description of image">
  <figcaption>Figure 16. Dissolved oxygen values at each mooring location in lap 3.</figcaption>
</figure>


**Salinty in lap 3**


<figure>
  <img src="/_figures/salinity_lap3_subplots.png" alt="Description of image">
  <figcaption>Figure 17. Salinity values at each mooring location in lap 3.</figcaption>
</figure>


**Temperature in lap 3**


<figure>
  <img src="/_figures/temperature_lap3_subplots.png" alt="Description of image">
  <figcaption>Figure 18. Dissolved oxygen values at each mooring location in lap 3.</figcaption>
</figure>









## The TS plots for each lap

The TS plots are broken up for each location. They are plotted with both the "thermal" color pallette from cmocean and the hypoxia color pallette from cmocean.


### Lap 1

#### Wire walker south

<figure>
  <img src="/_figures/WWS_lap1_TSplot.png" alt="Description of image">
  <figcaption>Figure 19. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/WWS_lap1_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 20. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### LoveJoy south

<figure>
  <img src="/_figures/LoveJoyS_lap1_TSplot.png" alt="Description of image">
  <figcaption>Figure 21. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/LoveJoyS_lap1_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 22. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>





#### Inner bay south

<figure>
  <img src="/_figures/InnerS_lap1_TSplot.png" alt="Description of image">
  <figcaption>Figure 23. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/InnerS_lap1_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 24. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### Inner bay north


<figure>
  <img src="/_figures/InnerN_lap1_TSplot.png" alt="Description of image">
  <figcaption>Figure 25. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/InnerN_lap1_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 26. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### LoveJoy north


<figure>
  <img src="/_figures/LoveJoyN_lap1_TSplot.png" alt="Description of image">
  <figcaption>Figure 27. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/LoveJoyN_lap1_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 28. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### Wire walker north

<figure>
  <img src="/_figures/WWN_lap1_TSplot.png" alt="Description of image">
  <figcaption>Figure 29. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/WWN_lap1_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 30. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




### Lap 2



#### Wire walker south

<figure>
  <img src="/_figures/WWS_lap2_TSplot.png" alt="Description of image">
  <figcaption>Figure 31. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/WWS_lap2_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 32. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### LoveJoy south

<figure>
  <img src="/_figures/LoveJoyS_lap2_TSplot.png" alt="Description of image">
  <figcaption>Figure 33. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/LoveJoyS_lap2_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 34. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### Inner bay south

<figure>
  <img src="/_figures/InnerS_lap2_TSplot.png" alt="Description of image">
  <figcaption>Figure 35. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/InnerS_lap2_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 36. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>



#### Inner bay north


<figure>
  <img src="/_figures/InnerN_lap2_TSplot.png" alt="Description of image">
  <figcaption>Figure 37. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/InnerN_lap2_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 38. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### LoveJoy north


<figure>
  <img src="/_figures/LoveJoyN_lap2_TSplot.png" alt="Description of image">
  <figcaption>Figure 39. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/LoveJoyN_lap2_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 40. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### Wire walker north


<figure>
  <img src="/_figures/WWN_lap2_TSplot.png" alt="Description of image">
  <figcaption>Figure 41. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/WWN_lap2_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 42. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>





### Lap 3



#### Wire walker south

<figure>
  <img src="/_figures/WWS_lap3_TSplot.png" alt="Description of image">
  <figcaption>Figure 43. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/WWS_lap3_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 44. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### LoveJoy south

<figure>
  <img src="/_figures/LoveJoyS_lap3_TSplot.png" alt="Description of image">
  <figcaption>Figure 45. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/LoveJoyS_lap3_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 46. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### Inner bay south

<figure>
  <img src="/_figures/InnerS_lap3_TSplot.png" alt="Description of image">
  <figcaption>Figure 47. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/InnerS_lap3_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 48. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>



#### Inner bay north


<figure>
  <img src="/_figures/InnerN_lap3_TSplot.png" alt="Description of image">
  <figcaption>Figure 49. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/InnerN_lap3_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 50. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### LoveJoy north


<figure>
  <img src="/_figures/LoveJoyN_lap3_TSplot.png" alt="Description of image">
  <figcaption>Figure 51. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/LoveJoyN_lap3_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 52. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>




#### Wire walker north


<figure>
  <img src="/_figures/WWN_lap3_TSplot.png" alt="Description of image">
  <figcaption>Figure 53. TS plot colored by dissolved oxygen.</figcaption>
</figure>

<figure>
  <img src="/_figures/WWN_lap3_TSplot_hypoxiaColors.png" alt="Description of image">
  <figcaption>Figure 54. TS plot colored by dissolved oxygen with the hypoxia colormap.</figcaption>
</figure>














