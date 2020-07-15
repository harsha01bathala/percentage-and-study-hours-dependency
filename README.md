# percentage-and-study-hours-dependency

ML-Model-Flask-Deployment

This is a demo project to elaborate how Machine Learn Models are deployed on production using Flask API and is also part of my internship program at The Sparks Foundation

# Prerequisites

You must have Scikit Learn, Pandas (for Machine Leraning Model) and Flask (for API) installed.

# Project Structure

#### This project has four major parts :

model.py - This contains code fot our Machine Learning model to predict percentage Based on training data in 'hours.csv' file.
app1.py - This contains Flask APIs that receives details through GUI or API calls, computes the precited value based on our model and returns it.
request.py - This uses requests module to call APIs already defined in app.py and dispalys the returned value.
templates - This folder contains the HTML template to allow user to enter employee detail and displays the percentage calculated.
Running the project

Ensure that you are in the project home directory. Create the machine learning model by running below command -
python model.py
This would create a serialized version of our model into a file model.pkl

Run app1.py using below command to start Flask API
python app1.py
By default, flask will run on port 5000.

Navigate to URL http://localhost:5000
You should be able to view the homepage as below : alt text

Enter valid numerical values in all 3 input boxes and hit Predict.

If everything goes well, you should be able to see the expected percentage on the HTML page! alt text

You can also send direct POST requests to FLask API using Python's inbuilt request module Run the beow command to send the request with some pre-popuated values -
python request.py


## edge cases taken care:
No.of study hours should always be less than 24 
Expected percentage should always be less than 100
