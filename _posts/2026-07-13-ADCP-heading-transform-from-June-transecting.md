## Correcting the heading from the ADCP we used for transecting in June transecting

The original data from the Teledyne RDI Workhorse Sentinel II 1200kHz ADCP we used for continual transecting during the flood and the ebb in June of 2026 has incorrect heading values. To fix this, I separated out the individual transect lines for both the flood and ebb surveys, used the lat/lon values to determine the course over ground (COG), found the heading of the ADCP and the difference between the COG and listed heading, and then corrected the velocities for each transect line using the average heading bias for each line. I will go into more detail about each step below.


### Separating out the transect lines

I did this visually using the transect line plots below colored by time. I was able to follow the different colors and pick out the beginning and ending time stamp for each line. I made sure to be conservative in my choices for what constituted the beginning and end of a line and made sure not to include turns or the beginning/ending of any turn action.



TransectPath_throughTime_ebb.png
