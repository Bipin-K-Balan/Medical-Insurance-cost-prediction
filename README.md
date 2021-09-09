# Medical-Insurance-predictor
Goal: Different persons have different body types and different living culture. So the diseases effection on them or the treatment expense for them also vary with respect to these situations. For example medical insurance premium of a smoker person may require more amount than a normal person without any bad habbits, since the probability of occurance of chronic disease are more for smokers. The main aim of this application is to help users to get overall idea about the appropriate medical insurance premium suitable for their living culture, gender and some other factors. 

This is an Machine Learning based Web application deployed in heroku which will forecast the medical insurance cost based on some input features. The web application has designed in such a way that we can do predictions in 2 modes. We can get the insurance premium prediction based on providing input features from the web interface or if we want to get predictions for large dataset, we can also upload the csv file and model will give the predictions as a csv file and we can download deom the webpage using download button.
Main features are Age, gender, body mass index, childrens, smoker or not, locality.


![screenshot1](https://user-images.githubusercontent.com/53367536/110672252-77188b80-81f5-11eb-93db-59615e6e9cd4.JPG)

## Data collection and training
The data is collected, after that seperated train and test data and created seperate data cleaning, transformation and feature engineering pipelines to avoid data leakage.
Sklearn pipelines has been used for train data and test data preprocessing and transformations seperately inorder to reduce the complexity and for clean code approach. The jupyter notebook file attached above has contains all the Exploratory data analysis, creating sklearn pipelines and model selection in detail. 5 seperate pipelines has been used to train different regression models (Vanilla Linear regression, Lasso and Ridge versions of Linear Regressions, Decision tree, Random Forest) and also performed grid search CV for hyper parameter tuning. From the metrics results best model (Random forest is giving good accuracy than other models where decision tree is more overfitted to the dataset) has been selected and saved as pikle file. Coding has been modularized for the future enhancement.

<img width="622" alt="randforest" src="https://user-images.githubusercontent.com/53367536/132633983-97153cf6-75c4-4413-beae-ae863f4dfe04.PNG">

## Web Integration and Deployment
Flask micro web framework is used to create the API calls to the from the python backend code that wrapeed around saved machine learning model to the front end web interface which uses css, html and few java script codes. The code in github is pushed to heroku for deployment. Since this is for testing purpose we did not worked on the latency and replicas of same applications. If thats the case we can dokerize it and deploy it on Kubernetes orchestration framework with auto scaling based on the CPU resource utilization.

