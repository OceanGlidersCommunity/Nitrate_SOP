# Pre-deployment operations and calibrations
Before any deployment a number of operations and checks have to be executed to ensure the proper functioning of any oceanographic instrument. For nitrate sensing instruments a calibration is also an important part of the pre-deployment procedures.

## Operations after removal from storage
Before any measurement (UV & LoC) with a nitrate measuring instrument it is most important and strongly recommended that the instrument’s internal clock is properly set.
This is particularly important for self-registering instruments with no data exchange with other instruments. If the clock is not properly set, the data can become untracable in space and time and thus basically useless.

In Slocum gliders the clock offset of Deep SUNAs can be recovered by comparing glider timestamps and Deep SUNA timestamps for exactly matching nitrate concentrations which are sent in real-time from the Deep SUNA to the glider.
It is however much better to set the clock properly before the deployment.

### UV Spectrometers
Instruments should be removed from storage and inspected according to the manufacturer's instructions.

### Lab-on-Chip Instruments
All the components of the hydraulic circuit must be inspected (lamp, tubing, reagent and standards bags, cadmium reduction column, syringe filter) and changed if necessary (keep ready supply of spare parts).

## Generic setup

### UV Spectrometers
Before a deployment a full function test of the UV spectrometer in the lab is recommended. The simplest way is to run some test measurements in waters with different nitrate concentrations. These concentrations do not necessarily need to be known as this is just a function test and no calibration.

For that a running self-registering instrument should be immersed into water samples with different nitrate concentrations. This can e.g. be different mixtures of filtered low nutrient surface water with deep water with higher nitrate concentratins.
The instruments have to be able to detect the difference and, if calibrated, should give good values and, if not calibrated, should at least detect a difference of the correct order of magnitude.

### Lab-on-Chip Instruments

## Pre-deployment lab calibrations

### General considerations
Depending on the deployment area, the possible impact of instrumental interferences (warm-up drift) and environmental interferences (e.g. température, salinity, turbidity, dissolved and particulate organic matter) can be simulated in the lab to assess the sensor performances (calibration range, limit of detection, linearity, accuracy and uncertainty). These results from these preparatory measurements or considerations should be compiled in a detailed report. 

### Data and calibration quality control
Cross-checking a measurement against a reference material with a certified value has become the most important test of the accuracy of a device or procedure for many environmental measurements. 
Certified reference materials (CRMs) for nutrient analysis have only recently become available due to the poor stability of solutions of nutrients. 
However materials are now available from the National Research Council of Canada (https://doi.org/10.4224/crm.2014.moos-3) and KANSO in Japan (http://www.kanso.co.jp/eng/production/). 

SCOR working group 147 (https://scor-int.org/group/147/) recommends the use of certified reference materials for every set of field measurements and has collaborated with the Japan Agency for Marine-Earth Science and Technology (JAMSTEC) to make KANSO nutrient CRMs more widely available to purchase by the community (http://www.jamstec.go.jp/scor/background.html).

While the cost of these materials is not insignificant, and their stability is poor once opened, this cost has to be put into perspective against the cost of glider and sensor technology and the huge costs and human effort that goes into any deployment. 
The use of reference materials in nutrient measurement represents an enormous step forwards in terms of reducing measurement uncertainty and improving data quality. 
The authors anticipate (and hope) that the use of such materials will become as standard as it is in the field of carbonate system parameter measurement or trace metal analysis, where it is no longer possible to publish field data that has not been cross-referenced to a certified reference material.

If at all possible, the performance of the sensor should be verified by measuring a CRM as a sample directly just before the deployment and immediately after recovery. 
This is relatively straightforward for a lab-on-chip analyser, but unrealistic for the UV spectrometer devices since it must be immersed in a large volume of solution in order to get a measurement. 
In this case we recommend the measurement of a suitable water sample. This sample might be collected from a CTD rosette or have been brought beforehand to the deployment. 
If necessary it can be spiked with a concentrated nitrate standard to bring it well within the measurement range of the instrument. 
A sample of this water should be taken and immediately analysed or frozen for later analysis together with a suitable CRM.

For the relatively voluminous UV spectrometers a method for using the small volumina CRMs has to be developed.

In the absence of controls with CRM, measurements from CTD samples collected as close as possible in space and time to the glider can be used to provide some reassurance as to the validity of the data obtained from the autonomous platform.
This method can be problematic if there are gradients in nutrient concentration (e.g. {cite}`Vincent2018`) and since this effectively results in the comparison of two separate measurements of two samples that differ to an unknown degree, the measurement uncertainty information provided is greatly diminished. 

In some cases where no cross-checks have been possible, it has sometimes been necessary to use values from historic databases to compare with the data obtained. Such an approach should be avoided if at all possible, since such datasets are often very limited in temporal and spatial coverage and provide no way to quantitatively verify a new dataset.

### UV Spectrometers
#### Deep SUNA
Deuterium UV lamps as used in Sea-Bird Deep SUNA instruments suffer from relatively rapid aging. 
With increasing age the output strength reduces and possibly shifts. 
It appears that the changes are relatively linear over deployment length time scales and can be estimated by measuring the lamp spectra before and after deployment on a glider. 
The software package delivered with Deep SUNA instruments (UCI, previously SUNACOM, available at https://www.seabird.com) allows for the determination of these lamp reference spectra and internal storage and use for subsequent internal nitrate concentration calculations. 
At the same time these reference measurements should take care of any changes of the spectrometer sensitivity.

We strongly recommend this lamp reference calibration before each deployment. Detailed instructions can be found in the instrument manual (Deep SUNA: https://www.seabird.com , enter ‘deep suna manual’ in the search field).

Instead of a lamp reference calibration before a deployment, a lamp reference calibration directly after the previous deployment can possibly be used.

In theory there is no need to determine absorption spectra from nitrate as they are a  material property. These spectra are given by the manufacturer and stored in the instruments. Nevertheless reference measurements can easily be made when nitrate reference samples are available (e.g. by using nitrate CRM). They can be used to check the manufacturer’s nitrate absorption spectra and can also be used to confirm the linearity of the sensor response. Deep SUNA will directly output nitrate concentrations when measuring reference samples. These concentrations should within the uncertainty given by the manufacturer agree with the known concentration in the reference sample.

We recommend these reference measurements particularly when there are doubts on the instrument performance.

#### TriOS OPUS
Xenon UV flash lamps as used in TriOS OPUS instruments should suffer much less from aging. The before-and-after deployment lamp reference measurements should thus not be as important as for instruments with Deuterium lamps. However, in one instrument we (GEOMAR) have found possible changes in lamp intensity or spectrometer sensitivity which we were able to correct for by measuring the lamp reference spectra before and after a deployment (the OPUS was used on a CTD not on a glider).

While Deuterium UV lamps have a very stable output with little noise, the Xenon flash lamps of the TriOS OPUS result in considerable noise from one measurement to the next. To obtain a reliable reference lamp spectrum, a larger number of measured spectra (>10) should be averaged.

If ever a TriOS OPUS is used on a glider, we would strongly recommend lamp reference calibrations before each deployment. 

Again, in theory there is no need to determine spectra from nitrate containing reference samples. They can however easily be collected when nitrate reference samples are available and they then can be used to confirm the linearity of the sensor response. 

#### Lab-on-Chip Instruments
For a LoC analyser it is recommended that the analyser makes multiple measurements (>10) of solutions with known nitrate concentrations that span the range expected during deployment. 
For this, the sensor can be powered externally (e.g. using a  benchtop power supply). 
The analytical cycle (blank-standard-sample sequence) can be tailored to for each deployment, therefore a platform simulation, which can be performed using the GUI, should be conducted using solutions of known concentrations as the sample to ensure that the analytical cycle produces expected results. 

## Pre-deployment field calibration

### General considerations
The technical limitations of the nitrate sensor (power consumption, data memory, measurement rate, anti-fouling options, volume of reagents and standards) have to be carefully evaluated in relation to the specifics of the deployment (duration, study area). Additional measurements (water sampling, temperature, salinity and turbidity) and several factors (measurement rate, calibration range) must be adapted to match the expected uncertainty of the nitrate measurement. Pictures of the sensors should be taken before and after deployment.

### UV Spectrometers
If possible, we recommend any nitrate sensing UV spectrometer to be attached to the CTD and run through a CTD cast with several bottle stops. 

The bottle stops have to be long enough (a few minutes) for the instrument to measure several spectra. During the bottle stops water samples for high accuracy nitrate concentration measurements have to be taken and later measured according to GO-SHIP recommendations {cite}`Becker2020`. Depths with significant gradients in nitrate concentrations should be avoided for these stops.

This type of field calibration requires an external power source for the spectrometer. This can be a dedicated battery pack or a special cable connecting the instrument to one of the CTD’s connectors (GEOMAR has followed this second way for both Deep SUNA and TriOS OPUS instruments).

Note that Deep SUNAs have to be reconfigured for such a calibration cast and that the configuration has to be reverted back to the glider-specific configuration thereafter.

### Lab-on-Chip Instruments
Pre-deployment field calibration is not required for the LoC analyser as the blank and standard solutions are assessed during the lab calibration. However, when deploying a LoC-glider platform it is ideal to manually collect samples, following GO-SHIP protocols {cite}`Becker2020`, in order for a field validation. Experience shows that after a period of dormancy the first dive may not produce reliable data as the chip ‘equilibrates’, this is typical of many flow analysis instruments. Initially conducting simultaneous dives with LoC measurements to generate a robust comparison is advisable. 

#### Cadmium column checks

Performance of the Cu-Cd reduction column requires careful monitoring. For best results, the efficiency of conversion of nitrate to nitrite should be > 95% {cite}`Becker2020`. Columns operating at lower efficiency can give reliable measurements, provided their performance does not vary with time, but this will result in erroneously high measured values for NO<sub>2</sub>+NO<sub>3</sub> if the sample contains significant amounts of nitrite, which can occur near the nitracline in many ocean regions. It is thus essential that the performance and stability of the column should be evaluated in the laboratory prior to any deployment, and it is advisable that its performance be checked in the field immediately prior to and following the glider mission by measuring a pure nitrite standard of known concentration. Such a check can be invaluable in diagnosing faults after recovery of the sensor.

## Data submission (pre-deployment)
To ensure a smooth processing of real-time data by Global Data Assembly Centers (GDACs) it is important that glider operators contact their respective GDAC and prepare them for the data that will be collected. 
This typically includes the collection of various Metadata for all sensors present on the glider as well as other deployment specific information.
