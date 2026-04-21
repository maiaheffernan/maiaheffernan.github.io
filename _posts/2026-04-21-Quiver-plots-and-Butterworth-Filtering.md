# Adding to the plots from December with some quiver plots and butterworth filtering to get general processes

## Quiver plots

We talked about these plots last meeting. Plotted are the average velocities from the top 0-10m and bottom 10-20 meters in the water column at each mooring location. Note these are rough plots and definitely need more fine tuning (note the large 0.5 m/s reference arrow at the bottom). 


#### Lap 1

Tidal stages for the first lap:

- Wire walker south: Ebb
- LoveJoy south: Ebb
- Back bay south: Ebb
- Back bay north: Slack (assuming slack occurs about 30 minutes before the high or low)
- LoveJoy north: Low
- Wire walker north: Slack, entering the flood



<figure>
  <img src="/_figures/lap1_quiverPlots.png" alt="Description of image">
  <figcaption>Figure 1. Quiver plot of velocity in the first lap from the RDI Workhorse ADCP pole-mounted on the R/V Echo in December.</figcaption>
</figure>


Okay this is a rough and ready plot here, as you can see by the ridiculous size of the 0.5 m/s arrow in the bottom of the figure. Nonetheless, there are some interestin trends during the ebb and slack. In this plot, the south-end sites all occur during the ebb and the north end plots occur during the slack/low. Missing from these quivers is the Signature data from the SWIFTS-- see the next installation of these plots for that update!

- There is an interesting trend in the south sites during the slack: water exits at the surface, but enters at depth for WWS and LoveJoyS and exits at depth at Inner S. There must be some mixing of the two bottom layers at some point in the water column? **Maybe this is where the low DO comes from! The hypoxic water at depth in the southern part gets mixed up and sits at about 15-20 meters because this is where the water goes fromg being stratified at the surface to being mixed at depth (per the temperature and salinity plots). So the low DO is trapped by this stratification (...but wait, didn't Aurora or Dakota have something that disproved this stratification effect...?).**
- The northern sites: Lots of northward movement during the slack and low! This is something I noted in the profile plots last week. I think it was Alex that brought up the idea that mayeb on the ebb we create an unbalanced surface ($\eta$) from the E/W velocities that are then restored by the N/S velocities. This could be what is happening here. It is interesting that the (almost) bottom velocities go the opposite direction.
- There is hardly any bottom movement at the WWN location

#### Lap 2

Tidal stages for the second lap:

- Wire walker south: Flood
- LoveJoy south: Flood
- Back bay south: Flood
- Back bay north: Flood 
- LoveJoy north: Flood
- Wire walker north: Flood becoming slack


<figure>
  <img src="/_figures/lap2_quiverPlots.png" alt="Description of image">
  <figcaption>Figure 2. Quiver plot of velocity in the first lap from the RDI Workhorse ADCP pole-mounted on the R/V Echo in December.</figcaption>
</figure>


- The flood is a totally different story here! The southern sites' bottom velocities are stronger than the surface velocities and we see the continuation of the consistent circulation cell that leaves at the surface and enters at depth. This change in magnitude is really interesting, though.
- The northern sites: Still primarily trending north at the surface but definiely exiting the cove at the surface. It is interesting that the bottom velocities are similar to what they were during the ebb and slack and heading towards the middle of the cove-- maybe this points to the circulation pattern Dakota plotted up a while ago?
- WWN north has no surface velocity and water is entering the cove at depth? Not sure I believe this arrow, but if it is true that would be a strange process.




#### Lap 3

Tidal stages for the third lap:

- Wire walker south: Ebb
- LoveJoy south: High/slack
- Back bay south: Slack/ebb
- Back bay north: Ebb
- LoveJoy north: Ebb
- Wire walker north: Ebb



<figure>
  <img src="/_figures/lap3_quiverPlots.png" alt="Description of image">
  <figcaption>Figure 3. Quiver plot of velocity in the first lap from the RDI Workhorse ADCP pole-mounted on the R/V Echo in December.</figcaption>
</figure>


The southern sites, EXCEPT FOR WWS, are showing velocities during the slack/high and the northern sites are showing velocities during the major ebb of the day.

- The velocities at LoveJoyS and InnerS are so much smaller during the slack and high tides. This makes sense. Interestingly we do see in the inner bay that the water is leaving at depth and entering at the surface which is a reversal of what we saw in the previous plots. Maybe when not forced by strong tidal flows this is the tendency of this area? Or it is a result of something?
- The northern sites: Interesting that during the ebb the inner bay seems to have its own circulation. The surface waters get pulled down back there (and supposedly out? We do not have the data for this). The LovejoyN site shows that water is definitely leaving the cove suring the ebb (duh), but it is interesting that the surface and bottom layers are doing something totally different.
- WWN north and southare both during the ebb and we can guess that the tide definitely pulls water down Saratoga Passage as it leaves. Makes sense but is good to verify.


## Butterworth filter for the dissolved oxygen to see super high-level general trends


#### Lap 1



Tidal stages for the first lap:

- Wire walker south: Ebb
- LoveJoy south: Ebb
- Back bay south: Ebb
- Back bay north: Slack (assuming slack occurs about 30 minutes before the high or low)
- LoveJoy north: Low
- Wire walker north: Slack, entering the flood


<figure>
  <img src="/_figures/DO_lap1_subplots_Butter.png" alt="Description of image">
  <figcaption>Figure 4. Second-order lowpass Butterworth filter applied to dissolved oxygen concentrations. Sampling frequency was 1Hz, cutoff frequency was 0.03Hz. </figcaption>
</figure>



#### Lap 2

Tidal stages for the second lap:

- Wire walker south: Flood
- LoveJoy south: Flood
- Back bay south: Flood
- Back bay north: Flood 
- LoveJoy north: Flood
- Wire walker north: Flood becoming slack



<figure>
  <img src="/_figures/DO_lap2_subplots_Butter.png" alt="Description of image">
  <figcaption>Figure 5. Second-order lowpass Butterworth filter applied to dissolved oxygen concentrations. Sampling frequency was 1Hz, cutoff frequency was 0.03Hz. </figcaption>
</figure>



#### Lap 3

Tidal stages for the third lap:

- Wire walker south: Ebb
- LoveJoy south: Low/slack
- Back bay south: Slack/ebb
- Back bay north: Ebb
- LoveJoy north: Ebb
- Wire walker north: Ebb


<figure>
  <img src="/_figures/DO_lap3_subplots_Butter.png" alt="Description of image">
  <figcaption>Figure 6. Second-order lowpass Butterworth filter applied to dissolved oxygen concentrations. Sampling frequency was 1Hz, cutoff frequency was 0.03Hz. </figcaption>
</figure>

