# Combined-Cycle-Power-Plant-Energy-Prediction

**Problem Statement:**

We will design a predictive model to predict full-load power output of Combined Cycle Power Plant Dataset from UCI machine learning repository and evaluate the performance of the model.

Includes Linear Regression, its assumptions and regularization. Also Random Forest Regressor model

https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant

**About Data Set:**

The dataset contains 9568 data points collected from a Combined Cycle Power Plant over 6 years (2006-2011), when the power plant was set to work with full load. Features consist of hourly average ambient variables Temperature (T), Ambient Pressure (AP), Relative Humidity (RH) and Exhaust Vacuum (V) to predict the net hourly electrical energy output (EP) of the plant.

**Attribute Info:**

Features consist of hourly average ambient variables:

1. Temperature (T) in the range 1.81°C and 37.11°C
2. Ambient Pressure (AP) in the range 992.89-1033.30 milibar
3. Relative Humidity (RH) in the range 25.56% to 100.16%
4. Exhaust Vacuum (V) in the range 25.36-81.56 cm Hg

Target is:
Net hourly electrical energy output (PE) 420.26-495.76 MW

**Conclusion:**

* We check for the linearity of our dataset using residual plots, and found our dataset amlost linear
* We use Shapiro-Wilk and Anderson-Darling test, to check whether our dataset is normally distributed or not
* Check for the multicolinearity and try to improve our dataset so that there is no effect of multicolinearity
* We also test for homoscedasticity and it's present in the dataset
* Using Durbin-Watson test, we check for the autocorrelation of our dataset
* There is high negative correlation between AP, V, AT features with Power Output
* We also see the predictor features (AT and V) are highly correlated to each other
* We don't see any change in the accuracy of linear regression model after using  ridge regularization
* Accuracy of linear regression model increased from 92% to 99% after preprocessing.normalize()
* Accuracy of random forest regressor model has increaded from 96% to 99% after preprocessing using normalize
