# This is my first blog post! 

This is very exciting. As you might have seen, the name of this blog is Maia's Ocean Motion because it details my progress (motion) on my project work (describing ocean motion). The credit goes to my father for coming up with this one.

Okay let's get into it.

## Progress from this past week (Thurs. 10/2-Thurs.10/8)

My main focus this week has been diving into the instrumentation plan and beginning to think about the details of all the instruments I will be using. The M<sup>2</sup> O <sub>2</sub> group has access to the [shared map](https://www.google.com/maps/d/u/5/edit?mid=19WqOTR2bKADb4Jw-watROjY16_MfuRU&ll=48.23290121449544%2C-122.68552805415038&z=13), which is where we have been putitng our instrument location thoughts down by way of pins.
There are three new things that were mentioned this week that we need to consider when thinking about instrumentation plans:
1. The King County mooring that is still measuring data.
2. The cables that are on the seafloor that we cannot place instruments on or between.
3. The SWIFT v4 moorings will have to be in 20m or less as some of the instruments (I believe the ADCPs?) cannot reach further than that, so we will have to be careful where we place those.

For context, King County has a permanent mooring located at the mouth of Penn Cove. This mooring has bottom readings and surface readings.
At the bottom, the instrument collects:
- Date/time
- Temperature (°C)
- Conductivity (sm<sup>-1</sup>, which measures a material's ability to conduct electric current)
- Specific conductivity (sm<sup>-1</sup>)
- Salinity (psu)
- Pressure (dbar)
- Oxygen (mgL<sup>-1</sup>
- Oxygen saturation (%)
- pH
- Chlorophyll (sd of µgL<sup>-1</sup>, which means the standard deviation is being reported)
- Turbidity (sd of ntu, Nephelometric Turbidity Unit, which is the cloudiness of the water caused by suspended particles that scatter light)
- NO<sub>3</sub> (nitrate)
- Also NO<sub>3</sub> in mgnL<sub>-1</sub> and in n, which refers to nitrate levels expressed in terms of the weight of the nitrogen atom within the nitrate ion and is equivalent to mgL<sub>-1</sub>

At the surface, the mooring measures the same properties but also measures atmospheric conditions (at ~2m above the water):
- Wind direction (deg, ~2m above water surface)
- Wind speed (ms<sub>-1</sub>, ~2m above water surface
- Air temperature (°F, and °C)
- Humidity (%)
- Pressure (Hg)

This could be really useful data and is something I think we should build our array setup around if we are able to access the data. If not, then we can work around it.

### Figures
In addition to the shared drive map, I also made a map from data and code Jim provided (thanks, Jim!) of the bathymetric data for Penn Cove and the location of the King County mooring.
![Map of Penn Cove with isobaths and coordinating color variation with the King County mooring plotted in red.](https://github.com/maiaheffernan/maiaheffernan.github.io/blob/main/_posts/PennCoveandBay_withKCmooring.png "Penn Cove bathymetry with King County mooring")

Here, the isobaths are plotted every 10 meters. As I introduced above, the SWIFT v4 moorings will have to be between the 10-20m isobaths.

The other aspect that we need to consider is the cables that run through Penn Cove. 

![Map of Penn Cove with the cables plotted as dashed lines](https://github.com/maiaheffernan/maiaheffernan.github.io/blob/main/_posts/image.png "Penn Cove cables")

Thank you NOAA, Christie, and Jim!
I have found the data files for these cables and plotted them up in Python (they match the picture here!).

![Map of the cables in Penn Cove. They are shaded gray lines in a lat/lon coordinate grid](https://github.com/maiaheffernan/maiaheffernan.github.io/blob/main/_posts/PennCove_cablesPlot.png "Penn Cove cables") 

#### Next steps for plotting
My next plan is to overlay the two plots I made so that we can get the cable, bathymetry, and King County mooring data all from the same figure. I think this will be hlpeful when determining final lat/lon positions and will be hlpeful in future presentations.
Please let me know i something like this already exists that would be more helpful, though!

### Meetings
- Tia and I met with Christie to get a brief introduction to ROMS and using the command line to work with Live Ocean code. This was really helpful as this is a daunting task by itself! I am hoping to get more comfortable with it, though it will not be my main priority for the time being because I am a bit more focused on the instrumentation side at the moment.
- Aurora, Dakota, Tia and I have yet to set up our first journal club but I know it's coming soon!

## Looking forward
There are a few things that I want to get done this coming week:
- Re-read Parker's TEF paper-- I feel like these concepts will really apply when thinking about the data we might get from the instruments regarding Skagit plume intrusion!
- Continue to refine instrumentation setup, I made some comments on Jim's updated placements in the Drive, but I am sure there will be more things to think about/revise after our meeting on Thursday!
- Continue with my python plotting adventure
- Start getting comfortable with the DO sensors, especially how the optical aspects work (looking at manuals, maybe looking at current instruments in the lab if there are any, etc.)
- Work a bit on getting more comfortabe with command line work


