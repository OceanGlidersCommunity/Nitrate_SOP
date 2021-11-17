# Missions execution

## UV Spectrometers
For nitrate measuring UV spectrometers glider mission execution is fairly straightforward. As there are no sensor delays or similar to consider, the main point in mission planning and execution is energy consumption and possibly minimization of bio-fouling. Since these instruments use a significant amount of power the need for vertical resolution has to be balanced against the length of the deployment.

In difference to e.g. Oxygen optodes the measurement of only down- or upcasts is a possibility as there is no reason for them to differ (optodes have significant lags). For Deep-SUNAs with their relatively low noise levels one measurement every few seconds appears sufficient to resolve the larger scale nitrate concentration variations.

On Slocum, seaglider and seaexplorer gliders it is also possible to run different sample rates for different depth ranges. At GEOMAR reduced sampling rates have occasionally been used at depths below 500 m where nitrate concentrations were relatively constant.

When programming the Deep SUNA there are several options for how the data is stored internally. Storing of reduced spectra has also shown to be problematic and storage space will not likely be a limiting factor for normal operations.

We strongly recommend daily storage files and internal storage of full spectra. Data transmitted to Slocum gliders via the serial connection must however be ‘reduced spectra’ as the glider processor cannot handle more data.

We recommend as many nearby CTD casts with water samples for high accuracy lab based nitrate measurements as possible. 

The water sample based concentrations can be used to cross-check the concentrations from the UV spectrometers. If no spectrometer-on-CTD calibration casts or lab calibrations are available the water sample data can also be used to determine correction factors and offsets albeit at a higher uncertainty.
