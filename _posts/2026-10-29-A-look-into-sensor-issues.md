# Fantastic sensor issues and how (I am trying to) to fix them 

For the most part the data collection for Penn Cove went swimmingly. With about 85 sensors, I am impressed by the amount of things that went right and I cannot wait to start digging into the data. 

There are, of course, a few issues that we have run into with the data. In this blog post I focus specifically on 1) the casting CTD sampling rate issue and an update on how fixing that issue is going, 2) assessing whether a scratched DO sensor on the Wire Walker south Concerto gave bad data. 

## Starting with the bad DO sensor because it is somewhat less involved than the casting CTD

When we recovered Wire Walker south, we noticed that the optode on the Coda, the optical dissolved oxygen sensor, that was attached to the RBR Concerto was scratched. This is an issue because there is a really delicate foil on the top of the optode that quenches oxygen molecules from the water. When taking a measurement the sensor shines a light at the optode and foil. Depending on how many oxygen molecules are quenched by the foil, the frequency of the light that is returned to the sensor changes from the ping the sensor sent originally. The sensor then makes an internal calculation of the dissolved oxygen % saturation value based on the shift in light frequency. As you can imagine, if there is no/foil because it got scratched off the oxygen measurement is likely to be corrupted. 

Below I take a closer look at the oxygen data from this sensor. 
