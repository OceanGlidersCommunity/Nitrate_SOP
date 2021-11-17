# Sensors and integrations 

## Nitrate sensors

### UV Spectrometers
To our knowledge there are currently at least two different instruments for UV spectroscopy Nitrate measurements in seawater, one manufactured by Sea-Bird Scientific (USA) called Deep SUNA and one by TriOS (Germany) called OPUS. 
A similar instrument has been developed in China (Zhu et al., 2021) but is not yet commercially available.
Deep SUNAs have been specially developed for use on gliders and Argo floats and have been in use now for several years with good experiences. 
OPUS instruments have been tested on floats within the Euro-Argo project (https://www.euro-argo.eu/) but not yet on gliders. 
Both instruments have a 10 mm sample path length in common as this appears to be optimal for the used light sources and spectral sensors and the Nitrate concentrations expected in seawater.
Apart from these instruments there exists a larger number of submersible Nitrate sensors that are optimized for use in freshwater lakes and rivers or for monitoring wastewater (e.g. by YSI, see https://www.ysi.com/parameters/nitrate; by Xylem, see https://www.xylemanalytics.com/en/products/listing-wtw-process-all). 
Whether these could be modified for use in seawater and on gliders is not known.

#### Sea-Bird Scientific Deep SUNA
These instruments are based on the original development by Johnson and Coletti (2002) from MBARI. 
The original was intended for use in underwater moorings and thus had a more voluminous housing to accommodate batteries. 
The MBARI-ISUS was commercialized by Satlantic under the same name (Satlantic-ISUS). 
Satlantic was in 2011 acquired by Sea-Bird Scientific which continues to produce the instruments. 
Satlantic modified the design of the ISUS which used a mirror together with a light source and a spectrometer next to each other to that of the SUNA which has a light source and a spectrometer on opposing sides of the sample volume. 
This modified instrument relied on external power and thus was able to have a much more lightweight and streamlined design. 
The SUNA was further developed into the Deep SUNA which was optimized for the use on autonomous vehicles like gliders or floats with a pressure rating of 2000 dbar and a large internal memory (see also Johnson et al., 2018).

All these instruments share the same basic configuration with a Deuterium UV lamp and a 256 channel UV spectrometer covering the wavelengths from 190 to 370 nm. 
Their internal processor is capable of not only storing the measured spectra but also of converting the data in real time into estimates of the Nitrate concentration.

Deep SUNA have so far been attached to Teledyne Webb Research Slocum and ALSEAMAR SeaExplorer gliders.

The Deep SUNA is capable of one measurement per second. 
Older Slocum gliders (G1 and G2) are however not able to handle more than one measurement every 4 seconds (possibly 2 seconds). 
Typical use on a glider is thus with a reduced sampling rate of one measurement every 5.5 seconds (GEOMAR). 
This also significantly reduces the high power consumption while still delivering one measurement per meter depth for fast diving gliders.

The latest version of G3 Slocum gliders should be capable of sampling and recording Deep SUNA data at 1 Hz, but this has to our knowledge not been tested.

Deep SUNA raw data and internally computed Nitrate concentrations are transferred to Slocum gliders via a serial connection. Raw data is in the ‘reduced spectra’ format containing only a limited wavelength range. The full raw data is recorded in the Deep SUNA itself.

Deep SUNA sensors are available with three different anti-fouling options:
- none
- a copper guard around the sampling volume
- a mechanical wiper

The mounting of Deep SUNA sensors on top of gliders and along the main axis of the glider is probably not optimal as the sampling volume of the Deep SUNA is perpendicular to the glider’s movement. 
At GEOMAR no anti-fouling option has been used so that the water exchange to and from the sample volume is not further decreased.

The nominal energy consumption for a Deep-SUNA given by the manufacturer is 7.5 W. 
We have to assume that this is the maximum power consumption for the fastest possible sampling rate. 
This has to be taken into account for mission planning. 
With a reduced sampling rate of 1 measurement every 5.5 seconds the power consumption is about 1.4 W. 
This is still significantly higher than the power consumption of the CTD or Aanderaa optodes but comparable to that of Microrider microstructure sensors. 
For comparison, a Slocum glider with only a CTD diving at full speed uses on average a total of around 5 W.

Deep SUNAs are commercially available and have mounting solutions and data and power transfer cables have been developed for at least Slocum and SeaExplorer gliders.

#### TriOS OPUS
TriOS (Germany) developed an instrument comparable to the Deep SUNA but decided on a couple of design choices differently. 
In principle the OPUS measures the same information based also on a 256 channel spectrometer. 
However, the OPUS’ lamp is a Xenon flash lamp that has a much longer life cycle (typically >10<sup>9</sup> flashes) than Deuterium lamps (900 h). 
The spectral characteristics of Xenon flash lamps are however less ideal. 
They exhibit line-like spectral peaks in the range in which Nitrate absorbs which might make the analysis of the spectra prone to higher uncertainties possibly because of small shifts in the spectra. 
For single non-averaged spectra the noise level of the OPUS is typically a factor 3 to 8 higher than that of a Deep SUNA. TriOS OPUS are available with a titanium housing with a 6000 dbar pressure rating. 
This should make them suitable also for deep gliders. The OPUS is capable of making one measurement every 3 seconds (factory configuration is slower possibly because of internal averaging). 
For a vertical platform speed of 0.1 m/s this results in a vertical resolution of 0.3 m.







## Sensor integration with gliders

### Mounting location

#### Spray
- XXX

#### Seaglider
- XXX

#### Slocum
- XXX

#### SeaExplorer
- XXX
