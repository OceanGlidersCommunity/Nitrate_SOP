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
### UV Spectrometers
Four real time quality control checks should be implemented to detect suspicious measurements:
- valid range checks
- spike/outlier detection 
- comparison with climatological information, when available
- sensor drift detection

Real time quality control relies on knowledge of the typical nitrate concentration in the deployment region and on the, in most cases, slow spatial variation of the nitrate concentrations (eddies and fronts are often special cases with larger horizontal gradients). New profiles are typically compared with the previous ones to detect profiles or single values that stand out. Such data can be flagged as suspicious or even bad.

For the different instruments their respective noise level, concentration range and limit of detection has to be taken into account when creating an outlier check. Very rarely objects appear to get into the sampling volume and are usually there for only a few samples after which the measurements return to the previously measured concentrations. The result of this are spikes to higher concentrations (higher apparent absorption).

A slow measurement drift is to be expected for Sea-Bird’s Deep SUNA because of lamp aging and/or bio-fouling. This can not be corrected *in situ* as the reduction in lamp strength is not measured (see also below for the post-recovery calibration). A drift might also occur because of bio-fouling. Both lamp aging and bio-fouling drifts should lead to values increasing with deployment time. Small drifts are often difficult to detect as they might not stand out against other measurement variability. Prior knowledge, such as e.g. an expected nitrate depletion in the surface mixed layer, can potentially be used to detect a small drift. After recovery, renewed calibration and reference measurements may also be used to differentiate between lamp drift and bio-fouling.

### Lab-On-Chip instruments

## Data submission (real time)
It is recommended that real time data is submitted to GDACs for immediate redistribution of the data. 
At the moment of writing (May 2021) it is unclear whether any GDACs process real time nitrate measurements, nevertheless we recommend implementing the submission process.

### UV Spectrometers
Deep SUNAs on Slocum gliders currently (May 2021) transfer to the gliders only nitrate concentrations based on internally optimized temperature and salinity values.
An unknown internal optimization scheme determines temperature and salinity values as well as a nitrate concentration for which the expected spectrum agrees best with the observed one. These optimized temperatures and salinities are often significantly off (by several degrees or PSU) and consequently result in wrong nitrate concentrations.
It should be possible to feed CTD data from the glider into Deep SUNAs to allow for more accurate calculations. 
This should be particularly true for modern Slocum G3 gliders which use faster processors. 
Alternatively raw spectra could be transmitted to data centres albeit at the cost of 30-40 times larger data sets with the consequence of higher costs and longer glider time spent at the sea surface. 
In the future this might also be easier with faster and cheaper satellite transmission systems.
Because of the high costs in time at surface and in money of satellite data transmission typically only a reduced data set is transmitted. 
GEOMAR e.g. transmits only one measurement every 30 seconds or about 3-4 m. Raw spectra are not transmitted.


