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


<br><br>
<br><br>

## The soloT sensors

<br><br>
<figure>
  <img src="/_figures/solotT_Temp_cleaned_AugSep2026.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 5. Median-filtered soloT temperature. </figcaption>
</figure>
<br><br>

<br><br>
<br><br>


## RBR Duo temp/pres sensors


### Temperature
<br><br>
<figure>
  <img src="/_figures/Duo_temp_timeseries_cleaned_AugSep2026.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 5. Median-filtered RBR Duo temperature data. </figcaption>
</figure>
<br><br>

<br><br>

### Pressure


<br><br>
<figure>
  <img src="/_figures/Duo_pre_timeseries_cleaned_AugSep2026.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 6. Median-filtered RBR Duo pressure data. </figcaption>
</figure>
<br><br>

<br><br>
<br><br>


## YSI CTD timeseries


### Salinity

<br><br>
<figure>
  <img src="/_figures/YSI_Salinity_timeseries_cleaned_AugSep2026.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 7. Median-filtered YSI 600LS Sonde CTD salinity data. </figcaption>
</figure>
<br><br>
<br><br>


### Temperature

<br><br>
<figure>
  <img src="/_figures/YSI_Temp_timeseries_AugSep2026.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 8. Median-filtered YSI 600LS Sonde CTD temperature data. </figcaption>
</figure>
<br><br>


## Cleaned transect CTD data






