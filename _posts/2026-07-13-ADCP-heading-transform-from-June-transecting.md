## Correcting the heading from the ADCP we used for transecting in June transecting

The original data from the Teledyne RDI Workhorse Sentinel II 1200kHz ADCP we used for continual transecting during the flood and the ebb in June of 2026 has incorrect heading values. To fix this, I separated out the individual transect lines for both the flood and ebb surveys, used the lat/lon values to determine the course over ground (COG), found the heading of the ADCP and the difference between the COG and listed heading, and then corrected the velocities for each transect line using the average heading bias for each line. I will go into more detail about each step below.


### Separating out the transect lines

I did this visually using the transect line plots below colored by time. I was able to follow the different colors and pick out the beginning and ending time stamp for each line. I made sure to be conservative in my choices for what constituted the beginning and end of a line and made sure not to include turns or the beginning/ending of any turn action.

#### First the ebb tide 

<figure>
  <img src="/_figures/TransectPath_throughTime_ebb.png" alt="Description of image">
  <figcaption>Figure 1. Ship-mounted ADCP path from the major ebb of the day in Penn Cove. Colors indicate time. The timestamps for hte colobar are in MATLAB datenum format. </figcaption>
</figure>
<br><br>


Here is the breakdown of the line directions for the ebb tide:

- Line 1: North to south across LoveJoy line
- Line 2: West to east across Penn Cove (back bay to mouth of cove)
- Line 3: North to south across LoveJoy line
- Line 4: West to east across Penn Cove (back bay to mouth of cove)
- Line 5: South to north across LoveJoy line
- Line 6: North to south across LoveJoy line
- Line 7: West to east across Penn Cove (back bay to mouth of cove)
- Line 8: East to west across Penn Cove (mouth of cove to back bay)


### Flood tide



### Finding the course over ground (COG)

Once I determined the different lines and separated them out in the data, I used the lat and lon values from each line to determine the COG and the heading in degrees clockwise from North. **Note here that these are lat/lon values from the ADCP, not the boat. We don not actually know the boat's true heading because we do not have that data. When fighting the wind or current (such as a major flood or ebb of the day), the boat drives at a crab angle which affects the true heading. So the *true* heading of the boat is not reflected correctly here.**

I pulled out the average COG for each transect line and looked at the *circular standard deviation* of each COG to detemine how much the data deviated from the average COG in the line. If the standard deviation was much more that about 6 degrees or so, I went back and looked at the transect line I defined and removed any loops from the physical turning of the boat when transitioning between transect lines. The north/south transect lines had higher standard deviations than the east/west lines because the boat was clearly fighting the current and possibly the wind so the boat's physical path was a little more wobbly than the east/west lines. 

Below are three figures from the **ebb tide** that show the an example of the deviation around the mean COG in line 8 (east/west), an example from line 3 (north/south), and a visualization the the slightly wobbly boat path for line 5 (north/south) and the COG heading direction that corresponds to each value of that transect.



<figure>
  <img src="/_figures/Example_checkCOGplot_ebbLap8.png" alt="Description of image">
  <figcaption>Figure 2. COG for each data point in the 8th line of the ebb transect. This was the final line and went from east to west across the bay. </figcaption>
</figure>
<br><br>


<figure>
  <img src="/_figures/Example_checkCOGplot_ebbLap3.png" alt="Description of image">
  <figcaption>Figure 3. COG for each data point in the 3rd line of the ebb transect. This line went from north to south across the LoveJoy line. </figcaption>
</figure>
<br><br>

See how between these two plots, line 3 has a larger circular standard deviation around the COG heading mean than line 8. 


<figure>
  <img src="/_figures/TransectLineWanderingExample_ebbLap5.png" alt="Description of image">
  <figcaption>Figure 4. Left panel shows the course of the boat across the LoveJoy line from south to north. The colors indicate the data point number through this section of the time series. The right panel shows the COG heading direction in degrees for each data point. </figcaption>
</figure>
<br><br>

Note that the large dip in COG direction in degrees in the right-hand panel corresponds to the same data points that bracket the large bend in the transect.


For the **ebb tide** here are the breakdown of the COG means and their circular standard deviations:
- Line 1: circular std of cogDir = 4.67 deg (mean COG = 186.96 deg)
- Line 2: circular std of cogDir = 3.29 deg (mean COG = 84.33 deg)
- Line 3: circular std of cogDir = 6.00 deg (mean COG = 172.51 deg)
- Line 4: circular std of cogDir = 1.23 deg (mean COG = 85.39 deg)
- Line 5: circular std of cogDir = 7.14 deg (mean COG = 358.36 deg)
- Line 6: circular std of cogDir = 6.37 deg (mean COG = 173.60 deg)
- Line 7: circular std of cogDir = 3.11 deg (mean COG = 83.47 deg)
- Line 8: circular std of cogDir = 2.76 deg (mean COG = 262.89 deg)

One check here is that reciprocal lines have opposite mean COG headings and similar circular standard deviations, which is a sign that everything makes sense so far. 

Reciprocal lines: 
- 1, 3, and 6 are reciprocals of 5 (north to south vs. south to north)
- 2, 4, and 7 are reciprocals of 8 (west to east vs. east to west)

Below are similar figures for the **flood tide**.



### Comparing the COG to the ADCP headings

I pulled out the average ADCP heading for each line and then calculated the bias between the COG and the ADCP heading for each transect line. I decided to use the average heading and COG for each transect line instead of for each data point because it reduces any noise that might be introduced from point-to-point due to jumps in the boat's velocity. Applying an average means that the resulting east and west velocities are not EXACT, but then again they were not going to be exact anyway because of unknown confounding variables from the boat's crab angle. Applying an average correction for each line also standardizes the data in each line so they points can be compared together in a line instead of having to account for the small differences in the headings adjustment from data point to data point in a line. 


#### Ebb tide COG and ADCP heading summary



| Line number | COG (degrees CW form north) | ADCP reported heading (degrees CW form north) | Mean bias (degrees CW from north)  |
| --- | --- | --- |  ---  |
| 1 | 186.96 | 223.71 |  -36.75  |
| 2 | 84.33 | 1.33 |  83.01  |
| 3 | 172.51 | 214.10 |  -41.59  |
| 4 | 85.39 | 7.62 |  77.78  |
| 5 | 358.36 | 311.98 |  46.38  |
| 6 | 173.60 | 207.91 |  -34.31  |
| 7 | 83.47 | 18.99 |  64.48  |
| 8 | 262.89 | 258.47 |  4.42  |


Here, a positive bias means the GPS COG is clockwise of the ADCP heading. In other words the ADCP is under-reading, so we need to rotate its data clockwise/add degrees to correct it.
A negative bias means the GPS COG is counterclockwise of the ADCP heading. In other words the ADCP is over-reading, so we need to rotate the other way.


#### Flood tide COG and ADCP heading summary



### Corrected velocity timeseries

If enerything above is correct, the following time series are the corrected east and north velocity time series. 

#### Ebb tide

First the **original, incorrect** time series:

<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_ebb_ENUquicklook.png" alt="Description of image">
  <figcaption>Figure 5. Original, incorrect east/west and north/south velocity profiles for the major ebb tide. </figcaption>
</figure>
<br><br>




Next the **corrected** time series:


<figure>
  <img src="/_figures/Corrected_velocity_timeseries_ebb.png" alt="Description of image">
  <figcaption>Figure 6. Corrrected east/west and north/south velocity profiles for the major ebb tide. </figcaption>
</figure>
<br><br>


A major difference here is that the majority of the east/west velocity is actually east in the corrected ebb tide, which makes more sense in Penn Cove. Another good check here is that in the corrected velocities the east/west velocities are larger than the north/south velocities which is to be expected with the tidal propogation in the cove.





### Comparing to a pcolor plot of velocity from the LoveJoy SWIFTs during the major ebb and flood tide to check the patterns in the corrected data are correct

#### Ebb


#### Flood






