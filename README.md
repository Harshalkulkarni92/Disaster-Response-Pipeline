# Disaster-Response-Pipeline

## Project Overview

This project holds repository that contains code for application which can be used by employees during a disaster event 
(e.g. an earthquake or hurricane), to be able to classify the messages into several categories, in order that the message can be directed 
to the appropriate aid agencies.

The app uses a ML model to categorize any new messages received, and the repository also contains the code used to train the model and to 
prepare any new datasets for model training purposes.

## File Descriptions


• ETL Pipeline Data cleaning pipeline contained in data/process_data.py:  

  • Loads the messages and categories datasets  
  • Merges the two datasets  
  • Cleans the data  
  • Stores it in a SQLite database  
  
• ML Pipeline Machine learning pipeline contained in model/train_classifier.py:  

  • Loads data from the SQLite database  
  • Splits the dataset into training and test sets    
  • Builds a text processing and machine learning pipeline   
  • Trains and tunes a model using GridSearchCV    
  • Outputs results on the test set    
  • Exports the final model as a pickle file    

• Flask Web App is the web application the employees can use during emergencies to classify messages into respective categories.  
  The web app also displays visualizations of the data.  
  
  
## Instructions:

• Run the following commands in the project's root directory to set up your database and model.  

  • To run ETL pipeline that cleans data and stores in database python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
  • To run ML pipeline that trains classifier and saves python models/train_classifier.py data/DisasterResponse.db models/model.p  
  
• Run the following command in the app's directory to run your web app. python run.py  

• Go to [http://0.0.0.0:3001/](https://view6914b2f4-3001.udacity-student-workspaces.com/)  

## Acknowledgement

• [Udacity](https://eu.udacity.com/) for providing such a complete Data Science Nanodegree Program  
• [Figure Eight](https://www.figure-eight.com/) for providing messages dataset to train my model  
