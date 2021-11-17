# Delayed Mode Processing and Quality Control

## Delayed Mode Processing 
### UV Spectrometers
The processing of UV attenuance spectra to obtain nitrate concentrations has been fully described in Sakamoto et al. (2009, 2017) and Johnson et al. (2018). 
In delayed mode  temperature and salinity can be used to remove the effects of Bromide on the observed spectra. 
For an additional correction pressure data can be fed into the calculations. 
Matlab code has been published for Deep SUNA processing (https://github.com/SOCCOM-BGCArgo), but can be adapted to other spectrometers. 
Recently (2020) a modified temperature dependency of the Bromide correction has been developed (https://argo.ucsd.edu/wp-content/uploads/sites/361/2021/04/BGC_meeting_ADMT2020_Minutes.pdf). 
Another code version is available at https://github.com/oceanobservatories/ion-functions/blob/master/ion_functions/data/nit_functions.py.

Reference lamp spectra taken before and after the deployment can now be used to remove the effects of lamp aging on the attenuance spectra. 
Nitrate concentrations should be calculated for both pre- and post-deployment lamp reference spectra. 
A linear blend of the two concentrations gives probably the optimal nitrate concentration estimate. 
Depending on the strength of the bio-fouling the linear blend calculation should probably be based on either lamp use time (no or weak bio-fouling) or deployment time (strong bio-fouling).

A cross-calibration of the resulting nitrate concentrations is strongly recommended. 

Reprocessed nitrate concentrations typically differ from higher quality water sample based measurements by a few % (see also Table 1). 
The differences are linear with the concentrations and can be corrected by applying an offset and a slope factor. 
GEOMAR has found that for Deep SUNAs the remaining differences after the correction are typically between 0.5 and 1 µM, significantly better than the >= 2 µM given for uncorrected concentrations. 
Without such a correction the differences can be significantly larger (see Table 1).
Cross-calibration is also possible between Deep SUNA-glider profiles and nearby CTD water sample profiles. 
Preferably close in time and space (acceptable practice). 
As a last resort SUNA values can be cross-calibrated against open ocean climatological values which are typically close to 0 umol/kg near the surface and relatively stable below 500 m depth (tropical Atlantic). 
Calibrations using data from the nutricline will be rather uncertain and one might have to resort to using only the near surface values to determine an offset (and no slope).

### Lab-on-Chip Instruments
For the lab-on-chip analyser there are a number of post processing steps to be conducted:
1. Check the consistency of blank and standard absorbance values to identify any calibrations that are clear outliers. Data from such calibrations can either be omitted from further analysis, or an alternative calibration could be applied e.g. deployment average calibration values or values from preceding or subsequent dives.

2. Screen sample concentrations for extreme values, the definition of extreme values depends on sampling region and prior knowledge. The sensors have an optional optical correction feature which allows for inherent optical differences between the sample and standard to be accounted for, particularly in estuarine environments. This feature was occasionally shown to make data reduce data quality (e.g. produce extreme negative concentrations) during glider deployments. If large amounts of noise are seen in the data it may be worth investigating whether this feature has introduced any artefacts. 

3. Flag any values that are below the Limit of Detection (LoD). There is no current consensus on how to treat concentrations < LoD. For plotting purposes data can be replaced with LoD/2.

4. Compare the data product to climatological data and if available grab samples collected at beginning and end of deployment.

It is important to note that LoC sample intake takes approximately 15-20 seconds, the precise duration, and hence vertical distance over which the sample is collected, can be calculated for each sample using raw data accessed on glider recovery. This is important when the glider is passing through strong nutrient gradients and for accurately reporting the  sample measurement depth. In dynamic regions, such as shelf seas, it is expected that there will be significant temporal and spatial variation of nutrient concentrations. Not every glider dive will include NO3 measurements, therefore it is helpful to occasionally conduct NO3 analysis on subsequent dives. By minimising natural spatial and temporal variability this allows for an assessment of LoC analyser field precision by comparing samples measured at similar points in the water column. 

## Delayed Mode Quality Control (DMQC)
### UV Spectrometers
Delayed mode quality control for UV spectrometers is comparable to that of real time quality control. See the chapter on RTQC.

The detection limit of SUNA measurements is 0.3 uM which has to be considered when observing oligotrophic regions. Typical issues occur near the surface due to interférence with sunlight and highly turbid regions. 

Based on longitude, latitude, pressure, temperature, salinity and oxygen Argo floats users estimate the DM for nitrate with CANYON B  (https://doi.org/10.3389/fmars.2018.00328. , https://doi.org/10.1002/2017JC012838). This should be done at depth where nitrate values are not so variable. to in situ data as the SUNA is a sensor that drifts in time.
