# Second bucket test of the miniDOTs 

This week Tia and I conducted a second bucket test of the miniDOT loggers because the data was really funky from last week. You might recall that the oxygen values decreased by an entire mg/L over the course of 3 hours, which was really strange. Just in case this was a real signal, we decided to chage up the methods this time around. Many thanks to Kate for the brainstorming help!

### New methods

This time we used fresh tap water from the hose in the lab. Since this is municipal water I am hoping that there is nothing living or decomposing in it that might draw down oxygen (fingers crossed for many reasons there).
After doing some inventory in the lab it turns out we do not have a bubbler and the stir plate is very small and made of thin plastic so I did not feel confident in putting a 5-gallon bucket filled with water on top of it. So instead of having the water continually circulating we decided to stir it up at one point to see the effect this had on the dissolved oxygen values. We also added ice a little while later to cool the water down. Since oxygen solubility decreases with warming water temperatures we were hoping to see an increase in oxygen after adding ice. 
All in all the sensors were in the bucket for 2.5 hours with a lid on top, but not locked down onto the rim of the bucket so oxygen could still get through. I also put my rain jacket over the bucket to minimize any light interference with the optodes just in case this is important. Below is a photo of the setup.


<figure>
  <img src="/_figures/ice_sensorSetup.png" alt="Description of image">
  <figcaption>Figure 1. MiniDOT and RBR T.ODO setup with ice added about an hour after the test was started.</figcaption>
</figure>





<figure>
  <img src="/_figures/jacket.png" alt="Description of image">
  <figcaption>Figure 2. Keeping the light out of the bucket.</figcaption>
</figure>



#### Results

**Dissolved Oxygen**


<figure>
  <img src="/_figures/miniDOT_DOcomp_23Apr2026.png" alt="Description of image">
  <figcaption>Figure 3. Dissolved oxygen comparison between the miniDOTs and the RBR T.ODO sensor.</figcaption>
</figure>


Okay so some good and bad here. First, when we stirred the bucket the DO concentration increased across all sensors. This is what we expected to happen so this is good. The initial DO values before we stirred the bucket spread about 0.2-0.3 mg/L which is within the spec range of the DO values. The DO values from the miniDOTs are generally higher than the T.ODO values in this first part of the test before we stirred the bucket but then the values are a bit over the map but generally smaller than the T.ODO oxygen concentrations after we stirred everything. This spread isn't great, but it is not totally unexpected given that we know these aren't the most accurate sensors.

What concerns  me, though, is that when we put the ice in the bucket the T.ODO concentrations increased whereas the miniDOT values all decreased, some by 1 mg/L. Eventually all the measurement values evened out to a more realistic level between the T.ODO and the miniDOTs, but the initial opposite trends are a bit concerning. I do not think that the dissolved oxygen concentrations will drastically change within a 5-10 minute period but the discrepancy and the fact that the miniDOTs showed the exact opposite trend from what we expect both scientifically and in terms of matching with the RBR are disconcerting.


**Temperature**

<figure>
  <img src="/_figures/miniDOT_Tempcomp_23Apr2026.png" alt="Description of image">
  <figcaption>Figure 4. Temperature comparison between the miniDOTs and the RBR T.ODO sensor.</figcaption>
</figure>


This pattern looks a lot more realistic and I am really happy to see that all the values line up nicely together. The lag in the temperature drop makes sense because it takes time for the ice to melt and the thermistors have a 5 minute response time.


### Takeaways

Well we knew the miniDOTs were not great. The dip in DO concentration when it should really be an increase is concerning, though I don't think there is much we can do about this. The temperature looks good, though!

### Plan for this week

I've got a few lofty goals for this week!

- retest the T.ODOs again now that the optodes have been rehydrated
- serial program the RBR Concerto
- finish the sampling plan document
