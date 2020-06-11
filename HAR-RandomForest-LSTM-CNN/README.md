
# Human Activity Recognition Using Accelerometer Data

This repeository contains the code for Human Activity Recognition (HAR) using data collected from accelerometers in mobile phones. The data was collected by UC Irvine Machine Learning Repository in the following link: https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones

## Files

This folder contains: 
* 
* `Feture_extraction` folder:
  * `Feature_Extraction_Main.ipynb` - Python script that perform the full feature extraction process over localy saved HAPT database and      extract features file for model training and testing in ratio of 0.7/0.3.
  * `Accelerometer_Signal_Proccessing.ipynb` - Python script file, containis acceleromera data cleaning and filtering, for noise              reduction and computing gravity and body acceleration components. 
  * `Feature_Compute.ipynb`  - Python script for computing the statistical metrics on a sliding window of the accelerometer data.
* `RandomForest.ipynb`	- Python script containing sklearn implementaion of the Random Foresr based model for HAR.


### Tools Required

The code in this repository is created using Python 3.6. Furthermore, following libraries are required to run the code provided in this repository:
* `Numpy`
* `Matplotlib`
* `Pandas`
* `sklearn`
* `scipy`
* `os`

### The Dataset

The dataset was experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist.
The acceleromter data is recorded in 50 Htz. As preparation for feature extraction the following process were implemented:
* Median filter for noise reduction.
* A third order low-pass Butterworth filter with a cutoff frequency of 20 Hz - to reduce unrelated frequencies.
* A third low pass filter was implemented to extract the gravity from to body acceleration under the assumption of TA = G+BA.
* The jerk was computed by first order derivetive of the data dA/dt.


### Feature extraction

According to the literature, a rollong window of 2.56 sec with 50% overlap was used to calculatet the following features in time domain and frequeny domain:
* Time domain features:
   * Mean
   * STD
   * Max
   * Min
   * Median
   * Range
   * IQR (75 precentile - 25 precentile)
   * Entropy
   * SMA
* Fequency domain features
   * 6 primary frequencies and their indices (as found by FFT analysis)
   * Total band energy
   * Mean Energy
   * Avarage Frequency


### Model Performances

The Random Forest model acheive accuracy of 0.918
Model selection using gini score threshold of 0.05 didn't approved performnace, acheiving accuracy of 0.904.
