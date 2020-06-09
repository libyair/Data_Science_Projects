
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


### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

