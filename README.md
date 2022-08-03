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

This code will be upgraded constantly to persue user-friendly interface. If you have any comments, please mail to me :D



# Reference:


Abuter, R., Amorim, A., Bauböck, M., et al. 2021, Astronomy Astrophysics,
647, A59
Damour, T. & Taylor, J. H. 1991, ApJ, 366, 501
Guo, Y. J., Freire, P. C. C., Guillemot, L., et al. 2021, Astronomy Astrophysics,
654, A16
Holmberg, J. & Flynn, C. 2004, MNRAS, 352, 440
Lazaridis, K., Wex, N., Jessner, A., et al. 2009, Monthly Notices of the Royal
Astronomical Society, 400, 805–814
Shklovskii, I. S. 1970, Soviet Ast., 13, 562
