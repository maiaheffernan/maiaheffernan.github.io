# Applying a Godin filter to the dissolved oxygen data


I am new to the world of Godin filtering and really only understand it from a theoretical level. Here is where my understanding is at: the Godin filter applies two 24 hour and one 25 our low pass filters to a dataset so that only tidal modulations on frequencies lower than these will remain in the data. This filtering is done by averaging the values in these bands *(not sure about any of this)*.


Once I pull out these time windows I will be able to see the larger-scale / longer time scale modulation of a given variable in time. In this case I am trying to understand how or even if bottom dissolved oxygen varies with the tides in Penn Cove. The idea comes from the Deppe et al. 2018 paper in which perigean signals in DO concentration were observed in Admiralty Inlet. From this, we were wondering if the oxygen levels at the bottom of the water column in Penn Cove also experience perigean cycling. 

Specifically, we are wondering two things: 
1) If there are larger fluctuations in the DO that are stronger during the first spring tide of the month, weaker during the neap tide, and then slightly larger but weaker fluctuations in the second spring tide season when compared to the first spring tide season.
2) If there is a bottom oxygen renewal forced by some function we do not yet know about. From squinting at the time series of oxygen it appears that there is a set level at the start of the month, a decline in oxygen levels, then a renewal in oxygen levels and then a steep and steady decline from there that carries on into the next month where this same pattern exists.


Let's look at the time series to see if there is an obvious signal fluctuation in the data.


## Godin filtered bottom dissolved oxygen plots
<br><br>

### First, here is the full time series.

<br><br>
<figure>
  <img src="/_figures/AllMonths_allMoors_godinDO.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 1. Godin filtered data from the bottom dissolved oxygen sensors at all four mooring locations in the cove. </figcaption>
</figure>
<br><br>

Without needing to squint this time it is clear that there is a peak in oxygen levels at the beginning of the month that then falls to a low point, then gets renewed and falls again near the end of the month. There is no discernible trend in this pattern between the moorings, meaning that there is no mooring location that seems to consistently have higher peaks or lower troughs or even larger DO values form month to month. The only observable thing is that the pattern of rising and falling DO levels seems to be similar between the moorings from May to June and that the hypoxic season really drags everything down beginning in mid-jury and continuing on through August. Despite the lower oxygen values, though, this rising and falling pattern is still somewhat evident. Note, however, that throughout the entire time series the DO values do not drastically fluctuate. These rises and renewals are only around 1-2 mg/L in each month. 

<br><br>

I pulled out the months individually in order to see this pattern with the tidal signals.

## A closer look at each month


### First May to June

<br><br>
<figure>
  <img src="/_figures/MayJun_godinDO_withTide.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 2. Godin filtered data from May to June in Penn Cove. </figcaption>
</figure>
<br><br>

Frankly, I am not sure what mooring this is. This is something I need to go back and look at in my code. The pattern here with the SSH is interesting, though. The first dip in DO seems to be during what I assume to be the neap tide, then it jumps up with the onset of the spring tide, eventually dipping down again in the middle of the spring tide, rising again when the spring weakens, and then falling with the onset of what I assume to be the neap tide. What could this be?? Could it be that there is more estuarine exchange during the neap tide that then shows a lagged increase in DO levels? Then with more tidal exchange the low DO water gets spun around in Penn Cove with the weird two-circulation cell structure we think exists in the cove? Maybe increase estuarine exchange helps flush the entire cove and the weird tidal dynamics trap it? If this is the case, though, how is it that there is a second bump in oxygen levels during the largest tides of the time series? I honestly have so many questions and 0 answers.

Here is what would be helpful for the next installation of this plot: 
1) Figure out which mooring this is
2) Plot the velocity from this SWIFT mooring to help show how the velocity changes with the different tidal phases. Are they stronger or weaker at different times?
3) This is more of a question: should I plot stratification? Would that help or be distracting?


<br><br>

<br><br>

### June to July


<br><br>
<figure>
  <img src="/_figures/JunJul_godinDO_withTide.png" alt="Description of image">
  <figcaption class="fig-caption">Figure 3. Godin filtered data from June to July in Penn Cove. </figcaption>
</figure>
<br><br>

Okay it looks like similar overall timing with the previous month, which is cool. But now LJN seems to be on its own journey with no discernible trend. Could it be that it is just so affected by the tides there that there is no weakening of the tidal circulation at all? Honestly I am thinking stratification might be important for this because the river really stopped producing high discharge right around this time (**CHECK THIS**). Again, velocities would be helpful here. I should plot all of them in subplots along with the stratification at each mooring.

Here is what else is missing:
- I need a true tidal harmonic analysis. When are the true spring and neap times?
- I need the rest of the mooring data from MAyJun and the data from JulAug



