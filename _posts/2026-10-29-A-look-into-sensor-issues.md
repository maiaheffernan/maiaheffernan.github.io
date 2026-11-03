# Fantastic sensor issues and how (I am trying to) to fix them 

For the most part the data collection for Penn Cove went swimmingly. With about 85 sensors, I am impressed by the amount of things that went right and I cannot wait to start digging into the data. 

There are, of course, a few issues that we have run into with the data. In this blog post I focus specifically on 1) the casting CTD sampling rate issue and an update on how fixing that issue is going, 2) assessing whether a scratched DO sensor on the Wire Walker south Concerto gave bad data. 


## Starting with the casting CTD progress

Based on what Alex found and what RBR said it seems the CTD was actually logging somewhere around 20.7-20.8 Hz. In my own exploration with Claude I found from the raw data that the timestamps are not all individually sampled. Like Alex's Claude session indicated the sensor uses the start time and then the sampling rate to construct the more miniscule timestamps. It also records the offload timestamp, but this is not super helpful. Without knowing the actual timestamps it is hard to get at the actual sampling rate because as we have found the sensor is self-consistent, and therefore it is difficult to know the exact stretching value that should be applied to the timestamps.

So, without knowing the true timestamp the fix gets a little tricky. I used claude to help me create this function that relates the CTD to the ADCP data. Essentially the function finds how deep each CTD cast went, according to the incorrect clock. It then read in the raw ADCP data from WinADCP and computes the seafloor depth from the four beams and adds the transducer depth so that the ADCP depth is referenced from the surface like the CTD. 

Assuming that the best way to determine the correct CTD time stamp. The corrected time should be t_corr = t0 + (t_i - t_0)*x where t_i is each time value from the CTD, so essentially t_i - t_0 is the duration from the start time. The x variable is the stretch factor needed to fix the time. Using the ADCP, the basic idea is that the deepest measurement of each CTD cast should track the bottom pretty well. So the function tries many stretch factors, x (from 1.3 to 1.8). For each of these points, the function moves every profile's deepest point to its "corrected time", looks up the ADCP bottom depth at that time, and then calculates the correlation between those two values. The x value with the highest correlation wins, and then the true rate is 32/x. It also reports how wide the correlation peak is which gives the uncertainty. 


I tried doing this with the September ebb casting data.

Here are the values that the function came up with :

samples: 285366   nominal rate: 32.000 Hz   nominal duration: 8917.7 s
  ADCP (raw WinADCP): bottom depth = mean of 4 beams + transducer depth; median beam spread 0.86 m
  ADCP: 477 ensembles, 12:20:16 -> 16:18:16, 88% with valid bottom depth
  true rate: 20.7657 Hz (from ADCP match)   x = fsNominal/fsTrue = 1.54100
  ADCP match at this x: r = 0.862
  x within 5% of best correlation: 1.5360 - 1.5455  (rate 20.71 - 20.83 Hz)

Logging (corrected, UTC): 2026-09-23 12:27:15.375  ->  2026-09-23 16:16:17.482
Logging (as recorded)   : 2026-09-23 12:27:15.375  ->  2026-09-23 14:55:53.031


The ending timestamp is certainly more correct here. Especially given that the CTD is offloaded about 2 minutes later according to the log. 

Here are some plots from this:



















## Now for the bad DO sensor 

When we recovered Wire Walker south, we noticed that the optode on the Coda, the optical dissolved oxygen sensor, that was attached to the RBR Concerto was scratched. This is an issue because there is a really delicate foil on the top of the optode that quenches oxygen molecules from the water. When taking a measurement the sensor shines a light at the optode and foil. Depending on how many oxygen molecules are quenched by the foil, the frequency of the light that is returned to the sensor changes from the ping the sensor sent originally. The sensor then makes an internal calculation of the dissolved oxygen % saturation value based on the shift in light frequency. As you can imagine, if there is no/foil because it got scratched off the oxygen measurement is likely to be corrupted. 

Below I take a closer look at the oxygen data from this sensor. 
