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

<img width="1415" height="558" alt="PennCoveArray_21Jan2026_draft" src="https://github.com/user-attachments/assets/c5dc49c0-7e02-4199-9ccd-e241d3a2bcfd" />

### Average profiles

Before we even get into the different transect lengths or the mooring locations themselves, let's look at the average profiles for the entirety of Penn Cove.

<img width="1446" height="1031" alt="Overall_averageProfiles" src="https://github.com/user-attachments/assets/a0f776bd-6702-42a2-ab6f-a634d2539bae" />

