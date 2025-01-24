# HI-MaNGA
Investigating correlation of misalignment between galaxies' non-ionized ('cold') hydrogen gas and stellar disks, and their cold hydrogen gas deficiencies

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