### Table of Contents

1. [About](#about)
3. [Description](#description)
2. [Installation](#installation)

## About - Disaster Response Pipeline Project <a name="about"></a>

On this project, I created a machine learning pipeline that classify messages. With the web app, it is possible to input a message and classify this same message in some categories. That is a project that has a real application and could be very helpful to the society, that can be helpful for the emergency worker when insert some message to get a classification to a problem for example. 

### File Descriptions: <a name="description"></a>

The project contains the following files:

app
| - template
| |- master.html # main page of web app
| |- go.html # classification result page of web app
|- app.py # Flask file that runs app
data
|- disaster_categories.csv # data to process
|- disaster_messages.csv # data to process
|- process_data.py
models
|- train_classifier.py
|- classifier.pkl # saved model
README.md
ETL Pipeline Preparation.ipynb # notebook with the ETL pipeline;
ML Pipeline Preparation.ipynb # notebook with the Machine Learning pipeline;


### Installation: <a name="installation"></a>
1. Run the following commands in the project's root directory to set up the database and model.
    - To run ETL pipeline that cleans data and stores in database:
    `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier:
    `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python app.py`

3. Access the following URL http://127.0.0.1:5000/

