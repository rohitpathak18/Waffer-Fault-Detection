# Waffer-Fault-Detection

## Problem Statement: The production Line supply Depends on the Wafer (Thin layer of semiconductor devices). & each wafer is containing many sensors. You have to check whether Wafer is working or Not based on sensor data reading.

### About Dataset:- 
 1. Data is containing the sensor from 1-591 as a features.
 2. Target Column is Having Value [1,-1] 1 means = wafer is Faulty. -1 means = wafer is working. Solution:- • we have Defined Two Route one is Training & second is Prediction         Route. • Both the Route Divided into two Parts :i). Raw Data Validation ii). Training/prediction.
 * In Raw Data Validation, Client Sending the Data in the form of Batch Files of 100 records.
 * then we are applying validation on Raw data & divide the data into two parts : 1) Good Data, 2) Bad Data.
 * After that we are taking the information of Bad Files & sending it to the Client for References Through Email.
 * then we are dumping the data into MongoDB atlas.
 * then creating the One Master CSV file from DataBase & saving that file to s3 bucket & applying the all machine learning stuff on the that one master csv file.
 * we have used the PCA decomposition for the feature reduction & saving model from curse of dimensionality. for that we have used no. of features = 100 which is giving us the 90%    of Explained Variance.
 *  Here we have applied Customized machine learning approach for better result & buiding the different model for different clusters,then we have used two best performing          algorithm which is gives us best result 1). RandomForest 2). Xgboost  
 * we have selected these two algorithms because we have Imbalanced data set & these two algorithms are not Impacted by the Imbalanced Dataset.
 * for Prediction Route we have define the the same pipeline for doing the Validation & data preprocessing, then we will finding the best model for each cluster based on cluster name.
 * & doing the prediction for each clustered data & saving the prediction into  a Prediction File.

# How to run the project? :thinking:
1. Download all the files.
2. Install PyCharm.
3. Open the "main.py" file.
4. In the terminal type -> pip install -r requirements.txt
5. After installing all the necessary libraries.
6. Run the main.py file.
7. Open the localhost in the web browser.
8. You can see the Web API to predict the wafer quality.
9. Place the Folder path of which csv files need to be predicted in the text box. Here it is "Prediction_Raw_Files_Validated".
10. Click the Custom File Predict and you can see the output. You will also get the output csv file in "Prediction_Output_File" folder.
11. In case you want to train the model again.
12. Install Postman.
13. Pass the URL:localhost:5000/train and along with that send the file's folder path which you want to train as json format. Here it is 'folderPath':'Training_Batch_Files'.
14. After getting output "Training Successful", do the prediction as mentioned above.

Thank you.

## Connect with me! 🌐
- [[Linkedin]](bit.ly/3xNkOzO)
- [[Instagram]](bit.ly/3eTGyRT)
- [[Twitter]](bit.ly/3aWT16g)
