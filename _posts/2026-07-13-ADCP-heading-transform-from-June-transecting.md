# Correcting the heading from the ADCP we used for transecting in June transecting

The original data from the Teledyne RDI Workhorse Sentinel II 1200kHz ADCP we used for continual transecting during the flood and the ebb in June of 2026 has incorrect heading values. To fix this, I separated out the individual transect lines for both the flood and ebb surveys, used the lat/lon values to determine the course over ground (COG), found the heading of the ADCP and the difference between the COG and listed heading, and then corrected the velocities for each transect line using the average heading bias for each line. I will go into more detail about each step below.


If you are curious about my code, you can find it here in the [PennCove_codes repo I have created for this project.](https://github.com/maiaheffernan/PennCove_codes/blob/main/Processing/transectADCP_headingCorrection.m) The script is a little messy and full of my comments, so strength to anyone who ventures in there.


## Separating out the transect lines

I did this visually using the transect line plots below colored by time. I was able to follow the different colors and pick out the beginning and ending time stamp for each line. I made sure to be conservative in my choices for what constituted the beginning and end of a line and made sure not to include turns or the beginning/ending of any turn action.

### First the ebb tide 

<figure>
  <img src="/_figures/TransectPath_throughTime_ebb.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 1. Ship-mounted ADCP path from the major ebb of the day in Penn Cove. Colors indicate time. The timestamps for hte colobar are in MATLAB datenum format. </figcaption>
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

The transect path for the flood was a little more wobbly, but that's okay.


<figure>
  <img src="/_figures/TransectPath_throughTime_flood.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 2. Ship-mounted ADCP path from the major flood of the day in Penn Cove. Colors indicate time. The timestamps for hte colobar are in MATLAB datenum format. </figcaption>
</figure>
<br><br>

Here is the breakdown of the line directions for the flood tide:

- Line 1: East to west across Penn Cove (mouth of cove to back bay)
- Line 2: North to south across LoveJoy line
- Line 3: West to east across Penn Cove (back bay to mouth of cove)
- Line 4: South to north across LoveJoy line
- Line 5: East to west across Penn Cove (mouth of cove to back bay) -- this is the one that is particularly wavy
- Line 6: North to south across LoveJoy line
- Line 7: West to east across Penn Cove (back bay to mouth of cove)
- Line 8: South to north across LoveJoy line


## Finding the course over ground (COG)

Once I determined the different lines and separated them out in the data, I used the lat and lon values from each line to determine the COG and the heading in degrees clockwise from North. **Note here that these are lat/lon values from the ADCP, not the boat. We don not actually know the boat's true heading because we do not have that data. When fighting the wind or current (such as a major flood or ebb of the day), the boat drives at a crab angle which affects the true heading. So the *true* heading of the boat is not reflected correctly here.**

I pulled out the average COG for each transect line and looked at the *circular standard deviation* of each COG to detemine how much the data deviated from the average COG in the line. If the standard deviation was much more that about 6 degrees or so, I went back and looked at the transect line I defined and removed any loops from the physical turning of the boat when transitioning between transect lines. The north/south transect lines had higher standard deviations than the east/west lines because the boat was clearly fighting the current and possibly the wind so the boat's physical path was a little more wobbly than the east/west lines. 

------
**A quick math aside:** When I say cicular standard deviation I am referring to this equation:

$$
\sigma_{\text{circ}} = \sqrt{-2\ln(R)} \cdot \frac{180}{\pi}
$$

(the $\frac{180}{\pi}$ converts the values from radians to degrees)

where **R** is the mean resultant vector length. When we impart the unit circle onto a plane, each heading observation becomes a point in space on that plane represented by a unit vector with components $\cos\theta_i$ and $\sin\theta_i$. The sum of those observations as unit vectors gives a resultant vector with length **R** = |r|. 


Now comes the cool part: $\overline{R}$ is actually a representation of the concentration of the observations. If we imagine all the observations pointing out from the origin at their respective angles, to find the resultant we have to add up all the arrows head-to-tail then measure the length of the final arrow (simple vector addition). If the arrows all point in roughly the same direction they stack on top of each other in this head-to-tail addition and the resultant arrow ends up being long. If all the arrows point in many different directions, however, the resultant arrow will be short or even cancel out.

Because I am averaging the vector components rather than summing them the quantity I get directly is the mean resultant length, $\overline{R} = R/n$, which is already bounded in [0,1]. So an $\overline{R}$ value at or close to 1 means that there is a tight cluster of angles represented in the observations (aka a *high concentration* of angles in a given direction), so the standard deviation will be low. An $\overline{R}$ value at or close to 0 means that there is a large spread in the observed angles (aka a *low concentration* of angles in a given direction), so the standard deviation will be high.


It is calculated from the averaged sine and cosine components of the angles:

$$
\overline{R} = \sqrt{\left(\frac{1}{n}\sum_{i=1}^{n} \cos\theta_i\right)^2 + \left(\frac{1}{n}\sum_{i=1}^{n} \sin\theta_i\right)^2}
$$


*Also note* that when I refer to the mean COG I am referring to the circular mean calculated as the arctangent of the average sines and cosines of each degree:

$$
\overline{\theta} = \text{atan2}\left(\frac{1}{n}\sum_{i=1}^{n} \sin\theta_i, \; \frac{1}{n}\sum_{i=1}^{n} \cos\theta_i\right) \bmod 360°
$$

I use the atan2 function in matlab to include the full 360 degree range by using the individual signs of the sine and cosine components to determine the correct quadrant in the compass. Also the mod(360) ensures the result is expressed as a standard compass bearing between 0 and 360 degrees from north.  


______

Below are three figures from the **EBB TIDE** that show the an example of the deviation around the mean COG in line 8 (east/west), an example from line 3 (north/south), and a visualization the the slightly wobbly boat path for line 5 (north/south) and the COG heading direction that corresponds to each value of that transect.



<figure>
  <img src="/_figures/Example_checkCOGplot_ebbLap8.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 3. COG for each data point in the 8th line of the ebb transect. This was the final line and went from east to west across the bay. </figcaption>
</figure>
<br><br>
<br><br>

See how between these two plots, line 3 has a larger circular standard deviation around the COG heading mean than line 8. 

<br><br>
<figure>
  <img src="/_figures/Example_checkCOGplot_ebbLap3.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 4. COG heading for each data point in the 3rd line of the ebb transect. This line went from north to south across the LoveJoy line. The dotted red line in the top panel shows the mean for the line and the blue lines shows the point-by-point fluctuations. The bottom panel shows the boat's speed. Drastic changes in boat speed could be indications of times when the boat's/ADCP's heading briefly changed or times of a small turn, so comparing this with the COG heading might help explain any large outliers.  </figcaption>
</figure>
<br><br>
<br><br>

Looking at the boat's path and the corresponding COG.
<br><br>

<figure>
  <img src="/_figures/TransectLineWanderingExample_ebbLap5.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 5. Left panel shows the course of the boat across the LoveJoy line from south to north. The colors indicate the data point number through this section of the time series. The right panel shows the COG heading direction in degrees for each data point. </figcaption>
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


<br><br>


Below are similar figures for the **FLOOD TIDE**.


First we have an example of a transect lines 2 and 5 that have a large circular standard deviations in COG. These are accompanied by somewhat wobbly transect lines or lines that gradually meander in one direction, which is what creates the large standard deviations here. 

<br><br>


<figure>
  <img src="/_figures/Example_largeSTD_Flood_line2.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 6. COG heading for each data point in the 2nd line of the flood transect. This line went from north to south across the LoveJoy line. The dotted red line in the top panel shows the mean for the line and the blue lines shows the point-by-point fluctuations. The bottom panel shows the boat's speed. Drastic changes in boat speed could be indications of times when the boat's/ADCP's heading briefly changed or times of a small turn, so comparing this with the COG heading might help explain any large outliers. </figcaption>
</figure>
<br><br>
<br><br>

Looking at the boat's path and the corresponding COG.
<br><br>

<figure>
  <img src="/_figures/Line2_flood_track.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 7. Left panel shows the course of the boat across the LoveJoy line from north to south. The colors indicate the data point number through this section of the time series. The right panel shows the COG heading direction in degrees for each data point. </figcaption>
</figure>
<br><br>
<br><br>

This line wanders a bit, and the large arcs in one direction or another corresopnd with the large jumps in the heading in the right panel in the figure above. This accounts for the large standard deviation in the COG. 


The same thing can be seen in Line 5, the transect line from east to west, below.

<br><br>

<figure>
  <img src="/_figures/Example_largeSTD_Flood_line2.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 8. COG heading for each data point in the 5th line of the flood transect. This line went from east to west across the cove. The dotted red line in the top panel shows the mean for the line and the blue lines shows the point-by-point fluctuations. The bottom panel shows the boat's speed. Drastic changes in boat speed could be indications of times when the boat's/ADCP's heading briefly changed or times of a small turn, so comparing this with the COG heading might help explain any large outliers. </figcaption>
</figure>
<br><br>
<br><br>

Looking at the boat's path and the corresponding COG.
<br><br>

<figure>
  <img src="/_figures/Line5_flood_path.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 9. Left panel shows the course of the boat across the cove from east (the mouth) to west (the end). The colors indicate the data point number through this section of the time series. The right panel shows the COG heading direction in degrees for each data point. </figcaption>
</figure>
<br><br>
<br><br>


Finally, a really good example of how the wiggles affect the heading is in line 8 from the flood transect. You can see that from the start of the transect there are a few bends in one direction and then the other as an over-correction. You can see the heading jump up and down in the right-hand panel in concert with this.



<figure>
  <img src="/_figures/Line8_flood_path.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 10. Left panel shows the course of the boat across the cove from south to north across the LoveJoy line. The colors indicate the data point number through this section of the time series. The right panel shows the COG heading direction in degrees for each data point. </figcaption>
</figure>
<br><br>
<br><br>



My main point here is that the boat paths are, understandably, not perfectly straight. There is inherent noise in the COG heading in each line. However, to be able to make comparison for headings and ultimately velocities in each line and between lines I am just going to be applying the mean heading from each line to the data. 

<br><br>

For the **flood tide** here are the breakdown of the COG means and their circular standard deviations:
- Line 1: circular std of cogDir = 3.61 deg (mean COG = 263.39 deg)
- Line 2: circular std of cogDir = 10.29 deg (mean COG = 168.39 deg)
- Line 3: circular std of cogDir = 2.81 deg (mean COG = 84.07 deg)
- Line 4: circular std of cogDir = 4.36 deg (mean COG = 353.23 deg)
- Line 5: circular std of cogDir = 9.11 deg (mean COG = 264.52 deg)
- Line 6: circular std of cogDir = 3.23 deg (mean COG = 169.19 deg)
- Line 7: circular std of cogDir = 2.51 deg (mean COG = 83.44 deg)
- Line 8: circular std of cogDir = 3.56 deg (mean COG = 351.40 deg)

One check here is that reciprocal lines have opposite mean COG headings and similar circular standard deviations, which is a sign that everything makes sense so far. 

Reciprocal lines: 
- 1 and 5 are reciprocals of 3 and 7 (east to west vs. west to east)
- 2 and 6 are reciprocals of 4 and 8 (north to south vs. south to north)



## Comparing the COG to the ADCP headings

I pulled out the average ADCP heading for each line and then calculated the bias between the COG and the ADCP heading for each transect line. I decided to use the average heading and COG for each transect line instead of for each data point because it reduces any noise that might be introduced from point-to-point due to jumps in the boat's velocity. Applying an average means that the resulting east and west velocities are not EXACT, but then again they were not going to be exact anyway because of unknown confounding variables from the boat's crab angle. Applying an average correction for each line also standardizes the data in each line so they points can be compared together in a line instead of having to account for the small differences in the headings adjustment from data point to data point in a line. 


### Ebb tide COG and ADCP heading summary



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


### Flood tide COG and ADCP heading summary

| Line number | COG (degrees CW form north) | ADCP reported heading (degrees CW form north) | Mean bias (degrees CW from north)  |
| --- | --- | --- |  ---  |
| 1 | 263.39 | 251.22 |  12.17  |
| 2 | 168.39 | 153.83 |  14.57  |
| 3 | 84.07 | 51.99 |  32.08  |
| 4 | 353.23 | 341.09 |  12.14  |
| 5 | 264.52 | 253.79 |  10.79  |
| 6 | 169.19 | 165.03 |  4.16  |
| 7 | 83.44 | 50.19 |  33.25  |
| 8 | 351.40 | 328.64 |  22.76  |


Interesting that the bias is always positive for the flood. I don't know if that means anything, but just a curious pattern. 


## Corrected velocity timeseries

If enerything above is correct, the following time series are the corrected east and north velocity time series. 

### Ebb tide

First the **original, incorrect** time series:

<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_ebb_ENUquicklook.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 11. Original, incorrect east/west and north/south velocity profiles for the major ebb tide. </figcaption>
</figure>
<br><br>




Next the **corrected** time series:


<figure>
  <img src="/_figures/Corrected_velocity_timeseries_ebb.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 12. Corrrected east/west and north/south velocity profiles for the major ebb tide. </figcaption>
</figure>
<br><br>


A major difference here is that the majority of the east/west velocity is actually east in the corrected ebb tide, which makes more sense in Penn Cove. Another good check here is that in the corrected velocities the east/west velocities are larger than the north/south velocities which is to be expected with the tidal propogation in the cove.



### Flood

First the **original, incorrect** time series:

<figure>
  <img src="/_figures/Echo_ADCP_24Jun2026_flood_ENUquicklook.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 13. Original, incorrect east/west and north/south velocity profiles for the major flood tide. </figcaption>
</figure>
<br><br>



Next the **corrected** time series:


<figure>
  <img src="/_figures/Corrected_eastNorth_timeseries.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 14. Corrrected east/west and north/south velocity profiles for the major flood tide. </figcaption>
</figure>
<br><br>


There is not a huge difference here, but the main thing I see is that the north/south velocity magnitudes are dimished which makes sense given that we think the tidal excursion is primarily east/west. 

## Comparing to a pcolor plot of velocity from the LoveJoy SWIFTs during the major ebb and flood tide to check the patterns in the corrected data are correct

Ostensibly, if the tide propogates in and out of Penn Cove in a similar manner evert ti

### Ebb


### Flood






