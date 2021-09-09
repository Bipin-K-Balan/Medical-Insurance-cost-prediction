# Medical-Insurance-predictor
Goal: Different persons have different body types and different living culture. So the diseases effection on them or the treatment expense for them also vary with respect to these situations. Foe example medical insurance premium of a smoker person may require more amount than a normal person without any bad habbits, since the probability of occurance of chronic disease are more for smokers. The main aim of this application is to help users to get overall idea about the appropriate medical insurance premium suitable for their living culture, gender and so many other factors. 

This is an Machine Learning based Web application deployed in heroku which will forecast the medical insurance cost based on some input features. The web application has designed in such a way that we can do predictions in 2 modes. We can get the insurance premium prediction based on providing input features from the web interface or if we want to get predictions for large dataset, we can also upload the csv file and model will give the predictions as a csv file and we can download deom the webpage using download button.
Main features are Age, gender, body mass index, childrens, smoker or not, locality.


![screenshot1](https://user-images.githubusercontent.com/53367536/110672252-77188b80-81f5-11eb-93db-59615e6e9cd4.JPG)


The data is collected, after that seperated train and test data and created seperate data cleaning, transformation and feature engineering pipelines to avoid data leakage.
Sklearn pipelines has been used for train data and test data preprocessing and transformations seperately inorder to reduce the complexity and for clean code approach. 5 seperate pipelines has been used to train different regression models and also performed grid search CV for hyper parameter tuning. From the metrics results best model has been selected and saved as pikle file. Coding has been modularized for the future enhancement.

Flask is used to create the API calls to the front end web interface which uses css, html and few java script codes.

