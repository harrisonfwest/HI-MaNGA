Running To-do list:
1. Create clear documentation for the usage of David Stark's statistical code wrapper (`survival_analysis.py`).
Some challenges that arise with this code are the installation of R dependencies on the system and the references 
made to online sources for the R software being implemented.
2. Graphics to refine: HI Gas Fraction vs. Stellar mass for each population (co-plotted); 
CDF of HI richness from Kaplan-Meier; Line used to calculate deficiency should be on HI fraction plot
3. Start writing research note (overleaf)

Recap:
.fits file of galaxies is imported with columns for stellar and gas masses (detections and upper limites),
RA/DEC, SFR, and position angles of stellar and gas discs. This allows us to calculate the amount of misalignment 
between the stellar and mass discs. From stellar and gas masses, we can calculate gas mass fraction, and separate
the galaxies into aligned and misaligned galaxies. From this, we can fit binned average trends to the gas mass fractions
of each galaxy set. We see that surprisingly, the misaligned galaxies have less HI gas than their aligned counterparts.
We confirm this trend with CDFs, along with plots and CDFs for HI depletion time and SFR for both galaxy sets.