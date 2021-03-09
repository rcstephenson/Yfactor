# Y-Factor Measurments

This notebook provides some tools to preform a simplistic Y-factor measurments for some device under test (DUT). For more information regarding Y-factor measurments see ref.1

The governing equations for the Y-factor measurment are as follows: 

<img src="https://render.githubusercontent.com/render/math?math=Y%20\equiv%20\frac{P_{hot}}{P_{cold}}%20\left[%20\frac{W}{W}%20\right]">


<img  src="https://render.githubusercontent.com/render/math?math=T_{sys} = \frac{T_{hot} - Y \cdot T_{cold}}{Y-1} [K]">

where Y is a _linear_ unitless parameter from measuring the response of the system taken with a hot and cold input load temperature, and $T_{sys}$ is the _additive_ temperature of the over all system from some $T_{amb.}$ (= 290 K, in our case). To measure the temperature of our device under test more precisely we can take cascaded temperature of our overall system and subtract out the noise of our reciever  to isolate our devices temperature: 

<img  src="https://render.githubusercontent.com/render/math?math=T_{sys} =T_{dut} = T_{sys}-\frac{T_{recv}}{G_{dut}} [K]">

Where the reciever is all componets following our DUT in the RF chain.

## Refrences

[1] Mike Leffel, Rick Daniel (2019). "The Y Factor Technique for Noise
Figure Measurements." Rhode & Schwartz. Application Note 1MA178_4E. https://scdn.rohde-schwarz.com/ur/pws/dl_downloads/dl_application/application_notes/1ma178/1MA178_4e_NoiseFigure.pdf

[2] Pozar, D.M. (2010) Microwave Engineering. 3rd Edition, John Wiley, Hoboken, NJ. 