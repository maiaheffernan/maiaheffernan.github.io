# A detailed look into the main figure for my PECS poster for 2026


As of right now, the main thing I want to look at with this figure are the relationships between the tides, stratification, bottom DO levels, and water velocities. I am trying to explain how the stratification is primarily driven by the tides bringing fresh water into the cove from the Skagit and how this affects DO, and how velocity is also affected by the tides. 


I have three time scales to look at:
- A full time series from May to July (which has a lot of weird and missing data, this will be fixed to look better!)
- A time series of just June to July
- A time series of two tidal cycles to see small-scale effects

Please note that the stratification data comes from LoveJoy north, the bottom DO data comes from LoveJoy north and LoveJoy south, and the velocity data is from LoveJoy north.


### Full time series

<figure>
  <img src="/_figures/PECS_timseries_MayJul.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 1. Time series of tidal elevation, stratification, bottom DO concentrations, and velocity. Stratification is calculated as the different between top and bottom salinity measurements at LoveJoy north. The velocity data is also from LoveJoy north. The tide data is from a pressure sensor on the Inner south mooring but is calculated as η = H - H_mean. The bottom DO data is from both LoveJoy north and LoveJoy south. </figcaption>
</figure>
<br><br>

As we can see there are some large gaps in the data and I am trying to figure out why the tidal time series looks weird in May to June. Any suggestions to make this look nicer are appreciated!

From this high-level time scale there are a few trends we can pick out:

1. Bottom oxygen levels steadily decrease over time and even become hypoxic. LoveJoy south becomes hypoxic before LoveJoy north.
2. At LoveJoy north the velocity is predominantly westward, which is consistent with the CCW circulation pattern we have observed in the cove.
3. There are large changes in stratification on small time scales! I am thinking this is because of how shallow the bay is and how prominent the fresh water inflow is from the Skagit. More detail on this in the following plots.


### Zooming in on June to July


<figure>
  <img src="/_figures/PCES_timeseries_JunJul.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 2. Time series of tidal elevation, stratification, bottom DO concentrations, and velocity for only the month of June. Stratification is calculated as the different between top and bottom salinity measurements at LoveJoy north. The velocity data is also from LoveJoy north. The tide data is from a pressure sensor on the Inner south mooring but is calculated as η = H - H_mean. The bottom DO data is from both LoveJoy north and LoveJoy south. </figcaption>
</figure>
<br><br>

At this level we can start to see the impact of the tidal forcing in the system. Here are some takeaways from that:

1. During the first spring tide, there are large jumps in stratification and bottom DO concentrations that seem to coincide. We can really see here that increases in stratification correspond to decreases in DO concentrations. Similarly, large decreases in stratification coincide with large increases in bottom DO levels.
2. During the first spring tide we can also see that the surface eastward flowing velocity at LoveJoy north, which corresponds to the high, low, and small ebb and flood periods, extends much deeper into the water column than it does for the neap tides and even for the following spring tide. Large, strong tides drive strong, deep eastward flows.
3. During the neap tide, we see that stratification generally decreases (though there are of course still variations with the tide). Similarly, DO concentrations remain pretty steady. Also at this time the eastward surface velocities do not protrude as deeply into the water column and at peak neap almost fully disappear. The changes in stratification, DO levels, and velocity patters between the spring and the neap tides highlight how the tide is the main source of changes in density in the cove. This then affects flow and oxygen levels. 
4. What is really interesting is that in the second spring tide time block, even though the fluctuations in stratification pick up again, the DO levels begin to decrease. The fluctuations in DO at LoveJoy south are also a lot less dramatic. We can really begin to see here how the seasonal-level forcing begins to outweigh the spring/neap and tidal forcing on dissolved oxygen levels. *(Maybe there is a cool frequency or wavelet analysis somewhere down the line here??)*
5. Also interestingly, the eastward surface velocity at LoveJoy north does not reach as deep into the water column in the second spring cycle than it does in the first spring cycle.


### Zooming in to two tidal cycles


This is where we can really start to see the granularity of the relationships between the tides, stratification, bottom DO levels, and velocity.


<figure>
  <img src="/_figures/PECS_timeseries_oneDay.png" alt="Description of image">
  <figcaption class="fig-caption"> Figure 3. Time series of tidal elevation, stratification, bottom DO concentrations, and velocity for only the month of June. Stratification is calculated as the different between top and bottom salinity measurements at LoveJoy north for two tidal cycles. The velocity data is also from LoveJoy north. The tide data is from a pressure sensor on the Inner south mooring but is calculated as η = H - H_mean. The bottom DO data is from both LoveJoy north and LoveJoy south. </figcaption>
</figure>
<br><br>

There are lots of patterns to see here, so I am going to walk through it by main tidal stage.

1. Major flood
- There is a LARGE increase in stratification during the flood. Notice that this corresponds to a period of low bottom DO at both LoveJoy moorings.
- The entire water column at LoveJoy north is flowing westward.

2. High/minor ebb
- There is a steady decrease in stratification and an increase in bottom DO at both LJN and LJS. Interestingly, at LJN, there is a big jump in bottom DO that coincides with a large dip in stratification at that same location.
- Here we see the two-layer flow come into play with eastward velocity at the surface and westward velocity at depth. The sheared layer is at 10m depth.

3. Small low tide
- This is where we see the BIG jump in bottom DO at LJS and a big-ish jump in bottom DO at LJN. Something that might be missing here is the wind. Maybe since it is shallower the wind is able to stir up the water column more? The stratification is not at its lowest but it is close, so I think there is another forcing here that I am not accounting for in the current plot.

4. Minor flood/small high
- There is an interesting decrease in bottom DO at LJN here. Numerically it is less than 1 mg/L, and I am not quite sure what might be causing it. Maybe there was a big fish nearby at this time (I am only partially kidding)?
- There is a weakening of the surface eastward velocity here. This corresponds with the lowest stratification levels. Maybe there is something there.

5. Major ebb
- We are set up with low stratification and high DO values and a small eastward surface velocity.

6. Lower low
- It is a bit stagnant here, but it looks to be the beginning of the decrease in DO concentrations.
- Most of the water column is west except for maybe a SMALL eastward velocity at depth? I am not totally convinced of this, but if you look this pattern also shows up in the previous lower low and the next lower low. If it is real it would be so crazy!


We then see all these same patterns the following tidal cycle.

**The big takeaways here:**
- Increase in stratification at LJN during the major flood of the day which corresponds to a decrease in bottom DO at both LJN and LJS.
- Overall a decrease in stratification = an increase in DO
- The velocity at LoveJoy north is all west through the entire water column until the flood which creates a 2-layered system with a sheared layer at around 10m.


### Next steps

- Maybe plot wind and flow at LoveJoy south to make that comparison?
- The other plots on my poster will dive more into the spatial differences in velocity at all the moorings.
- Make the poster!





5. Major ebb


