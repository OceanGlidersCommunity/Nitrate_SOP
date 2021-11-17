# Pre-deployment operations and calibrations

## Storage and Maintenance

### UV Spectrometers
The described UV sensors have no special storage needs apart from that typical for high sensitivity optical instruments. Follow the manufacturer’s instructions in the instrument manuals. 

Regular monitoring of the UV lamp usage is important for Deep SUNA instruments. 
The advertised lifetime of 900 h translates to more than 5 weeks of continuous operation at the fastest sampling rate of 1 Hz or nearly 30 weeks of operation at a reduced sampling rate of 5.5 seconds. 
At GEOMAR one Deep SUNA was in use for 7 two to three week long deployments before a lamp replacement and servicing was initiated.  

### Lab-on-Chip Instruments
Similarly, the LoC analysers have limited storage requirements (room temperature, clean and dry is sufficient).
Reagents have also been shown to be remarkably stable, year long deployments have been conducted in the marine environment and replacement reagents can be purchased. 
For long term storage (several weeks and more), it is recommended to remove the cadmium reduction tube (accessible outside the housing) and store as per manufacturer instructions (so that it cannot dry out and risk becoming blocked).

## Generic function test
### UV Spectrometers
Before deployment a full function test of the UV spectrometer in the lab is recommended. 

A running self-registering instrument should be immersed into water samples with different nitrate concentrations.
E.g. into distilled water (or low nutrient surface water) and, if available, into a sample from a deeper water mass which is known to contain nitrate. 
The instruments have to be able to detect the difference and, if calibrated,  should give good values and, if not calibrated, should at least detect a difference of the correct order of magnitude.

## General setup
Before any measurement (UV & LoC) with a nitrate measuring instrument it is most important and strongly recommended that the instrument’s internal clock is properly set.

In Slocum gliders the clock offset of Deep SUNAs can be recovered by comparing glider timestamps and Deep SUNA timestamps for exactly matching nitrate concentrations which are sent in real-time from the Deep SUNA to the glider.
It is however much better to set the clock properly.

## Pre-deployment lab calibrations
### Data traceability
Cross-checking a measurement against a reference material with a certified value has become the most important test of the accuracy of a device or procedure for many environmental measurements. 
Certified reference materials (CRMs) for nutrient analysis have only recently become available due to the poor stability of solutions of dissolved nutrients. 
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

In the absence of CRM measurements, measurements from CTD samples collected as close as possible in space and time to the glider can be used to provide some reassurance as to the validity of the data obtained from the autonomous platform.
This method can be problematic if there are gradients in nutrient concentration (e.g. Vincent et al., 2018) and since this effectively results in the comparison of two separate measurements of two samples that differ to an unknown degree, the measurement uncertainty information provided is greatly diminished. 

In some cases where no cross-checks have been possible, it has sometimes been necessary to use values from historic databases to compare with the data obtained. Such an approach should be avoided if at all possible, since such datasets are often very limited in temporal and spatial coverage and provide no way to quantitatively verify a new dataset.

## UV Spectrometeres
### Deep SUNA
Deuterium UV lamps as used in Sea-Bird Deep SUNA instruments suffer from relatively rapid aging. 
With increasing age the output strength reduces and possibly shifts. 
It appears that the changes are relatively linear over deployment length time scales and can be estimated by measuring the lamp spectra before and after deployment on a glider. 
The software package delivered with Deep SUNA instruments (UCI, previously SUNACOM, available at https://www.seabird.com) allows for the determination of these lamp reference spectra and internal storage and use for subsequent internal nitrate concentration calculations. 
At the same time these reference measurements should take care of any changes of the spectrometer sensitivity.

We strongly recommend this lamp reference calibration before each deployment. Detailed instructions can be found in the instrument manual (Deep SUNA: https://www.seabird.com , enter ‘deep suna manual’ in the search field).

Instead of a lamp reference calibration before a deployment, a lamp reference calibration directly after the previous deployment can possibly be used.

In theory there is no need to determine absorption spectra from nitrate as they are a  material property. These spectra are given by the manufacturer and stored in the instruments. Nevertheless reference measurements can easily be made when nitrate reference samples are available (e.g. by using nitrate CRM). They can be used to check the manufacturer’s nitrate absorption spectra and can also be used to confirm the linearity of the sensor response. Deep SUNA will directly output nitrate concentrations when measuring reference samples. These concentrations should within the uncertainty given by the manufacturer agree with the known concentration in the reference sample.

We recommend these reference measurements particularly when there are doubts on the instrument performance.

### TriOS OPUS
Xenon UV flash lamps as used in TriOS OPUS instruments should suffer much less from aging. The before-and-after deployment lamp reference measurements should thus not be as important as for instruments with Deuterium lamps. However, in one instrument we (GEOMAR) have found possible changes in lamp intensity or spectrometer sensitivity which we were able to correct for by measuring the lamp reference spectra before and after a deployment (the OPUS was used on a CTD not on a glider).

While Deuterium UV lamps have a very stable output with little noise, the Xenon flash lamps of the TriOS OPUS result in considerable noise from one measurement to the next. To obtain a reliable reference lamp spectrum, a larger number of measured spectra (>10) should be averaged.

If ever a TriOS OPUS is used on a glider, we would strongly recommend lamp reference calibrations before each deployment. 

Again, in theory there is no need to determine spectra from nitrate containing reference samples. They can however easily be collected when nitrate reference samples are available and they then can be used to confirm the linearity of the sensor response. 

### Lab-on-Chip Instruments
For a LoC analyser it is recommended that the analyser makes multiple measurements (>10) of solutions with known nitrate concentrations that span the range expected during deployment. 
For this, the sensor can be powered externally (e.g. using a  benchtop power supply). 
The analytical cycle (blank-standard-sample sequence) can be tailored to for each deployment, therefore a platform simulation, which can be performed using the GUI, should be conducted using solutions of known concentrations as the sample to ensure that the analytical cycle produces expected results. 
