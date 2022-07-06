# PBDOT-calculator

This code finds $\dot{P_{b}}$ by Shklovskii effect, Galactic acceleration, and GW emission via MCMC.
The inputs from the parameter file generate the random array, following Gaussian.
This array finds the mean and standard deviation of each $\dot{P_{b}}$. 


# What you need

a. Parameter file (mandatory).

b. expected distance (mandatory). 

c. Mass MCMC generator (optional).

# Detail

For b, you can provide the distance and its error. The original code uses a fractional error. For instance, let`s assume that the distance is 100 pc. With the fractional error 0.3, your error of the distance is 30 pc.


For c, you can consider to use the output from TempoNest that includes the posterior of the companion mass. Alternatively, you can make the mass array by yourself. If you just want to find $\dot{P}_{b,int}$ by subtracting the obtained $\dot{P_{b}}$ from the Shklovskii effect, Galactic acceleration, you can use the option, subtract_only=True in PK.pbdot() function, additionally. 

