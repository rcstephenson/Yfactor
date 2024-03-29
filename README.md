# Y-Factor Measurements

This notebook provides some tools to perform a simplistic Y-factor measurements for some device under test (DUT). For more information regarding Y-factor measurments see ref.1

The governing equations for the Y-factor measurement are as follows: 



<center><p class="aligncenter">
    <img src="https://render.githubusercontent.com/render/math?math=Y%20\equiv%20\frac{P_{hot}}{P_{cold}}%20\left[%20\frac{W}{W}%20\right]"  alt="centered image" />
</p></center>



<center><img  src="https://render.githubusercontent.com/render/math?math=T_{sys} = \frac{T_{hot} - Y \cdot T_{cold}}{Y-1} [K]"></center>

where Y is a _linear_ unitless parameter from measuring the response of the system taken with a hot and cold input load temperature, and <img  src="https://render.githubusercontent.com/render/math?math=T_{sys}"> is the _additive_ temperature of the over all system from some <img  src="https://render.githubusercontent.com/render/math?math=T_{amb.}"> (= 290 K, in our case). To measure the temperature of our device under test more precisely we can take cascaded temperature of our overall system and subtract out the noise of our reciever  to isolate our devices temperature: 

<center><img  src="https://render.githubusercontent.com/render/math?math=T_{dut} = T_{sys}-\frac{T_{recv}}{G_{dut}} [K]"></center>

Where the reciever is all componets following our DUT in the RF chain. Additional corrections to account for losses in the RF-chain and error calculations may be applied as well to further resolve the noise temperature for the device.  

## Refrences

[1] Mike Leffel, Rick Daniel (2021). "The Y Factor Technique for Noise
Figure Measurements." Rhode & Schwartz. Application Note 1MA178 Version 5e.

[2] Pozar, D.M. (2010) Microwave Engineering. 3rd Edition, John Wiley, Hoboken, NJ. 
