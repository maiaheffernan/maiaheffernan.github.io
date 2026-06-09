# Timeseries with a tidal reconstruction using UTide

One of the things I have focused on this week is reconstructing the tidal signal using velocity data from the SWIFTs. Believe it or not there are no great tide gages near Penn Cove that minute-to-minute predictions or tidal harmonics. The closest gage that have this are in Everett and Snee Oosh Point, which is in the northern part of the Whidbey Basin. So, until we recover the RBR temp/depth Duo that is on the bottom of one of the SWIFT v4 moorings and use the high-resolution pressure values to give the tidal signal, I am using UTide to pull out the tidal constituents and velocities from the Wire Walker south mooring. I chose this mooring because it is likely less effected by any weird processes in Penn Cove that might bias the tidal reconstruction to an unreasonable/incorrect value. Also, since it is slightly outside the cove and to the south and we assume that the tide propogates up and down through Saratoga Passage I am thinking that it will be more representative of the greater area. 

Given all that, the reconstruction is definitely not perfect. The UTide function requires that you put in u and v velocity vectors. Working with ADCP data, the main question becomes how do I shrink down my matrix of velocity values from all the depth bins into one velocity vector. There are a few options: 1) You can take a depth-averaged velocity through the water column, 2) you can choose one depth bin to use, 3) you can average a few depth bins together to get a representative sample. I ended up choosing option 3. I did this primarily because I don't think the depth-averaged velocity makes the most sense here because I have not finished de-spiking the ADCP data and there are likely very incorrecty values near the surface and the bed (and potentially in the water column as well). These would skew the depth-averaged value. I also did not feel comfortable choosing a single depth bin because which would I choose to be representative of the water column? It is hard to know. So, I ended up average about 8 bins from the middle of the water column. The cell sizes on the ADCPs are 0.5m and start at 0.35m below the surface, so I ended up averaging from 6.35 to 10.35m from the surface. I chose this range from a diagnostic plot in which this band seemed to be the least spiky and showed some switches in velocity direction and magnitude which made me think it was resolving the tidal affects well. Below is that diagnostic plot, the black box indicates the depth bins I chose to average for the UTide reconstruction.


<figure>
  <img src="/_figures/UTide_diagnosticPlot.png" alt="Description of image">
  <figcaption>Figure 1. Diagnostic plot from SWIFT 09 showing the velocities in time and depth from the Signature 1000. The y-axis shows the depth from the surface. Note that the cell sizes for the ADCP are 0.5m starting at 0.35m below the surface. The black box indicates the depth bins I chose to average for the UTide reconstruction. This data has not been QC'd. </figcaption>
</figure>

<br><br>


I am not sure if this was the best decision but it is what I have at the moment. Moving on to how this turned out.

## Tides, salinity, temperature, and DO timseries

I reconstructed the tides mainly so that I could look at tidal timeseries, so that is what I have below. This data is from the daily telemetry values that get sent from all the SWIFTs. Note that SWIFTS 09 and 18 (WWS and WWN) do not have DO sensors at the surface. Also, a few of the SWIFTs were collecting and sending only sparse data so the timeseries below do not match up with each other, unfortunately. Alex dK and I visited Penn Cove last Friday to fix some of these SWIFT issues, so hopefully future telemetry installments will be more complete. Note all the tidal reconstruction is from SWIFT 09 (WWS) and this data spans from May 25th to June 3rd.


### Wire walker north


<figure>
  <img src="/_figures/PennCove_Wire_walker_north_TidetempSalDO.png" alt="Description of image">
  <figcaption>Figure 2. Tides, salinty, ane temperature at wire walker north. Note this data has only been lightly QC'd. </figcaption>
</figure>

<br><br>


Looking at the tidal velocities, it appears that at low tides there is a jump in tidal velocity. This seems incorrect since the UTide function is ostensibly only pulling out tidal velocities, but maybe there is a non-tidal velocity artifact here that is causing the function to think that there is something happenening to the tidal velocities at this time? I am not sure. Whatever it is, we can see that the tidal reconstruction is a bit rough. This makes some sense given I am using velocities and not sea surface elevations, but supposedly the function is agnostic to this. Hard to say, I think I might have to go back to the drawing board with UTide. 

Despite that, there are some interesting general signals here. The salinity tends to drop and the temperature tends to peak at the onset of the largest flood of the day. This makes sense given our hypothesis that the Skagit River water gets pushed into the cove from the north side. I would expect this to occur more vivedly on the flood as water rushes into Penn Cove. Before these drops the salinity is usually at its highest, which makes sense given that the water is pulled out of Penn Cove which hypothetically advects the Skagit River water out with it. Similarly, we see that after the dip in salinity it quickly begins to rise again and peak after the major flood during high tide. Could this be rapid mixing as the tide comes in??


### Wire walker south


<figure>
  <img src="/_figures/PennCove_Wire_walker_south_TidetempSalDO.png" alt="Description of image">
  <figcaption>Figure 2. Tides, salinty, ane temperature at wire walker south. Note this data has only been lightly QC'd. </figcaption>
</figure>


### LoveJoy north




### LoveJoy south






### Inner north



### Inner south


