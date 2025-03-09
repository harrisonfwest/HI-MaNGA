# HI-MaNGA

This repository houses my work with Haverford College Professor of Physics and Astronomy Karen Masters investigating a 
correlation between galaxy misalignment and HI concentration in the SDSS-IV/MaNGA survey. Galaxy misalignment describes a difference in the position 
angles of a galaxy's stellar and gas discs, which can range from 0 degrees (well-aligned) to 180 degrees (counter-rotating), 
and HI concentration describes how much non-ionized ('cold') hydrogen gas is present in a galaxy compared to the 
expected (average) amount at the galaxy's given stellar mass. HI mass is particularly easy to detect due to its distinct
21 cm spectral emission line, meaning that we are able to gather relatively abundant data for the HI concentrations of
galaxies up to significant redshifts.

This project has been compiled into a [Jupyter notebook](https://github.com/harrisonfwest/HI-MaNGA/blob/main/HI-MaNGA_MisalignmentAndDeficiency.ipynb) 
in this repository titled `HI-MaNGA_MisalignmentAndDeficiency.ipynb`. This notebook provides a step-by-step description
of the project's development, starting from importing the data to selecting rows of table data from which to make plots,
and so on. As detailed in the Jupyter notebook, we calculate misaligned galaxies 

More information about he MaNGA (Mapping Nearby Galaxies at Apache Point Observatory) survey, part of the Sloan Digital
Sky Survey, can be found on the [MaNGA section of the SDSS website](https://www.sdss4.org/surveys/manga/).

A running to-do list of tasks I hope to accomplish can be found in `TODO.md`.

The original fits image of the HI-MaNGA data is in `HI-MaNGA_base.fits`, while the counter rotating galaxy 
data from [Zhou et. al (2022)](https://ui.adsabs.harvard.edu/abs/2022MNRAS.515.5081Z/abstract) can be found in
`sampgal_misalign_final.fits`. Using the [TOPCAT software](https://www.star.bris.ac.uk/~mbt/topcat/), I matched these tables to each other to
create `HI-MaNGA_with-MA.fits`, which combines the two, and is the file that will actually be used to analyze the data.
This file can be found in the `Data` sub-directory, along with `.npy` files of the results of running certain statistical
methods on the data later in the notebook to avoid redudantly running notebook cells with excessively long runtimes.

The survival analysis code used (`survival_analysis.py`) is from https://github.com/dvstark/survival, courtesy of David 
Stark at the Space Telescope Science Institute (STScI). This repository (`HI-MaNGA`) also contains an example of this 
code's usage, and the code has been copied and slightly modified in the notebook `survival_analysis_example.ipynb` 
before being implemented into the main Jupyter Notebook (`HI-MaNGA_MIsalignmentAndDeficiency.ipynb`). Many thanks to 
David Stark for providing this code, which wraps survival analysis methods from the R Statistical Software into Python, 
and to my Undergraduate PI Karen Masters for referring me to David's repository as well as for her broader research guidance.