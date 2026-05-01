# Comparing three different bucket tests of the RBR T.ODO duets 

The RBR Duets have been giving me some issues as we all know by now. In this writeup I compare the results from three separate bucket tests. I think it is time to move forward with the two-point user calibration that is detailed in the RBR manual that was recommended to me by the folks up here in an email last week. I will walk through my reasoning below.


## Test 1, April 8

You might recall that I performed this test in a bucket of seawater 2 sensors at a time and did three different rounds of testing. I helpd the two sensors in the bucket for 2 minutes in each round. The range in dissolved oxygen values were concerning, so I reached out to RBR with a report and they suspected the optodes were not hydrated and suggested I hydrate them for at least 5 days and re-try the test and then perform a two-point calibration if things looked a little funky after that second test. Below are the plots from round 1.

**Note: Spec sheet accuracy ranges**
-   **Temperature: +/- 0.002 deg C**
-   **Optical DO: +/- 8µmol/L (0.2560 mg/L assuming a molar mass of 32 g/mol for O_2) or +/- 5%**
  


#### Round 1

<figure>
  <img src="/_figures/Round1_plots.png" alt="Description of image">
  <figcaption>Figure 1. Temperature and dissolved oxygen in Round 1 for the T.ODO pairs.</figcaption>
</figure>



#### Round 2

<figure>
  <img src="/_figures/Round2_plots.png" alt="Description of image">
  <figcaption>Figure 2. Temperature and dissolved oxygen in Round 2 for the T.ODO pairs.</figcaption>
</figure>



#### Round 3

<figure>
  <img src="/_figures/Round3_plots.png" alt="Description of image">
  <figcaption>Figure 3. Temperature and dissolved oxygen in Round 3 for the T.ODO pairs.</figcaption>
</figure>



*Here is what I said about this in a previous blog post:*

I am a little concerned with the DO readings between the sensors. Some of the differences between the values are within a few tenths of a mg/L, but there are a couple sensors, SN 241789 and SN 241790 (second panels in the plots) that are almost 1 mg/L different from each other. This could be pretty significant in our system. The initial accuracy of the dissolved oxygen values for these sensors should be a maximum of +/- 2µmol/L which is 0.064 mg/L. The differences in the vlaues we see here are larger than that. 


## Test 2, April 29

Okay so I think this test is a bit of a fluke. Instead of seawater, I put the sensors in a bucket of fresh water this time. I also used the pressurized air from the shop as a makeshift bubbler. After letting the bubbler aerate the bucket of fresh water for about 10 monites, I put all the sensors in the bucket and let them go for a couple hours with the bubbler still running. I covered the bucket with jackets to keep the light out as these are optical sensors and I did not want any interference. 

A rookie mistake, I did not take a photo of the sensors in the bucket. However, they were all resting in the bucket at an angle with the sensor heads on the bottom of the bucket and all the optical sensors pointing up. As you can see in the figure the values are all over the place and I think this is because some of the sensors were closer to the bubbler than others, so they were reading higher oxygen saturation and concentration values (duh... but I obviously did not think about this in the moment). 

Given this, I did/do not trust the resulting plot, but I figured I would include it anyway.

<figure>
  <img src="/_figures/bucketTest2_duets_flukeTest.png" alt="Description of image">
  <figcaption>Figure 4. Temperature and dissolved oxygen from the second day of bucket testing in the lab.</figcaption>
</figure>




Obviously, the large range in values is concerning. But is this lack of precision real given the setup? This brings us to the third bucket test. Note that between tests the sensors were stored with enough distilled water in their protective caps to ensure the optodes did not dry out.


## Test 3, May 1 

Given my failures from the past two tests I tried to make this setup ideal. I got a bigger bucket: a trash can, to be specific. I also made sure all of the sensor heads were on the opposite side of the trash can from the makeshift bubbler and all the optodes were pointed up. I also staggered the sensors so the heads weren't directly next to each other. See the image below for the setup.

<img width="1170" height="2532" alt="IMG_990B6891D2D9-1" src="https://github.com/user-attachments/assets/c8951caa-eb0c-4704-aca6-13767d19dc60" />


I put the sensors in the bucket after about 10 minutes of bubbling and kept the bubbler going for the next two hours while the sensors sampled at 1 Hz. I also covered the top of the bucket with a dark jacket to minimize light and secured the Duets in that position so they did not move (which I can confirm that they did not move or rotate when I retrieved them).

<img width="344" height="729" alt="Screenshot 2026-05-01 at 4 11 11 PM" src="https://github.com/user-attachments/assets/a684c519-0aa7-4821-9911-c37bb3d49e55" />


Despite my best attempts, the data from this bucket test still do not look good. 


<figure>
  <img src="/_figures/BucketTest3_duets.png" alt="Description of image">
  <figcaption>Figure 5. Temperature and dissolved oxygen from the third day of bucket testing in the lab.</figcaption>
</figure>



The range of DO concentration is especially concerning. Also, I am not sure why oxygen would be decreasing if there is continual bubbling. What it interesting to note is that the sensor that reads really low values in this plot, SN241790, is the same one that read low values in the previous two tests as well. 

I think it is time to do this two-point calibration that RBR suggested. Happy to elaborate more and talk through things next week. 
