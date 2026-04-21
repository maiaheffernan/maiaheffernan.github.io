# Bucket test results from the RBR T.ODOs, the RBR soloTs, RBR Duos, and the miniDOTS

## RBR T.ODO

These sensors measure dissolved oxygen (optical) and temperature (thermistor). I tested these on April 8, 2026. I tested two sensors at a time for two minutes each. I did this three times so there were three rounds. I did not change the water between the three rounds.

### Plots

#### Round 1

<figure>
  <img src="/_figures/Round1_plots.png" alt="Description of image">
  <figcaption>Figure 1. Temperature and dissolved oxygen in Round 1 for the T.ODO pairs.</figcaption>
</figure>



#### Round 2

<figure>
  <img src="/_figures/Round2_plots.png" alt="Description of image">
  <figcaption>Figure 2. Temperature and dissolved oxygen in Round 2 for the T.ODO pairs.</figcaption>
</figure>



#### Round 3

<figure>
  <img src="/_figures/Round3_plots.png" alt="Description of image">
  <figcaption>Figure 3. Temperature and dissolved oxygen in Round 3 for the T.ODO pairs.</figcaption>
</figure>


I am a little concerned with the DO readings between the sensors. Some of the differences between the values are within a few tenths of a mg/L, but there are a couple sensors, SN 241789 and SN 241790 (second panels in the plots) that are almost 1 mg/L different from each other. This could be pretty significant in our system. The initial accuracy of the dissolved oxygen values for these sensors should be a maximum of +/- 2µmol/L which is 0.064 mg/L. The differences in the vlaues we see here are larger than that. 


### Sampling intervals

With AA lithium iron batteries, we can choose from the following configurations:

- Sampling every 30 seconds gives a battery life of 26 days
- Sampling every 35 seconds gives a battery life of 30 days
- Sampling every 40 seconds gives a battery life of 34 days
- Sampling every 45 seconds gives a battery life of 39 days

It seems like 40 or 45 second sampling is the way to go to optimize samples and battery life. I would prefer to err on the longer side of battery life just in case something happens and we have to delay our monthly visits. 

This brings up the question of whether we want to tie everything to the same sampling interval across the entire deployment. I am not sure this is entirely possible or if it makes the most sense for resolving different processes. Any thoughts people have would be great as we have not talked about this yet!



## RBR solo Ts

I sampled these on April 15. I put 14 of these these sensors in one bucket and the other 14 sensors in the other bucket at the same time for 10 minutes. I am not totally convinced this was enough time, so I am planning to redo this test with Tia this week on Thursday.

### Plots

<figure>
  <img src="/_figures/soloT_testPlot.png" alt="Description of image">
  <figcaption>Figure 4. Temperature readings from the solo T sensors.</figcaption>
</figure>


This plot is a bit confusing because my end time filtering came after I pulled all the sensors out. However, the start time in this plot is correct as I started the timer after all the sensors were in the water for a couple minutes.

Given this, these look pretty good and are consistent with the temperatures that the RBR T.ODOs. I feel pretty good about these but I am still going to re-test them on Thursday.

### Sampling intervals

For these sensors we can realistically have the sensors sample at 1 Hz while still maintaining enough battery life for over a month. This is true for both alkaline and lithium iron batteries.


## RBR Duos

### Plots 

I sampled these on April 15. I put these sensors together in a single bucket with the thermistors and the pressure gages pointing down. They were in the bucket for just over 30 minutes.


<figure>
  <img src="/_figures/RBRDuo_bucketTest_tempTimeseries.png" alt="Description of image">
  <figcaption>Figure 5. Temperature readings from the Duo sensors.</figcaption>
</figure>


<figure>
  <img src="/_figures/RBRDuo_bucketTest_pressureTimeseries.png" alt="Description of image">
  <figcaption>Figure 6. Pressure readings from the Duo sensors.</figcaption>
</figure>

These both look pretty good to me! Yay for new sensors.

### Sampling intervals

The lithium batteries in these sensors are pretty powerful so we can kind of have our pick of sampling intervals with these. I think it makes the most sense to line them up with the intervals of the SoloTs so that the entire t-chain is reading at the same interval.



## miniDOTs

I did this bucket test yesterday, April 20. I put the miniDOTS in the same bucket at the same time and included an RBR duet T.ODO to accompany it. The miniDOTs read every 5 minutes, and the T.ODO measured every 30 seconds. They were in the bucket for several hours.


<figure>
  <img src="/_figures/DOComp_miniDOTsRBR.png" alt="Description of image">
  <figcaption>Figure 7. Dissolved oxygen readings from the miniDOT sensors compared to the RBR T.ODO.</figcaption>
</figure>



Well, the trends in dissolved oxygen are the same which is heartening. The range between the sensors is not super large and they match the RBR well. For our purposes, these values seem decent. Also, the oxygen accuracy is about +/- 0.3 mg/L (or +/- 5% of the measurement, depending on whichever is larger) which explains the differences in the values almost perfectly. In case you're curious, the oxygen response time is about 30 seconds.

<figure>
  <img src="/_figures/DOComp_miniDOTsRBR.png" alt="Description of image">
  <figcaption>Figure 8. Temperature readings from the miniDOT sensors compared to the RBR T.ODO.</figcaption>
</figure>



Again the values are showing a similar trend to each other and the RBR. There is some variation in the miniDOT values, but these all fall within the +/- 0.1 degrees C accuracy. The response time of temperature is 5 minutes. I feel good about these values.

### Sampling interval

The miniDOTS can sample at an interval of 5 seconds to 24 hours. I have yet to check the specifics of the battery life, but I am pretty sure that we will at least have to sample every couple minutes for the batteries to last the whole month. 


## Next steps for the bucket tests

- Re-test the solo Ts
- Test the RBR concerto with the upcast only sampling
- Test the other two Concertos that will go on the v4 SWIFT moorings

This will conclude the external sensors assumin

