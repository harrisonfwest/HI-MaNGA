Running To-do list:
1. Create clear documentation for the implementation and usage of David Stark's statistical code wrapper. Some challenges
that arise with this code are the installation of R dependencies on the system and the references made to online 
sources for the R software being implemented.
2. KLM: A collaborator (Jerry Sellwood) is interested in unbarred galaxies and proposing kinematic misalignment as a 
potential way to prevent bar formation (as far as I understand him anyway). Strikes me we have a sample to check this 
out quickly with. If you match with the “friendly” version of GZ:DESI here that would be interesting, and maybe try to
compare histograms of the strong and weak bar fraction vote for the MA and aligned samples. Seems just worth a quick
check. Might not be anything interesting. Sellwood’s galaxies are usually very idealized.
3. "Punchy" graphics to refine: HI Gas Fraction vs. Stellar mass for each population (co-plotted)
; CDF of HI richness from Kaplan-Meier; Line used to calculate deficiency should be on HI fraction plot
4. HI depletion time: MHI / SFR --> yrs, how long the galaxy can sustain its current SFR; and CDF for depletion time
5. https://arxiv.org/abs/2504.01410: ISM
6. HI richness: overlay fits
   #Huang et al. 2012 line of best fit (f1 below logM=9, f2 above)
   logM=stellar mass array
   fpred = 0.712 * logM + 3.117 - logM
   fpred[logM>9] = 0.276* logM[logM>9] +7.042 - logM[logM>9]
   HIrich = Mfrac - fpred
   Then run CDF code on HIrich including upper limits. 
7. Research note overleaf
8. new data file