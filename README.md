# HI-MaNGA
Investigating correlation of misalignment between galaxies' non-ionized ('cold') hydrogen gas discs and their stellar disks, and their cold hydrogen gas deficiencies

A running to-do list of tasks I hope to accomplish is in `TODO.md`

Most of this work requires the following Python libraries:

```
import numpy as np
from astropy.io import fits
from astropy.table import Table
from matplotlib.colors import LogNorm
import scipy
from scipy import stats

# Set up matplotlib
import matplotlib.pyplot as plt
%matplotlib inline
```

The original fits image of the HI-MaNGA data is in the file `HI-MaNGA_base.fits`.
The counter rotating galaxy data is found in the file `sampgal_misalign_final.fits`.
`HI-MaNGA_with-MA.fits` combines the two, and is the file that will actually be used to analyze the data.

A previous rendition of this work is found in the Jupyter Notebook titled `mass-fraction-graphing.ipynb`, but I am
currently in the process of redoing this work in `HI-MaNGA_MisalignmendAndDeficiency.ipynb`

The survival analysis code used (`survival_analysis.py`) is from David Stark at the STScI, found in
his repository https://github.com/dvstark/survival. This repository also contains an example of the code's usage,
which has been copied and slightly modified here as `survival_analysis_example.ipynb`. Many thanks to David Stark for
providing this code, which imports survival analysis based in R Statistical Software, and for Karen Masters for
referring me to his repository.
