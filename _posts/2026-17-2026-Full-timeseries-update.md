# Full time series from the v4 moorings

Since coming back from the field, my main goal has been concatenating, cleaning, and organizing all the data into a tidy structure. This is still in progress. But, I do have the fully concatenated, uncleaned time series for the mooring sensors. Exciting! These are below.


## Overall takeaways from the plots below

- Temperatures at the bottom of the water column and in the middle of the water column increased from around 9.5 degrees C to just over 12 degrees C throughout the course of the deployment. This is consistent at all moorings.

- Bottom dissolved oxygen decreased throughout the deployment (as we already know), as did oxygen levels in the middle of the water column. Lots of hypoxia!

- Visually, it looks like maximum salinity increased *slightly* from 29-30 PSU at all moorings and depths throughout the course of the deployment. My plan is to do a Mann Kendall test for a trend in the data after I get through all the organization and processing steps. 

- The variance in the temperature data decreases in September to October for all moorings and all sensors in the water column. There are some wind events that occur, but otherwise the data is steady.

- In July and August it looks like there is a kind of "waviness" to the temperature and salinity data? It is most noticeable in these months across the whole water column. In the bottom plot that shows the temperature and pressure data from the Duos, it looks like it might coincide with the Spring/Neap tidal variation. This is similar to the patterns we think we see in the Godin-filtered oxygen data. I think there is something to this! It is interesting it is most noticeable in these months, though. Maybe there is more Skagit discharge at this time? Or maybe not... See graph of discharge at the end of this blog post.



<br>




## The bottom-DO data from the TODOs

These sensors are located on the bottom of all the moorings. Those on the LoveJoy and Inner moorings sample every 1 minute and those on the bottom of the wire walkers sample once every 5 minutes. Note that the TODO on Wire Walker north instantly got submerged in the mud so the temperature reading is that of the bed, and the oxygen values are not useable and should not be interpreted.

<br><br>
<figure>
  <img src="/_figures/TODOdata_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 1. Bottom dissolved oxygen data. The sensors on the LoveJoy and Inner Moorings were reading every 1 minute, and the sensors on the bottom of the wire walker moorings were reading every 5 minutes. </figcaption>
</figure>
<br><br>


## The miniDOT data

These sensors were located mid-mooring on the LoveJoy line moorings. There were two miniDOTs per mooring. The other two miniDOTS were located in the Penn Cove Shellfish mussel rafts at 3m and 7m below the surface. They sample every 10 minutes.


<br><br>
<figure>
  <img src="/_figures/miniDOT_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 2. Dissolved oxygen and temperature data in the middle of the water column on the LoveJoy moorings and in the middle and on the bottom on the shellfish raft moorings. These sensors sample once every 10 minutes. </figcaption>
</figure>
<br><br>



## The YSI CTD data

These sensors were located in the upper part of the water column on the LoveJoy moorings. There were two sensors per mooring. They sample once every 10 minutes.


<br><br>
<figure>
  <img src="/_figures/YSI600LSdata_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 3. Temperature and salinity measured in the upper-middle water column on the LoveJoy moorings. These sensors sample once every 10 minutes. </figcaption>
</figure>
<br><br>


## The soloT data

These sensors make up the bulk of the moorings line sensors on all found v4 SWIFT moorings (LoveJoy and Inner moorings). There are 7 soloT sensors on each mooring line. They read at a rate of 1 Hz. 


<br><br>
<figure>
  <img src="/_figures/SoloTdata_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 4. Temperature measured at 1Hz at 7 discrete depths on each mooring. Exact depths have yet to be calculated </figcaption>
</figure>
<br><br>


## The SeaBird data

The SeaBird CTD was located on the bottom of the LoveJoy South mooring. It sampled every 10 minutes. For the first several months of deployment the tubing that led to the salinity sensor got filled with sediment, so the data quality is horrible. We ended up putting a float on the sensor in July, so the data quality got better beginning then.


<br><br>
<figure>
  <img src="/_figures/seabirdData_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 5. The Seabird CTD was located on the bottom of LoveJoy south. It sampled every 10 minutes. </figcaption>
</figure>
<br><br>


## The Bottom-mounted Concerto CTDs

From May through July only LoveJoy north had a concerto CTD at the bottom. From the end of July through August we added another concerto to the bottom of Inner north (thanks, Sam!). The concerto on the bottom of LoveJoy north took a measurement at 1 Hz for two seconds every 2 minutes (so essentially an average of two readings every 2 minutes). The concerto on the bottom of Inner north read once every 5 minutes at a sampling rate of ________ (I need to go back and look).


<br><br>
<figure>
  <img src="/_figures/mooredConcertoData_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 6. The bottom-mounted Concerto CTDs were located on the bottom of LoveJoy north and Inner north. </figcaption>
</figure>
<br><br>





## The Duo T.D. sensors

The Duos were located on the Inner moorings. Inner north had a Duo on the anchor, acting as a tide gage, and one on the line. Inner south only had one sensor on the line. From May-June these sensors measured at 1 Hz, but after that they measured at 10 seconds.


<br><br>
<figure>
  <img src="/_figures/DuoTDdata_MayOct2026_concatenated_L1.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 7. The Duo temperature and depth sensors. These sensors measured at 1 Hz from May to June and then at 10 second intervals from June onward. </figcaption>
</figure>
<br><br>


## Skagit River discharge from Mt. Vernon station from May 1 - Nov 1, 2026

<img width="1006" height="622" alt="Screenshot 2026-11-18 at 10 05 38 AM" src="https://github.com/user-attachments/assets/b701a142-7887-4d03-9ef8-70f8612cf99f" />


<br>


## Next steps for this data (hopefully by Thanksgiving)

1) De-spiking
2) Figuring out the depths for all the sensors at a given time with the SWIFT watch circle
3) Putting everything in data structures: right now there are 3 planned: one for the raw data and the different sampling intervals, one for de-spiked data at the different sampling intervals, one that is worked into the SWIFT structure that is on the same 30 minute timestamps as the SWIFT measurements. 

