# Velocity profiles at mooring locations

This is a rough draft of the velocity profiles at the mooring locations. There is still more to do to make these plots look nice and to tie in the biogeochemical data, but I am putting these here as a first step at making this more elaborate plot.


This data is pulled from the December sampling trip. For context, here is a plot of those tidal stages and the lap sampling windows from that day.

<img width="662" height="259" alt="Screenshot 2026-03-31 at 1 34 48 PM" src="https://github.com/user-attachments/assets/2bc30e26-860d-4797-abac-5fe4af3253c5" />

The red box is lap 1, the yellow box is lap 2, and the purple box is lap 3.


### The profiles

The profiles shown in this next section are average velocity profiles from the Workhorse ADCP that was attached to the R/V Echo on the sampling day in December. I pulled the five closest profiles in space to the lat/lon positions of the planned mooring locations for the long-term deployment starting in May and averaged them together. 

The goal of doing this is to see if the velocity is responsible for the DO minimum that we see between 10-20m in the water column from the CTD casts from the same December trip. These will be a part of a larger, more explanatory plot so for now here are the things I still have to do with them:

-  Make TS plots and color them by DO at the mooring locations. I need to grab the isopycnal lines for this, too.
-  Clean the velocity data to level 2 or 3.
-  Add the SWIFT data at the same times so I can see how water was circulating in and out of the cove at the time of each velocity profile ensemble.
-  Double check through plotting on a map which profiles I am actually averaging here. When I included 'omitnan' in the averaging I am afraid that I might have been averaging some weird values so I want to check this visually. This is coming later this week.



All that being said, here are the initial plots.

#### Lap 1

First the east/west velocities

<img width="947" height="672" alt="Screenshot 2026-03-31 at 1 45 08 PM" src="https://github.com/user-attachments/assets/9ab08253-6753-454b-95a6-379557063d45" />


Now the north/south velocities

<img width="963" height="755" alt="Screenshot 2026-03-31 at 1 46 17 PM" src="https://github.com/user-attachments/assets/67ee0809-b9d6-47f1-b060-8ba45b1b06ff" />



These profiles fall during the ebb with the exception of wire walker north and LoveJoy north which fall during the slack and slack/low respectively. 
I was looking for a clear eastward velocity at 15-20m in the water column that would carry the low DO signal through the cove, and though this is abvious in the inner bay north profile, it is really not that obvious or is in fact opposite in the other profiles. The north/south profiles do not have anything obvious that jumps out, either. The inner bay north does have southward velocities in this depth range, which could explain the trends that we saw in the "walking profiles" from the biogeochem profiles. What does make a bit of sense is that the south flowing water at this depth could be what is creating the low DO along the south length! This circulation pattern is also something that Dakota's plots have been pointing to. 




Here are those plots with linked axes. It greatly diminishes the clarity of the profile directions.

<img width="968" height="754" alt="Screenshot 2026-03-31 at 1 47 21 PM" src="https://github.com/user-attachments/assets/62a102c5-03c1-430f-b74b-402be7adb25b" />

<img width="960" height="722" alt="Screenshot 2026-03-31 at 1 47 35 PM" src="https://github.com/user-attachments/assets/68617aed-1d94-40c6-bb6e-564429651fd4" />



#### Lap 2

East/West


<img width="1008" height="739" alt="Screenshot 2026-03-31 at 1 58 15 PM" src="https://github.com/user-attachments/assets/11267697-a814-4220-9548-3470c0de2455" />


North/south

<img width="977" height="754" alt="Screenshot 2026-03-31 at 1 58 26 PM" src="https://github.com/user-attachments/assets/8d9bb482-0537-48cc-bdb8-8da44350965d" />



#### Lap 3

East/West

<img width="970" height="752" alt="Screenshot 2026-03-31 at 1 58 50 PM" src="https://github.com/user-attachments/assets/f0a7e79c-5475-4a7a-9796-fa7c9caba770" />


North/South

<img width="1000" height="760" alt="Screenshot 2026-03-31 at 1 59 13 PM" src="https://github.com/user-attachments/assets/0f987346-495d-4893-bddb-6cb0b29b2ad0" />





