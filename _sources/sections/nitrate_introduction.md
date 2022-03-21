# Introduction

This standard operating procedure (SOP) document for nitrate (NO<sub>3</sub><sup>-</sup>) aims to guide glider users through the steps necessary for the collection of good quality nitrate concentrations using gliders for both real time and post deployment data streams. 
It concentrates on glider specific questions and tasks. 
Additional in depth information on standard operating procedures for *in situ* nutrients measurements can be found in {cite}`Daniel2020`.

There are currently two methods available to conduct *in situ* nitrate measurements using glider platforms: ultraviolet (UV) absorption spectrometers (e.g. {cite}`Thomsen2019`), and miniaturised wet chemical analysers (e.g. Lab-on-Chip (LoC) instruments) (e.g. {cite}`Vincent2018`).

## Nitrate measurement with UV spectrometry
That ultraviolet light is absorbed by nitrate ions has been known since the 1950s {cite}`Bastian1957`. 
More recently the development of miniaturized spectrometers led to instruments which could be deployed *in situ* to determine nitrate concentrations in fresh- and seawater.

Around 1998 a prototype instrument was developed at Southampton Oceanography Centre for use in seawater using only a limited number of spectral channels {cite}`Finch1998`. 
Another instrument was developed at Monterey Bay Aquarium Research Institute (MBARI, {cite}`Johnson2002`) based on a miniaturized spectrometer measuring UV intensity at a larger number of wavelengths. This has since become commercially available as ISUS and  SUNA.
Other comparable instruments have been developed by various companies and institutions with the emphasis on freshwater monitoring (e.g. NitraLED by YSI, USA or spectro::lyser by s::can Messtechnik, Austria).

All these instruments determine the attenuation (absorption, reflection and scattering) of ultraviolet (UV) light in water, which for the range of wavelengths from about 200 to 250 nm is strongly dominated by bromide, nitrate and, to a much lesser extent, bisulfide (HS<sup>-</sup>), humic acid and nitrite (NO<sub>2</sub><sup>-</sup>) as well as by the scattering by particles (turbidity) {cite}`Johnson2002`. 
Temperature and pressure additionally influence the attenuation {cite}`Sakamoto2009`, {cite}`Sakamoto2017`.

The attenuation processes have different spectral characteristics in the UV wavelength range allowing their effects to be distinguished to some degree. 
This enables UV spectrometers to determine the concentrations of multiple chemical species at the same time. 
The spectral attenuation characteristics for the different chemical species are well known or can easily be determined in the lab with reference samples, while the temperature, salinity and pressure dependencies have been derived from lab and *in situ* data.

The known dependencies of the species that are not of interest are used to correct the observed spectra. 
E.g. the presence of bromide (from independent salinity information) is corrected for in regular processing. 
Similarly the effects of temperature and pressure (again from independent information) are removed from the spectra. 
The possible presence of nitrite and bisulfide is usually ignored as in most cases their concentrations are small, though in cases with high enough concentrations they can possibly be distinguished from nitrate {cite}`Meyer2018`. 
After correcting the observed spectra the concentration of nitrate can be estimated. 
In cases when the salinity and temperature of the sample is unknown (e.g. in the real time data on a glider) these two parameters can be estimated from the observed spectra using an iterative approach albeit at a reduced accuracy of the nitrate value. However additional controls are recommended in areas where the proportion of nitrite to nitrate, the dissolved organic matter concentration, the bisulfide concentration, the turbidity become significant (e.g. anoxic waters, hydrothermal vents, coastal waters).

## Nitrate measurement by wet colorimetric analysis
The ‘Griess assay’, first described in 1858, is a spectrophotometric technique used to measure nitrite in solution via formation of a pink-red azo dye {cite}`Griess1858`.
Quantification is achieved by relating the absorption of light by the azo dye to the concentration nitrite using the ‘Beer-Lambert’ law:

A = log<sub>10</sub>(I<sub>0</sub>/I) = elc

where A is absorbance, I<sub>0</sub> is incident intensity, I is the transmitted intensity, e is the molar absorption coefficient, l is path length and c is concentration. 
In the case of the ‘Griess assay’, the addition of a chemical reduction step (e.g. a copperized cadmium column) allows for the measurement of the NO<sub>2</sub><sup>-</sup>+NO<sub>3</sub><sup>-</sup> concentration. 
This approach is widely used in oceanographic studies and incorporation into gas segmented flow manifolds allows for high sample throughput and the accuracy and precision required for all but the most oligotrophic regions of the ocean {cite}`Becker2020`. 

Automated in situ analysers utilizing the Griess assay were first reported in the 1980s {cite}`Johnson1989`. 
Over the past decade, Lab-on-Chip (LoC) microfluidic technology has allowed miniaturization of this approach into analysers small enough to be installed on autonomous platforms such as Seagliders {cite}`Beaton2012`, {cite}`Vincent2018`. 
Relative to UV sensors, LoC analysers offer increased sensitivity and analytical figures of merit comparable to standard benchtop techniques {cite}`Birchill2019`, but require the use of chemical reagents and waste which must be stored on board the glider, and have a reduced sampling frequency due to the time required for chemical analysis and flushing.

