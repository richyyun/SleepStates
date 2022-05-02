# SleepStates

Tracking intracortical signals from the motor cortex of non-human primates via a Utah array for 20-24 hours and classifying brain states between 1) awake and moving, 2) awake and at rest, 3) REM sleep, 4) non-REM sleep. States were classified via dimensionality reduction and clustering. I first implemented a PCA (SVD) oriented approach, but ran into the limitations of linear transformations. I then implemented a stacked sparse autoencoder (inspired by Tsinalis et al. 2016) which was more consistent compared to EOG signals and movements recorded with the Kinect and showed clear REM cycles. 

Once the states are classified, spike and LFP dynamics throughout each state were analyzed.  

<p align="center">
  <img width="651.78" height="447.63" src="https://github.com/richyyun/SleepStates/blob/main/ClassificationFigure.png">
</p>

A. Diagram of classification process. LFP and accelerometer signals are used to perform PCA and k-means clustering to determine different sleep states. B. Example of classification and spectra over time.
