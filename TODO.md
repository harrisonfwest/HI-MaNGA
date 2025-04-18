Running To-do list:
1. Create clear documentation for the implementation and usage of David Stark's statistical code wrapper. Some challenges
that arise with this code are the installation of R dependencies on the system and the references made to online 
sources for the R software being implemented.
2. "Punchy" graphics to refine: HI Gas Fraction vs. Stellar mass for each population (co-plotted); 
CDF of HI richness from Kaplan-Meier; Line used to calculate deficiency should be on HI fraction plot
3. HI depletion time: MHI / SFR --> yrs, how long the galaxy can sustain its current SFR; and CDF for depletion time
4. HI richness: overlay fits
   #Huang et al. 2012 line of best fit (f1 below logM=9, f2 above)
   logM=stellar mass array
   fpred = 0.712 * logM + 3.117 - logM
   fpred[logM>9] = 0.276* logM[logM>9] +7.042 - logM[logM>9]
   HIrich = Mfrac - fpred
   Then run CDF code on HIrich including upper limits.
5. Research note overleaf