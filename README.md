# FakeNews

Github:

1. Download dataset from https://www.kaggle.com/yashasvis/fakenews

2. Execute "Phase-2_EDA_2.ipynb" 

==> File is responsible for performing data cleaning and it will also create numeric features which we need for Modeling. At the end all files will be imported into training and testing datasets.

3. Execute "Phase-2_EDA_2.ipynb" file

==> This file contains code for Exploratory Data Analysis.

4. After EDA run Phase-3-ML_Numeric_Features.ipynb file.

==> In this file we will be working with numeric features created while cleaning the data.
Various Machine Learning models will be trained and tested in this file.

5. Next step is to execute "Phase-3-TFIDF_Vectorization.ipynb" file.

==> Text data has been vectorized using TFIDF vectorizer and Machine Learning models has been trained on TFIDF vectors and combined TFIDF vector + Numeric Features.

6. Execute "Phase-3-ML_CountVector.ipynb".

==>Text data has been converted into count vectors using Count vectorizer and then Machine Learning models has been trained on Count vectors and combined Count vectors + Numeric Features.

7. After Machine Learning I have trained Deep Learning model on top of data in file "Phase-4-DL_algos.ipynb". Setup GPU environment for faster training.

8. Last stage is the productionization of models. Execute "streamlit run ap.py" for running app in local environment. To run app on cloud follow as below.
===> Make sure you have below 3 files in he folder to deploy app on Heroku cloud
--> setup.sh - Modify setup.sh file and replace youremail@domain.com with your heroku email id.
--> requirements.txt - File is already present. However, better is to create your own.  New file can be created using below command.
						pipreqs ProjectFolder
--> Procfile - This file can be left unchanged if name of app is not modified.


Steps to run streamlit app
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
	Note: After you will be routed to heroku login web page. Enter your credentials and login successfully
