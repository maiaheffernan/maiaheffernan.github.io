# Looking at time series with Everett tidal data

As I discussed in my other blog post today, the Penn Cove NOAA tide data do not have harmonic constituents and only have data for the high and low tides. Alex suggested using the Everett tide data until we get detailed pressure readings from the Duo at the bottom of one of the SWIFT moorings. I will do this now!

First, I compared the continuous tide data from Everett through the entire month of May to the high and low tide data from Penn Cove in the same time period. I wanted to see if they are comparable locations since Penn Cove is farther north than Everett and has a weird structure which might affect tidal propogation.

<figure>
  <img src="/_figures/EverettVsPenncove_tides.png" alt="Description of image">
  <figcaption>Figure 1. Comparison of the tides from the NOAA Everett tide gauge (station # 9447659) and Penn Cove (station # 9447929) tide gauge. These datasets are for the entire month of May, 2026 and are reported in MLLW. </figcaption>
</figure>
<br><br>

It looks like the timing of the highs and lows match up pretty well. If you look closesly you will see that the Penn Cove station highs and lows are slightly behind the Everett station. Also, the Penn Cove highs tend to be higher than the Everett highs, and the lows are sometimes lower and sometime higher at Penn Cove. For instance, the high on May 13 is at 09:24 in Everett and has a tidal elevation of 3.23m whereas the high in Penn Cove is not until 09:39 on the same day and the tidal elevation is 3.44m. Though it is not perfect, this is good enough for using in the initial time series of salinity, temperature, and DO from the SWIFT telemetry.
