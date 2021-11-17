# Required Metadata, Real Time Data Processing & Quality Control

## Required Metadata and Real Time Data Processing
### UV Spectrometers
Both Deep SUNA and OPUS instruments are capable of real time processing the measured spectra and output a nitrate concentration. 
For OPUS instruments the possibility exists to order a version without real time processing which then allows for a more rapid sampling rate.

As UV light is absorbed by the bromide ions in seawater this absorption has to be taken into account to give a number for the nitrate concentration. 
The absorption is linearly dependent on the salinity of the seawater and if the salinity is known the attenuance spectra can directly be corrected for this. If the salinity is not known, the concentration of bromide can be estimated from the spectra themselves as the UV absorption of bromide differs from that of nitrate. In Deep SUNAs the salinity is estimated using an optimization. The optimization algorithm has not been published by the manufacturer. Using the optimization algorithm however leads to elevated uncertainties of the nitrate concentrations (2.4 µM instead of 0.3 µM precision). Slocum G2 gliders equipped with a Deep SUNA do not feed their salinity measurements into the Deep SUNA, the optimization algorithm has thus to be used for real time calculations. This means that real time Deep SUNA data is typically relatively noisy. Only in post-processing the nitrate concentrations can be recalculated using the known salinities leading to better precision measurements. In theory CTD information could be fed from the glider into the Deep SUNA thereby enabling the calculation of concentrations with the lower noise levels. 
However it is currently (November 2021) not implemented and not planned to be implemented.

OPUS spectrometers can also derive nitrate concentrations in real time, but to the groups involved in writing this document no instrument with that capability was available.

## Real Time Quality Control (RTQC)
XXX

### Global range check
XXX

### Outlier and spike check
XXX

### Stuck value test
XXX

### Bad P/T/S QC spreading
XXX 

### Effects of biofouling
XXX

