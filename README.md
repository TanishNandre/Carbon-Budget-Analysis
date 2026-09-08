# Carbon-Budget-Analysis
CLASS/GILDAS reduction scripts for correcting atmospheric ozone contamination in APEX [C I] 492 GHz observations using manually scaled TSKYEBB reference spectra.
# APEX [C I] 492 GHz Ozone Correction

GILDAS/CLASS reduction scripts for correcting atmospheric ozone contamination in APEX [C I] 492 GHz observations using manually scaled TSKYEBB reference spectra.

## Method

Each science scan `n` is matched with the preceding TSKYEBB scan `n-1`.

The correction is

corrected = science - scale × TSKYEBB

with

scale = science_amp / tskyebb_amp

The amplitudes of the ozone feature in the science and TSKYEBB spectra are selected manually during the CLASS pauses.

If no ozone feature is present, the science spectrum is written unchanged.

If the corresponding TSKYEBB scan `n-1` does not exist, the science spectrum is also retained unchanged.

Negative scale factors are allowed.

The corrected spectra are then passed to the subsequent CLASS reduction/quicklook step.

## Software

- GILDAS / CLASS
- APEX [C I] 492 GHz observations

## Data Reduction

After subtraction is played out in PART 1 , data reduction like baseline subtraction etc takes place in PART 2
