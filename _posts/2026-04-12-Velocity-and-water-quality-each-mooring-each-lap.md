# Initial plots and analysis of velocity, salinity, temperature, and DO at each lap and mooring location

I pulled the velocity, temperature, salinity, and dissolved oxygen profiles that were nearest to each planning mooring location. To do this, I found the closest lat/lon position to each mooring location from the ADCP track. I found the closest CTD cast time to each ADCP ensemble time and assigned the corresponding ADCP lat/lon value to that CTD cast.

The main reason for doing this analysis has been to determine what might be causing the dissolved oxygen minimum at 15-20 meters throughout the water column. The main plot that has inspired this was the one with the profiles that "walked" west ot east throughout Penn Cove.


**First the north length:**

<img width="1240" height="860" alt="TempSalDO_marchingProfiles_northlength" src="https://github.com/user-attachments/assets/62dc1679-78be-4f26-8b8b-52dee09550c4" /><br>Fig 1. Dissolved oxygen, temperature, salinity profiles along northern length of Penn Cove.<br>





**South length:**

<img width="1527" height="919" alt="TempSalDO_marchingprofilesSouthLength" src="https://github.com/user-attachments/assets/dee76cc8-e8b6-42d4-9d0b-ff53a33642d6" /><br>Fig 2. Dissolved oxygen, temperature, salinity profiles along south length of Penn Cove.<br>


## New plots

I have pulled together the profiles of temperature, dissolved oxygen, salinity, and east/west and north/south velocities at the planned mooring locations for each lap. My hope is that this gives us some insight into how tidal processes might play into the trends we see.

First, I want to bring up the plot of the lap sampling intervals on the tide chart.

<img width="1443" height="574" alt="Screenshot 2026-04-12 at 11 57 05 PM" src="https://github.com/user-attachments/assets/f073affe-555f-4902-a22d-5f47daba349e" /><br>Fig 3. Tidal stage predictions from the NOAA Penn Cove station for December 4, 2025. The high of 3.73m occurred at 05:12, the low of 2.40m occurred at 10:06, the second high of 3.76m occurred at 15:04, and the second low of -1.18m occurred at 22:20. Time stamps are in PST. Tide window 1, detailed below, is outlined in red, tide window 2 is outlined in gold, and tide window 3 is outlined in purple.<br>


### Lap 1 

A quick note on the velocities. I did some initial cleaning of the individual profiles by removing values that were outside one stadnard deviation from the mean velocity value for each ensemble. There was a lot of scatter in the bottom velocities that were most definitely from bed interference, so removing anamolously high values seemed like the logical thing to do. I started with removing points that were only two standard deviations away from the mean, but that made no change to the profiles so I then applied the stricter tolerance of one standard deviaiton after that. 




For the velocity plots below for the first lap, here are the tidal stages each measurement was taken at. Note that WWS, the bottom right corner panel, was measured first in the sampling track we took.

- Wire walker south: Ebb
- LoveJoy south: Ebb
- Back bay south: Ebb
- Back bay north: Slack (assuming slack occurs about 30 minutes before the high or low)
- LoveJoy north: Low
- Wire walker north: Slack, entering the flood



<img width="1488" height="951" alt="lap1_EastWest_allmooringSubplots_LINKED" src="https://github.com/user-attachments/assets/4b1c1aff-0119-463a-97f8-9b6e065c733a" /><br>Fig 4. East/west velocities at each mooring location for the frist lap. Positive is east, negative is west. Profiles show the average of the 5 closest ADCP readings to each mooring location. Shading shows standard deviation. Time is in UTC.<br>




**Here are the north/south velocities at the same times.**




<img width="1488" height="951" alt="lap1_NorthSouth_allmooringsSubplots_LINKED" src="https://github.com/user-attachments/assets/54b7fc1e-e1d7-4d24-893f-ebd5f71d09a9" /><br>Fig 5. North/south velocities at each mooring location for the frist lap. Positive is north, negative is south. Profiles show the average of the 5 closest ADCP readings to each mooring location. Shading shows standard deviation. Time is in UTC.<br>



/

I am going to break down the velocity, CTD, and TS plots for each mooring in lap 1 now.







#### Wire walker south



#### LoveJoy south




#### Inner bay south



#### Inner bay north



#### LoveJoy north


#### Wire walker north



### Lap 2


#### Wire walker south



#### LoveJoy south




#### Inner bay south



#### Inner bay north



#### LoveJoy north


#### Wire walker north



### Lap 3


#### Wire walker south



#### LoveJoy south




#### Inner bay south



#### Inner bay north



#### LoveJoy north


#### Wire walker north








