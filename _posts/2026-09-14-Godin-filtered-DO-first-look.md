# Applying a Godin filter to the dissolved oxygen data


I am new to the world of Godin filtering and really only understand it from a theoretical level. Here is where my understanding is at: the Godin filter applies two 24 hour and one 25 our low pass filters to a dataset so that only tidal modulations on frequencies lower than these will remain in the data. This filtering is done by averaging the values in these bands *(not sure about any of this)*.

<br><br>

Once I pull out these time windows I will be able to see the larger-scale / longer time scale modulation of a given variable in time. In this case I am trying to understand how or even if bottom dissolved oxygen varies with the tides in Penn Cove. The idea comes from the Deppe et al. 2018 paper in which perigean signals in DO concentration were observed in Admiralty Inlet. From this, we were wondering if the oxygen levels at the bottom of the water column in Penn Cove also experience perigean cycling. 

<br><br>

Specifically, we are wondering two things: 
1) If there are larger fluctuations in the DO that are stronger during the first spring tide of the month, weaker during the neap tide, and then slightly larger but weaker fluctuations in the second spring tide season when compared to the first spring tide season.
2) If there is a bottom oxygen renewal forced by some function we do not yet know about. From squinting at the time series of oxygen it appears that there is a set level at the start of the month, a decline in oxygen levels, then a renewal in oxygen levels and then a steep and steady decline from there that carries on into the next month where this same pattern exists.


Let's look at the time series to see if there is an obvious signal fluctuation in the data.


## Godin filtered bottom dissolved oxygen plots


First, here is the full time series.



