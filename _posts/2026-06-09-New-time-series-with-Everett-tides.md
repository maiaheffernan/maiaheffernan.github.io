# Looking at time series with Everett tidal data

As I discussed in my other blog post today, the Penn Cove NOAA tide data do not have harmonic constituents and only have data for the high and low tides. Alex suggested using the Everett tide data until we get detailed pressure readings from the Duo at the bottom of one of the SWIFT moorings. I will do this now!

First, I compared the continuous tide data from Everett through the entire month of May to the high and low tide data from Penn Cove in the same time period. I wanted to see if they are comparable locations since Penn Cove is farther north than Everett and has a weird structure which might affect tidal propogation.

<figure>
  <img src="/_figures/EverettVsPenncove_tides.png" alt="Description of image">
  <figcaption>Figure 1. Comparison of the tides from the NOAA Everett tide gauge (station # 9447659) and Penn Cove (station # 9447929) tide gauge. These datasets are for the entire month of May, 2026 and are reported in MLLW. </figcaption>
</figure>
<br><br>

It looks like the timing of the highs and lows match up pretty well. If you look closesly you will see that the Penn Cove station highs and lows are slightly behind the Everett station. Also, the Penn Cove highs tend to be higher than the Everett highs, and the lows are sometimes lower and sometime higher at Penn Cove. For instance, the high on May 13 is at 09:24 in Everett and has a tidal elevation of 3.23m whereas the high in Penn Cove is not until 09:39 on the same day and the tidal elevation is 3.44m. Though it is not perfect, this is good enough for using in the initial time series of salinity, temperature, and DO from the SWIFT telemetry.

On to the updated plots:


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
  <figcaption>Figure 2. Tides, salinty, ane temperature at wire walker south. Note this data has only been lightly QC'd and the tidal data is from Everett. </figcaption>
</figure>
<br><br>



### LoveJoy north

<figure>
  <img src="/_figures/PennCove_LoveJoy_north_TidetempSalDO.png" alt="Description of image">
  <figcaption>Figure 3. Tides, salinty, ane temperature at LoveJoy north. Note this data has only been lightly QC'dand the tidal data is from Everett. </figcaption>
</figure>
<br><br>



### LoveJoy south

<figure>
  <img src="/_figures/PennCove_LoveJoy_south_TidetempSalDO.png" alt="Description of image">
  <figcaption>Figure 4. Tides, salinty, ane temperature at LoveJoy south. Note this data has only been lightly QC'd and the tidal data is from Everett. </figcaption>
</figure>
<br><br>




### Inner north

<figure>
  <img src="/_figures/PennCove_Inner_north_TidetempSalDO.png" alt="Description of image">
  <figcaption>Figure 5. Tides, salinty, ane temperature at inner north. Note this data has only been lightly QC'd and the tidal data is from Everett. </figcaption>
</figure>
<br><br>

### Inner south

<figure>
  <img src="/_figures/PennCove_Inner_south_TidetempSalDO.png" alt="Description of image">
  <figcaption>Figure 6. Tides, salinty, ane temperature at inner south. Note this data has only been lightly QC'd and the tidal data is from Everett. </figcaption>
</figure>
<br><br>
