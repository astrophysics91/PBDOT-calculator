# PBDOT-calculator

There are three different factors (Shklovskii effect, Galactic acceleration, and Gravitational wave damping) that affect the observed orbital period change ($\dot{P_{b}}$) in a pulsar binary.
To find each, complicated equations should be solved.
This code uses a numerical method to calculate different $\dot{P_{b}}$ effects.
The code requires a parameter file to read the related values and uncertainties of timing parameters.
This code measures values and errors based on the mean and standard deviation of probability density distributions.

# What you need

a. Parameter file (mandatory).
- please provide *par file in Tempo2 format.

b. expected distance (mandatory).
- you can modify this in the code. The uploaded version uses iteration of the distance, "d=np.linspace(655,1200,6)".
- This code uses a fractional error of the distance
- eg) 100 pc with 0.3 means that the uncertainty of the distance is 30 pc.

c. Mass MCMC generator (optional).
- If you have mass probability distributions obtained from TempoNEST, you can provide this.
- Alternatively, you can make the mass array by yourself. If you just want to find $\dot{P}_{b,int}$ by subtracting the obtained $\dot{P_{b}}$ from the Shklovskii effect, Galactic acceleration, you can use the option, subtract_only=True in PK.pbdot() function, additionally. 

d. Python packages
- Astropy, numpy, and pandas

# Others

This code will be upgraded constantly to persue user-friendly interface and description. 
If you have any comments, please mail to me (** jjang@mpifr-bonn.mpg.de).

If you use this code, please cite the paper (It is still under review. Submitted to A\&A)

# Reference:

Abuter, R., Amorim, A., Bauböck, M., et al. 2021, Astronomy Astrophysics, 647, A59

Damour, T. & Taylor, J. H. 1991, ApJ, 366, 501

Eilers, A.-C., Hogg, D. W., Rix, H.-W., & Ness, M. K. 2019, The Astrophysical Journal, 871, 120

Guo, Y. J., Freire, P. C. C., Guillemot, L., et al. 2021, A&A, 654, A16

Hobbs, G. B., Edwards, R. T., & Manchester, R. N. 2006, Monthly Notices of
the Royal Astronomical Society, 369, 655

Holmberg, J. & Flynn, C. 2004, MNRAS, 352, 440

Lazaridis, K., Wex, N., Jessner, A., et al. 2009, Monthly Notices of the Royal Astronomical Society, 400, 805–814

Lorimer, D. R. & Kramer, M. 2004, Handbook of Pulsar Astronomy, Vol. 4

Shklovskii, I. S. 1970, Soviet Ast., 13, 562
