# FakeNews

Github:

1. Download dataset from https://www.kaggle.com/yashasvis/fakenews </br>
	if you need raw data then please download from url given in project documentation.

2. First file is "Data_Cleaning.ipynb". 
	File is responsible for performing data cleaning and it will also create numeric features which we need for Model training. 
	After data cleaning and feature engineering all data's will get imported into training and testing datasets

3. Execute "EDA.ipynb" file
	This file contains code for Exploratory Data Analysis.

4. After EDA run "ML Algorithms.ipynb" file.
	This file is responsible for fitting and testing model on numeric features created in data cleaning phase.
	Various Machine Learning models will be trained and tested in this file on engineered Features.

5. Next step is to execute "tfidf-vectorization.ipynb" file.
	Text data has been vectorized using TFIDF vectorizer and Machine Learning models has been trained on TFIDF vectors and combined TFIDF vector + Numeric Features.

6. Execute "ML_Embedding.ipynb.ipynb".
	Text data has been converted into count vectors using Count vectorizer and then Machine Learning models has been trained and tested on Count vectors and combined Count vectors + Numeric Features.

7. After Machine Learning I have trained Deep Learning model on top of data. Next is to run "DL_algos.ipynb" file. Setup GPU environment for faster training.

8. Last stage is the productionization of models. I have deployed LR model using count vector however any model can be used.
	Execute "streamlit run ap.py" on Anaconda prompt or terminal for running app in local environment. 
	
	I have deployed this project on Heroku cloud. To run app on cloud follow as below.
===> Make sure you have below 3 files in he folder to deploy app on Heroku cloud
--> setup.sh - Modify setup.sh file and replace youremail@domain.com with your heroku email id.
--> requirements.txt - File is already present. However, better is to create your own.  New file can be created using below command.
						## pipreqs ProjectFolder
--> Procfile - This file can be left unchanged if name of app is not modified.


## Steps to run streamlit app
1. Open Anaconda prompt or git bash.
2. Navigate to folder where project is stored
3. Execute below commands:
		git init
		git add .
		git commit -m "Your Message'
3. Next step is to create heroku app
		heroku login
		heroku create -a "AppName"
		git remote -v
		git push heroku master
	Note: After "heroku login" you will be routed to heroku login web page. Enter your credentials and login successfully.
	
## Please refer documentation for furter details.
