# Time series of raw data from May to June 2026

We completed the first monthly mooring turn around on June 23-25, 2026! There is a lot to do to look at all the data from all the sensors and the transecting data, so I am starting by just plotting time series and histograms of the raw or lightly processed data. This month is going to be a little clunky as I develop a workflow that makes sense for processing everything. In the meantime, I think it makes sense to share some cool plots here!


All I have for today so far are the CTD casts from the transects, the ADCP data from the transects, and the miniDOT data from the rafts. I have a few takeaways from these so far. 


### Transects: ADCP

A HUGE note here is that the heading is incorrect in these ADCP files so the velocities are incorrect. I will be fixing this tomorrow, but for posterity's sake I am going to put this plot in here. More to follow on this.


#### Ebb tide
<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_ebb_ENUquicklook.png" alt="Description of image">
  <figcaption>Figure 1. Ship-mounted ADCP data from the major ebb of the day in Penn Cove. Note that the heading needs to be corrected. </figcaption>
</figure>
<br><br>



<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_ebb_track.png" alt="Description of image">
  <figcaption>Figure 2. Ship-mounted ADCP track from the major ebb of the day in Penn Cove. Note that the heading needs to be corrected. </figcaption>
</figure>
<br><br>


#### Flood tide

<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_flood_ENUquicklook.png" alt="Description of image">
  <figcaption>Figure 3. Ship-mounted ADCP data from the major flood of the day in Penn Cove. Note that the heading needs to be corrected. </figcaption>
</figure>
<br><br>



<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_flood_track.png" alt="Description of image">
  <figcaption>Figure 4. Ship-mounted ADCP track from the major flood of the day in Penn Cove. Note that the heading needs to be corrected. </figcaption>
</figure>
<br><br>



I am not even going to bother trying to interpret this when the heading is incorrect. Again, this will be fixed shortly.


### CTD casts


<figure>
  <img src="/_figures/pcolor_quicklook_SalTempDO.png" alt="Description of image">
  <figcaption>Figure 5. Ship-mounted CTD tow-yo data throughout the whole day in Penn Cove. </figcaption>
</figure>
<br><br>

There are a couple interesting tidbits here:
- The fresh layer on top is really small throughout the whole day! This is kind of crazy given the spikes we have been seeing in the SWIFT surface CT data. Next step is looping that data into these profiles and getting out of pcolor space.
- There might be hypoxia at depth (assuming the initial data cleaning I did removed bad values). I set the colorbar to be a minimum t 2 mg/L so we could really see the dark blue color. I am interested to pull apart where this is and at what time. This is a next step here.



### miniDOTs

The raft miniDOTs are giving suspiciously low DO values. Alex compared to Emily Carrington's data and the almost 0 mg/L values are not correct. The accuracy on the sensors is 0.03 mg/L or 5% of the measurement (whichever is bigger), but I have a hard time believing even that because that would imply that the data is still less than 1 mg/L at some instances which seems fishy. I think I am going to check with Emily to get confirmation whether her sensors were INSIDE or OUTSIDE the rafts. This might tell us a lot. We also did a small calibration in the field where we jung the miniDOTS from the side of the boat and hung the profiling CTD next to them for 5 minutes to test the accuracy of the miniDOTs. I am looking forward to seeing what that tells us. Somthing to think about for data cleaning...


<figure>
  <img src="/_figures/miniDOT_DO_timeseries_May2026.png" alt="Description of image">
  <figcaption>Figure 6. Time series of raw DO values from the miniDOTs. </figcaption>
</figure>
<br><br>


<figure>
  <img src="/_figures/miniDOT_Temp_timeseries_May2026.png" alt="Description of image">
  <figcaption>Figure 7. Time series of raw temperature values from the miniDOTs. </figcaption>
</figure>
<br><br>


<figure>
  <img src="/_figures/miniDOT_1mDO_hist_May2026.png" alt="Description of image">
  <figcaption>Figure 8. Histogram of surface DO values in the mussel rafts. </figcaption>
</figure>
<br><br>


<figure>
  <img src="/_figures/miniDOT_7mDO_hist_May2026.png" alt="Description of image">
  <figcaption>Figure 9. Histogram of bottom DO values in the mussel rafts. </figcaption>
</figure>
<br><br>



<figure>
  <img src="/_figures/miniDOT_1mTemp_hist_May2026.png" alt="Description of image">
  <figcaption>Figure 8. Histogram of surface temperature values in the mussel rafts. </figcaption>
</figure>
<br><br>


<figure>
  <img src="/_figures/miniDOT_7mTemp_hist_May2026.png" alt="Description of image">
  <figcaption>Figure 9. Histogram of bottom temperature values in the mussel rafts. </figcaption>
</figure>
<br><br>




### Next steps:

- Plot all the raw data as time series and PDFs where is makes sense
- Correct the ADCP heading
- Start to focus in on the circulation and front stories for PECS
- Planning for next month's turnaround!

