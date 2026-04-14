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
- Back bay north: Flood 
- LoveJoy north: Flood
- Wire walker north: Flood becoming slack

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



All data collection in lap 2 occured during the flood. The final reading at the wire walker north site almost borders the slack tide if we take the convenetion that slack tide is about 30 minutes on either end of the high and low tide. Interestingly, there are not very strong velocities in either the east/west or the north/south profiles. There is a lot of noise in the bottom few bins from the ADCP that even the one standard deviation cutoff did not exclude. Despite this I still don't fully trust these values so I am going to assume they are noise even though they are a few meters above the bed. 

Similar to what we saw during the ebb, the velocity on the south length of the cove leaves at the surface and comes in at depth. The fact that this occurs at both the ebb and the flood makes me confident in the circulation pattern that Dakota's plots show (I was already confident, but I am even more so now). This pattern does not make me think that the low DO water is being brought out at depth from the inner bay, though. The velocities at 15-20 meters are heading west, not east, and we do not see a DO minimum at the surface that might be advected from the eastward velocities (obviously, for both density and surface mixing reasons).

The north/south velocities are also very stagnant during this flood period. This is similar to the north/south velocity profiles during the peak ebb. It seems like the east/west velocitiy signals dominate during the transition tides.

#### Now the CTD profiles

**Dissolved oxygen in lap 2**

<figure>
  <img src="/_figures/DO_lap2_subplots.png" alt="Description of image">
  <figcaption>Figure 11. Dissolved oxygen values at each mooring location in lap 2.</figcaption>
</figure>



Honestly the DO profiles did not change much between this lap and the last lap. They have the same general shapes and there is still hypoxia. I am not too surprised, honestly, because drastic changes in DO levels on a tidal stage basis in the same day would be a little ridiculous.
There is not much to say about how the velocities might impact the DO levels because they are so small for this flood period.




**Salinty in lap 2**


<figure>
  <img src="/_figures/salinity_lap2_subplots.png" alt="Description of image">
  <figcaption>Figure 12. Salinity values at each mooring location in lap 2.</figcaption>
</figure>


We can kind of see the intrusion of what I assume to be the Skagit River water in the wire walker north site as that fresh layer sits at about 5 meters depth. It is hard to compare this to the previous lap because a lot of the data at the surface was removed in the CTD cleaning process.



**Temperature in lap 2**


<figure>
  <img src="/_figures/temperature_lap2_subplots.png" alt="Description of image">
  <figcaption>Figure 13. Dissolved oxygen values at each mooring location in lap 2.</figcaption>
</figure>


The temperature profiles here look similar to those in lap 1. There is no meaningful change here except for maybe the obvious Skagit surface layer at the wire walker north site.


### Lap 3

The tidal stages for this lap were :  
- Wire walker south: Ebb
- LoveJoy south: Low/slack
- Back bay south: Slack/ebb
- Back bay north: Ebb
- LoveJoy north: Ebb
- Wire walker north: Ebb

#### First the velocities

**East/West**

<figure>
  <img src="/_figures/lap3_EastWest_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 14. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean. Note that the timestamp for WWN and WWS is the same because this was the closest reading to both of these locations.</figcaption>
</figure>

**North/South**


<figure>
  <img src="/_figures/lap3_NorthSouth_allmooringsSubplots_LINKED.png" alt="Description of image">
  <figcaption>Figure 15. Average velocity profiles from 5 nearest readings for each mooring location. Shaded region shows standard deviation around the mean. Note that the timestamp for WWN and WWS is the same because this was the closest reading to both of these locations.</figcaption>
</figure>



It feels like this is where things get a bit interesting. Note that the timestamp for WWN and WWS profiles is the same. It is likely that the closest value to both of these sites is the same, but I will go back and double check the code to make sure it is doing the correct thing.

This lap contains the high tide, the biggest ebb of the day, and the biggest tidal change of the day overall. It makes sense that we see some more dynamic velocity profiles. 

Contrary to what we have seen above, the LoveJoy south and Inner bay south moorings show more dynamic profiles even though this occur during the low and slack/initially ebbing tides, respectively. The north/south velocity profiles are pretty stagnant at this time, as I have come to expect when the east/west velocities are large.

What seems counterintuitive is that during the ebb portion of the lap-- which occured when we were in the northern length of the cove, so the top three panels of the plots and the WWS plot-- the east/west velocities in the inner bay and at LoveJoy are small and the north/south velocities are really large and heading primarily north throughout the entire water column. If the going hypothesis is that water enters the cove in the north and leaves in the south it is interesting that at the northern sites the velocity is heading primarily to the north and only a bit to the east. Not sure what is going on here.


#### Now the CTD profiles

**Dissolved oxygen in lap 3**

<figure>
  <img src="/_figures/DO_lap3_subplots.png" alt="Description of image">
  <figcaption>Figure 16. Dissolved oxygen values at each mooring location in lap 3.</figcaption>
</figure>


The profiles all look similar to what they were before. Note that what looks like a reduction inhypoxia at the WWS site in comparison to previous laps is actually a false pattern because this is the same DO profile as the WWN site which shows a consistent trend through the different laps.



**Salinty in lap 3**


<figure>
  <img src="/_figures/salinity_lap3_subplots.png" alt="Description of image">
  <figcaption>Figure 17. Salinity values at each mooring location in lap 3.</figcaption>
</figure>

We can see that the increased fresh layer (supposedly) from the Skagit River that was present during the flood is no longer there on the ebb. This makes sense but is cool to see!



**Temperature in lap 3**


<figure>
  <img src="/_figures/temperature_lap3_subplots.png" alt="Description of image">
  <figcaption>Figure 18. Dissolved oxygen values at each mooring location in lap 3.</figcaption>
</figure>





## Takeaways 

- I really did not find much in the velocities that help tell a story about the DO minimum.
- Maybe I am conflating this minimum. If you look at the profiles at the DO "minimum" finger at depth of 15-20m, there is really only a change of about 1 mg/L of DO from the surrounding depths. The maximum DO concentration is about 9 mg/L, so this change is only 1/9th of the total range. Maybe these plots make it look much more drastic than it is and there is actually no meaningful DO minimum at depth. Hypoxia/near hypoxia really has the same biological implications everywhere. The more I look at the patterns, the more I think that I am barking up a non-existent tree.
- The tradeoff of north/south and east/west velocity magnitudes at different tidal stages is interesting. I will be curious to see how circulation changes on larger time scales from the mooring deployment. I think the larger story is here!







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














