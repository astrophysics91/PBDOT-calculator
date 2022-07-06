# PBDOT-calculator
This code finds the PBDOT by Sklavskii effect, Galactic acceleration, and GW emission via MCMC.

# What you need

a. Parameter file.
b. Mass MCMC generator.
C. expected distance. 



# Detail
For b, you can consider to use the output from TempoNest. Alternatively, you can make the mass array by yourself.
If you just want to find P_{b}

For c, you can provide the distance and its error. The original code uses a fractional error. For instance, let`s assume that the distance is 100 pc. With the fractional error 0.3, your error of the distance is 30 pc.
