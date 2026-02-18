# Profiles of CTD parameters at the currently planned mooring locations

These past few weeks I have been working on wrangling the CTD data to clean it up and use it confidently. As it turns out Ruskin has a great code tool set that walks thorugh functions they have written for this in MATLAB and Python. I guess this is a lesson to me to do a bit og digging before jumping into the data and trying to brute force my way through QAQC. 

The CTD data in the following analysis has been cleaned as such:
- Only looking at the down casts.
- Puts NaNs in the data where the instrument might have been recalibrating during/in between uses (this likely does not apply for our situation but I incorporated it anyway).
- Low-pass filtered.
- Aligns the time steps of the different sensors (the thermistors read SLIGHTLY slower than other sensors so it adjusts this small lag).
- Alignment of conductivity and temperature because these are co-located on the instrument and can sometimes read a different water parcel. This essentially estimates the optimal lag between conductivity and temperature by minimizing salinity spiking.
- Removes any loops from the data (loops being if the CTD "bounced" in the water column during a cast)
- Derives salintiy and sea pressure.
- Bin averages all channels by sea pressure in order to remove measurements taken when the instrument is profiling too slowly or during rough conditions or a pressure reversal.

Yay clean data!

## Profiles at the mooring locations

Here is the current plan for the mooring locations:

<img alt="PennCoveArray_21Jan2026_draft" src="https://github.com/user-attachments/assets/c5dc49c0-7e02-4199-9ccd-e241d3a2bcfd" />

### Average profiles

#### Overall

Before we even get into the different transect lengths or the mooring locations themselves, let's look at the average profiles for the entirety of Penn Cove.

<img alt="Figure 1. Overall_averageProfiles" src="https://github.com/user-attachments/assets/a0f776bd-6702-42a2-ab6f-a634d2539bae" />


The red lines are the average values and the grey lines are all the different profiles that got averaged together. Not much to say here except that the dissolved oxygen is doing weird things like we thought!


#### Per transect location

I matched up the lat/lon coordinates with the ADCP data to section off the profiles for each lap section. So I have the all the profiles from the entrance, south end, back bay, and north end. I used the third lap to pull these locations as the third lap had the longest transect time so there were more lat/lon data points collected. Here is a map of hte transect line and the profile locations along its path that were used for these next few plots:

<img alt="Figure 2. ProfilesOnADCPTrack" src="https://github.com/user-attachments/assets/7f461639-0baa-461f-9d37-6b7a9835a1f8" />


From this, I took the average profiles from the entrance line, the southern end line, the back bay line, and the north end line. Since we sampled in these locations many times, these are not necessarily time dependent *(though they likely are in fact time dependent, but I am not getting into that quite yet. Any thoughts about how to pull that apart would be helpful).*

In the plot below the red bar is the average profile for that tansect line and the grey shading shows the standard deviation.

<img alt="Figure 3. AverageCasts_perTransectLocation_STD" src="https://github.com/user-attachments/assets/c0fb3769-84df-4605-8a33-4653d861f78b" />


There are a few things here:

1) There is a lot more deviation in the DO values throughout a transect section than there are in the salinity and temperature values throughout a transect section. In some instances it deviates by almost 2 mg/L which is a large amount, especially when considering hypoxia.
2) In the temperature and salinity there is the most deviation in the surface values and around the mixed layer depth. Is this real-world or more careful data processing that needs to happen? I am considering both, but thoughts would be helpful.
3) We can see the clear 10m mixed layer here in the temperature and salinity profiles.
4) What is REALLY interesting is that we can clearly see the low-DO level around 15m deep in the water columns. In the south length of the bay this is pretty dramatic: there is a reduction and then a rebound of almost 2mg/L of oxygen at this depth. This reduction happens at other locations but it is a lot smaller. Honestly I need to bring together some other data to make a sound hyposthesis about why this is happening most drastically in this southern end. Maybe it is bathymetry related? Maybe Long Point is doing something to the water column? Hard to say, but here are my **next steps for this: bring in velocity profiles at same locations/same averages, figure out tidal timing of all this-- time series, profiles at peak ebbs, floods, highs, and lows, bring in the bottom data: are we reaching all the way to the bottom??**
5) Final point here: we can see that the DO levels are generally higher on the entrance line. This is in line with what we have seen before.


### Mooring location profiles

First, let's look at the singular profiles at each charted mooring location. We are going to look at salinity, temperature, and DO separately.

**First salinity:**


<img alt="Figure 4. SalProfiles_singluarMooringLocs" src="https://github.com/user-attachments/assets/54c895f6-4bce-43d9-b9c9-cd187b971edf" />

Some takeaways:
1) The mixed layer seems to extend slightly deeper in the back bay north and the LoveJoy north sites. I am still trying to convince myself of this, bu there might be an interesting pattern here!
2) There is a lot of stepping of salinity values, especially just below the mixed layer, even after low-pass filters. **What I really need to do here is find out when each of these profiles was taken. What if they were taken at different tidal stages? That is a worrying thought.**
3) Also the higher saliniy at the surface (~18 PSU) are a bit confusing now that I look at it. I wil have to go back and compare to the other salinity plots I've made.

**Now temperature:**

<img alt="Figure 5. TempProfiles_singularMooringLocs" src="https://github.com/user-attachments/assets/64059a35-f428-4b48-9f2a-8abfe0523d3a" />


Some takeaways:
1) Sinimlar results to salinity! Now that I am realizing the tidal stages might not line up, however, I am a bit more trepedatious.
2) What is interesting is that at LoveJoy south, wire walker north, and wire walker south we see a temperature increase around 15m, which is where that low DO signal in the other transects is. Let's look more closely.

**DO profiles:**

<img alt="Figure 6. DOProfiles_singularMooringLocs" src="https://github.com/user-attachments/assets/ddb77d5c-b0b4-4a0d-a2f9-c4a4fb842f5e" />

Takeaways:
1) That 15m intrusion really comes through in all the profiles. The back bay sites are just too shallow to show the trend I think, but they look like they might be tendig in a similar pattern as the rest of the bay.
2) There is definitely something funky with the LoveJoy South profile: What is there a DO increase at 15m? This looks too sharp and too narrow a band to be trustworthy to be real. Also in the average profiles form the southern transect this is where a decrease happens, not an increase. There is a large standard deviation in the average plot, so that could be explaining this opposite trend we see. Hard to say without digging into it.
3) It is interesting that this intrusion looks to be happening even outside Penn Cove at the wire walker sites. This tells me that is definitely something to do with the water coming in. **Time for velocity from the Echo Sig and the SWIFTS next!!**


#### Comparing the mooring locations

For this next plot I am comparing the above profiles to each other at leach location. 

<img alt="Figure 7. SalTempDO_allProfiles_noavg" src="https://github.com/user-attachments/assets/7eee6953-7ed2-4164-aa15-f6732e0c518d" />


Here, I do the same comparison as above but I averaged the 5 nearest values to the profile, so there is a bit more consideration of the water column around each mooring. I am currently working on getting the corect standard deviation bars on there, so that will be in the next installment. But for now please enjoy the comparison:

<img alt="Figure 8. MooringAverageCast_noSTD" src="https://github.com/user-attachments/assets/1bd75a76-029a-48cf-9be0-6c971035ecde" />


Some takeaways:
1) The **temperature** profiles seem to be pretty united at all the mooring locations. This is helpful! The homogenization at the surface and the bottom tells me that the boundary conditions in the water column are being affected in the same ways, and the slight variation in values at the different mooring locations likely comes from flow (obvious, but good to see I guess). Also, if zooming out, Penn Cove is relatively small and definietly enclosed, so it makes sense to see similar temperatures. To be fair, though, when we were out on the boat the wind was blowing pretty hard, so it makes sense that we might see similar temperatures from mixing. I am curious as to what this might look like in the summer.
2) The **salinity** profiles also are pretty similar, though we do see that the inner bay profiles tend to be slightly saltier than the lovejoy line and the wire walkers. Could this be from river water not propogating as far back like we saw Dakota's plots from last week? This is my going hypothesis.
3) I have a tiny formation of a thought that could be totally wrong: since the salinity is mostly but not fully homogneous and the temperature is homogenous that maybe the temperature and salinity signals are not necessarily driven by the same mecahnism. For instance, maybe temperature is driven by the atmospheic forcing and the salinty is driven by river inflow.
4) The **dissolved oxygen** levels are all over the place and we start to see the variation after the mixed layer ends. There is a lot here. First, the southern sites, which are the dotted lines, always have less DO than their northern coutnerparts. Second, the LoveJoy and wire walker sites, especially in the northern end, have a similar DO profile. This kind of makes sense if we are imagining that the flow into the bay will go past the wire walker north site and then to the LoveJoy north site. Their southern counterparts are somewhat similar, but we see that the LoveJoy south profile has a lot less DO than the wire walker south location. Comparing the northern and southern parts of these two sites again: the "rebound" in DO levels at depth after the 15m minimum is less extreme at the northern sites than it is at the southern sites, particularly at the wire walker sites. Finally, we see that the inner bay DO levels are the lowest. This is consistent with what we have seen before.



#### Final thoughts

**To tie all this back to the mooring plan:**
- We need to make sure we have sensors at the 10m and 15m marks to capture the mixed layer and the weird DO minimum points. Will these features be there in the spring/summer/early autumn? Hard to say, but based on what we have it would be interesting to find out.
- It seems like those inner bay locations are kind of doing their own thing. This resonates with Dakota's movies/quiver plots she showed last week. In terms of what sensors to put where, it is hearteneing to see that the northern and southern ends of the inner bay are not too different. So, this is sort of another vote in favor of the motion to put those YSIs on the LoveJoy SWIFTS instead of the mussel beds like we are planning.

**Next steps with this analysis**
- I will be including velocity profiles! This has been neglected for too long and will likely help tell us what is going on.
- I want to make a time series of this data to see how it changes with the tides. *I might need help sorting through the altimater issues from the SWIFTs as I try to make our own tidel patterns for the bay.*
- I am going to look at the timing of the profiles for the different mooring locations. If they are at different tideal stages then this whole thing breaks down. I am pretty sure that they are not because I pulled the nearest lat coordinate from the CTD casts to the ADCP location, and this pulled only one coordinate reading, so I assume it is static. But it would be nice to know when this static even occured.

**Other next steps**
- I have a large sampling plan to write up by March 1st! You will find me deep in the bowels of Word in the next couple weeks.















