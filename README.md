# Medical-Insurance-predictor
This is an end to end regression based deployable Web application which will forecast the medical insurance cost based on some input features. The web application has designed in such a way that if we want to predict large data, we can also upload the csv file and model will give the predictions.
Main features are age, gender, body mass index, childrens, smoker or not, locality.


![screenshot1](https://user-images.githubusercontent.com/53367536/110672252-77188b80-81f5-11eb-93db-59615e6e9cd4.JPG)


The data is collected, and analysed, after that seperated train and test data set initially to prevent any kind of data leakage that may occur during data transformations and imputation of missing values.
Sklearn pipelines has been used for train data and test data preprocessing and transformations seperately inorder to reduce the complexity and for clean code approach. 5 seperate pipelines has been used to train different regression models and also performed grid search CV for hyper parameter tuning. From the metrics results best model has been selected and saved as pikle file. Coding has been modularized for the future enhancement.

Flask is used to create the API calls to the front end web interface which uses css, html and few java script codes.

