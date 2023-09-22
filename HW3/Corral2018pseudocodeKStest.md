# Section 3 

# Goal: compare the distribution of time gaps between earthquakes for magnitude M > Mk with that of  
time gaps between earthquakes of magnitude M > Ml for various values of Ml and Mk.
If a scaling law holds the distributions should be “the same” 
i.e. you cannot rule out that they are drawn from the same parent distribution. 
The KS test is designed to test this last hypothesis.

Before performing the test though, the distributions must be scaled by the average gap time and cleaned of events too close in time.


# pseudocode:

```
For threshold 0.01 and 0.001:
  	For all Mk values of M in Corral2018:
		{
		# remove gaps below minimum gap threshold
		x_Mk =  gaps where M > M_k
		For i in [1,2]: # do it twice
			{
			# Rescale the time gaps distribution by the mean value of the time gaps.
			Rk = 1 / mean of x_Mk
			X_Mk = x_Mk * Rk where x_Mk*Rk  > threshold # can be achieved broadcasting in python
			}
		# these two lines of code are not necessary cause Rk~1
		Rk = 1 / mean of x_Mk
		x_Mk = x_Mk * Rk
		
	For all Mk values of M in Corral2018:
		{
   		For all Ml values of M in Corral2018 greater than Mk
			{
			Perform the KS test on (Mk, Ml)
			}
   		}
