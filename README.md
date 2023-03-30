# Software-complexity-predictor

Software complexity assessment (SCA) module predicts software complexity (SC) of the user requirements specification (URS) documents of model car. URS document is a MS word document with goal of the project, functional requirements and non functional requirements. URS document is prepared at the beginning of the project. SCA considers functional requirements of the model car and predicts the software complexity.

Software Complexity assessment module software code is done in 3 steps.
  1. To prepare dataset to train model for prediction
  2. Training the model using dataset from previous step.
  3. predicting the complexity of new URS document from the trained model

## Step 1: Prepare Dataset for creating a learning model

Dataset preparation is critical step in the project as the accuracy of prediction depends on dataset. To prepare dataset, features needs to be selected. Functional requirements(FR) section in URS document defines the software requirements which needs to be implemented. Software complexity of the module depends on the 'functional requirements' section. URS document may consists of FR of single modules like 'collision detection' or multiple modules like ' battery display', 'head lights', 'horn' etc of model car. Each module of FR of URS document forms one feature of the dataset.

features of dataset are "Document_name" : "Battery","Collision","HeadLights","Indicators","RemoteControl","Sync","brakelights","rearlights","similIDE", "Horn","Wiper

Entities of dataset are dataset are created using code in file 'dataset.ipynb'. Database is initially created using excel sheet. Database has FR and SC drivers and software complexity value. Each functional requirement of URS document is compared to database using NLP and steps are shown in comments of 'dataset.ipynb'


## Step 2: Train the learning model

After creating dataset in step 1, model is trained using 'clustering', 'SVM' and 'KNN'. results shows that SVM has good accuracy and it is used to train the model. Eash of the model training is as per file named 'clustering', 'SVM and KNN'

## Step 3: Predicting Software complexity for new requirement document

Monitor, Analyse, plan and execute (MAPE-K) loop is implemented for automatic detection of URS file, analysing for FR, predicting the SC and executing. code for this can be found in 'github version
