# Time series plots from my loading in the data from the August to September deployment window


Some of these time series are cleaned and some are raw data. I will specify which is which. It changes depending on how confident I am on the cleaning procedures I came up with for each sensor. There is a lot more to do for this to formalize the cleaning, so right now I just have a few placeholders in the form of Hampel filters (moving median).




## TODO temperature and salinity


<br><br>
<figure>
  <img src="/_figures/TODO_L2_plots.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 1. TODO cleaned data. Data was cleaned using a Hampel filter (7 measurements on each end of the sample, removed anything larger or smaller than 3 standard deviations from the median). I also removed any changes in temperature greater than 0.5 deg C between samples and changes in DO heater than 0.3 mg/l between samples. Note the TODOs read every 1 minute. </figcaption>
</figure>
<br><br>



## miniDOT from the mussel rafts

### DO
<br><br>
<figure>
  <img src="/_figures/miniDOT_DO_timeseries_AugSep2026_rafts.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 2. Mussel raft miniDOT raw DO data (mg/l). The miniDOTS sample once every 10 minutes. </figcaption>
</figure>
<br><br>

### Temperature

<br><br>
<figure>
  <img src="/_figures/miniDOT_temp_timeseries_AugSep2026_rafts.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 3. Mussel raft miniDOT raw temperature data (deg C). The miniDOTS sample once every 10 minutes. </figcaption>
</figure>
<br><br>



## SeaBird moored CTD (LoveJoy south)

<br><br>
<figure>
  <img src="/_figures/SeaBird_TempSal_rawtimeseries_AugSep2026.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 4. SeaBird SeaCat19 CTD raw temperature and salinity data. The SeaBird CTD samples once every 10 minutes. </figcaption>
</figure>
<br><br>


