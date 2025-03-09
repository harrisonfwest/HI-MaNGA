# HI-MaNGA

This repository houses my work with Haverford College Professor of Physics and Astronomy Karen Masters investigating a 
correlation between galaxy misalignment and HI concentration in the SDSS-IV/MaNGA survey. Galaxy misalignment describes a difference in the position 
angles of a galaxy's stellar and gas discs, which can range from 0 degrees (well-aligned) to 180 degrees (counter-rotating), 
and HI concentration describes how much non-ionized ('cold') hydrogen gas is present in a galaxy compared to the 
expected (average) amount at the galaxy's given stellar mass. HI mass is particularly easy to detect due to its distinct
21 cm spectral emission line, meaning that we are able to gather relatively abundant data for the HI concentrations of
galaxies up to significant redshifts.

More information about the MaNGA (Mapping Nearby Galaxies at Apache Point Observatory) survey, part of the Sloan Digital
Sky Survey, can be found on the [MaNGA section of the SDSS website](https://www.sdss4.org/surveys/manga/).

As detailed in the Jupyter notebook, we calculate misaligned galaxies, on average, to have approximately 
60% as much HI gas as a well-aligned galaxy at similar stellar mass, a very significant decrease, though the data used
to reach this conclusion is somewhat limited given that compared to more than 6000 galaxies classified as well-aligned,
we only have ~300 misaligned galaxies. Furthermore, more than half of the well-aligned galaxies' HI mass concentrations
are upper limits, or non-detections indicating the upper bound of the galaxy's potential HI concentration, and about
two thirds of the misaligned galaxies' HI mass concentrations are upper limits. This means that it is difficult to
make decisive claims about the behavior of these galaxies, since our already small data set is affected by significant
statistical issues. The implementation of survival analysis and other statistical methods are used to attempt to remedy
this, though there are elements of this that I am yet to complete as of March 9, 2025 (the time of writing). 

This project has been compiled into a [Jupyter notebook](https://github.com/harrisonfwest/HI-MaNGA/blob/main/HI-MaNGA_MisalignmentAndDeficiency.ipynb) 
titled `HI-MaNGA_MisalignmentAndDeficiency.ipynb`. This notebook provides a step-by-step description of the project's 
development, starting from importing the data to selecting rows of table data from which to make plots, and so on.

A running to-do list of tasks I hope to accomplish can be found in `TODO.md`.

The original fits image of the HI-MaNGA data is in `HI-MaNGA_base.fits`, while the counter rotating galaxy 
data from [Zhou et. al (2022)](https://ui.adsabs.harvard.edu/abs/2022MNRAS.515.5081Z/abstract) can be found in
`sampgal_misalign_final.fits`. Using the [TOPCAT software](https://www.star.bris.ac.uk/~mbt/topcat/), I combined these
tables by matching their on `MaNGA ID` columns to create `HI-MaNGA_with-MA.fits`, which is the file that is actually 
used to analyze the data. This file can be found in the `Data` subdirectory, along with `.npy` files of the results of 
running certain statistical methods on the data later in the notebook to avoid redundantly re-running notebook cells 
with excessively long runtimes.

The survival analysis code used (`survival_analysis.py`) is from [the repository of David Stark](https://github.com/dvstark/survival) 
at the Space Telescope Science Institute (STScI). My repository contains an example of this code's usage: the code
has been copied and slightly modified in the notebook `survival_analysis_example.ipynb` before being implemented into 
the main Jupyter Notebook (`HI-MaNGA_MIsalignmentAndDeficiency.ipynb`). Many thanks to David Stark for providing this 
code, which wraps survival analysis methods from the R Statistical Software into Python, and to my Undergraduate PI 
Karen Masters for referring me to David's repository as well as for her broader research guidance.