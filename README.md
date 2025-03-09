# HI-MaNGA

This repository houses my work with Professor Karen Masters investigating a correlation between galaxy misalignment and 
HI deficiency. Galaxy misalignment describes a difference in the position angles of a galaxy's stellar and gas discs,
and HI deficiency describes how much less non-ionized ('cold') hydrogen gas is present in a galaxy compared to the 
expected (average) amount at the galaxy's given stellar mass.

A running to-do list of tasks I hope to accomplish can be found in `TODO.md`.

This work requires the following Python libraries, which are imported in the beginning of the Jupyter notebook:

```
import numpy as np
from astropy.io import fits
from astropy.table import Table
from matplotlib.colors import LogNorm
import scipy
from scipy import stats
from survival_analysis import survival, ats_fit, kaplan_meier

# Set up matplotlib
import matplotlib.pyplot as plt
%matplotlib inline
```

The original fits image of the HI-MaNGA data is in the file `HI-MaNGA_base.fits`.
The counter rotating galaxy data is found in the file `sampgal_misalign_final.fits`.
`HI-MaNGA_with-MA.fits` combines the two, and is the file that will actually be used to analyze the data. This file
is found in the `Data` sub-directory, along with `.npy` files of the results of running certain statistical methods on
the data later in the notebook.

A previous rendition of this work is found in the Jupyter Notebook titled `mass-fraction-graphing.ipynb`, but I am
currently in the process of redoing this work in the updated `HI-MaNGA_MisalignmentAndDeficiency.ipynb`

The survival analysis code used (`survival_analysis.py`) is from https://github.com/dvstark/survival, courtesy of David 
Stark at the Space Telescope Science Institute (STScI). This repository (`HI-MaNGA`) also contains an example of this 
code's usage, and the code has been copied and slightly modified in the notebook `survival_analysis_example.ipynb` 
before being implemented into the main Jupyter Notebook (`HI-MaNGA_MIsalignmentAndDeficiency.ipynb`). Many thanks to 
David Stark for providing this code, which wraps survival analysis methods from the R Statistical Software into Python, 
and to my Undergraduate PI Karen Masters for referring me to David's repository as well as for her broader research guidance.