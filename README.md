# Solar-Radiation-Prediction

Project developed alongside Marco Antonioli and Elia Torre for the Hackathon of the Bocconi Students for Data Science.

The original dataset was released as part of a task for NASA Hackathon and can be retrieved from [kaggle.com](https://www.kaggle.com/dronio/SolarEnergy).
The dataset is related to the level of solar radiation on earth registered from 11/9/2016 to 31/12/2016. 
It contains measurements of 5 athmospheric variables, plus useful information about the time of measurement.

The goal was to predict the radiation level at a specificied instant, given all the sensor data available.

Let’s try to dive into this dataset and let me denote the units of the following columns.

  1. UNIX time: seconds since Jan 1, 1970
  2. The date
  3. The local time of day
  4. Solar Radiation: watts per meter squared (Target variable, to be predicted)
  5. Temperature: degrees Fahrenheit
  6. Humidity: percent
  7. Barometric pressure: Hg
  8. Wind direction: degrees
  9. Wind speed: miles per hour
  10. Sunrise: sunrise time
  11. Sunset: sunset time

For the purpose of our challenge, the dataset was divided into:
* "train_set.csv": (31051 entries) It contained the target feature and was used for training and model selection.
* "test_set.csv": (1635 entries) It did not contain the target feature and was used to evaluate the final performance of the algorithm.
 
 We decided to tackle the problem using a voting regressor, averaging the predictions of two decision tree-based models. 
 
 For our work, which predicted the solar radiation with a mean squared error in the test set of 5569, we have been crowned winners of the competition. The analysis, with the necessary comments and explanations can be found in the "Solar_Radiation_Prediction.ipynb" file.
