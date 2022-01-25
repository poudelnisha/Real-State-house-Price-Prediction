In this project we are going to build a Real Estate price prediction website
Firstly, we will use a home price dataset from Kaggle.com(kaggle datasets download -d amitabhajoy/bengaluru-house-price-data), build a model using linear regression. (We will compare few other models and chose the best model.)
Secondly, we write a python flask server that uses a saved model to serve as a http request.
Lastly, we will make a simple website in HTML, JavaScript, and CSS. This user interactive website would allow user to enter users desired requirement (like area sqft, BHK,Area) and would predict the home price. 

The model building notebook would comprise of all the machine learning concepts like:
•	Data cleaning
•	Outlier detection
•	Feature Engineering 
•	Dimensionality Reduction
•	GridSearchCV for hyperparameter tuning
•	K fold cross validation technique

Steps:
1. Run model/HousePricePrediction.ipynb
2. Run Server/server.py. It uses a saved model to serve a HTTP request.
3. Run client/app.html 


![image](https://user-images.githubusercontent.com/52985004/150883914-dca40f19-aef5-4e15-8c16-a1ea0e9a7bce.png)
Note: Would like to thank codebasics for the insights. 
This project is ongoing and would like to replicate to US context.
