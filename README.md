# A-data-driven-approach-for-diabetes-prediction-

This project aims to detect the pre-diabetoc or diabetic status of people using the data from the NHANES dataset for years 2011-2014 in which various health-related variables are considered for the final decision to be given for the user input. This was a part of a Biological database managment course which was designed by a team of 4 people. A SQL database was designed to store in the patient data and a Dashboard was built using HTML and CSS for user input with few questions that helps us calculate the score of the major questions to come to a conclusion that the person has diabetes or have a risk of developing diabetes. if the person has already been diagnosed with diabetes we calculated the risk of developing the co-morbidities with the healp of lipid measurements.So, each positive instnace for the answered question was added as apoint to calculte the person having or a higher chance of developing diabetes.<br>

This is the framework of our model.<br>
![image](https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/58696f69-d9cb-43a1-80fb-6f64f4346817)<br>
• Django used MVC pattern to create 5 models for storing data and user input.<br>
• Views connect data tables to HTML templates for updating and deleting data.<br>
• Machine learning and statistical analyses executed via views upon request.<br>
• Results submitted to HTML templates for display.<br>

**Exploratory data analysis and prediction modelling:** The dataset was pre-processed to eliminate any missing values. Using scikit-learn7library in python, a feature selection and machine learning algorithm were built for the prediction. Dimensional reduction was performed on the data using recursive feature elimination (RFE) function in the model selection tool. The elimination was done using a Decision tree estimator, resulting in the selection of the most significant features with respect to the condition. Decision Tree Classifier was used to train the model with BMI, weight, cholesterol and Triglycerides levels, physical activity to predict the stage of diabetes. Data distribution visualizations were conducted to examine the variation of data between pre-diabetic and diabetic conditions, while the Pearson correlation coefficient test was utilized to analyze the correlation between features.<br>

**SQL connector**
MySQL Connector is a popular Python driver used for MySQL databases. It enables developers to execute various database operations and is frequently used in web development and data analysis projects. For this project, MySQL Connector was used to connect the SQL database to Django and import data into models,
which are essentially the tables in the SQL database.<br>
![image](https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/5fce57ed-fa1d-470a-9ee2-b0d1fdb6df2c)<br>
Entity Relationship Diagram Depicting the tables and their relationships.<br>

**Explanation of ERD:** <br>
The database consists of 4 tables namely **PersonalInformation, LabReports, MedicalHistory, Lifestyle**.<br>
**1. PersonalInformation:** This table consists of the information on name, sequence number(seqn), age,
height, weight, gender, race, bmi, email and phone number. Seqn is the primary key for the table and is auto assigned for each new datapoint. It is connected to every other table through the primary key in a one-to-one relationship.<br>
**2. LabReports:** It consists of information on the blood reports of the patients. HbA1C levels, cholesterol, triglycerides, blood pressure, glucose levels and also the condition of the individual are stored in this table. As every patient has only one blood report it has a one-to-one relation with
PersonalInformation on seqn.<br>
**3. MedicalHistory:** family history, PCOD, pregnancy and hypertension are the medical conditions in the table. Every seqn has one record of medical history, hence the table is in one-to-one relation with PersonalInformation.<br>
**4. Lifestyle:** this consists of smoking, alcohol, physical activity, and sleep habit data for each individual. This is also in one-to-one relationship with the PersonalInformation table on seqn.<br>

**DBDL:** <br>
**PersonalInformation (SEQN**, Age, Name, Gender, Race, Height, Weight, BMI, Email, phone_number)<br>
**LabReports (LabReports_ID,** SEQN, Diabetes_Status, HbA1c, Glucose, Cholesterol, Triglycerides,
Blood_Pressure_Systolic, Blood_Pressure_Diastolic)<br>
SEQN: FK —-> PersonalInformation<br>
**MedicalHistory (MedicalHistory_ID,** SEQN, DiabetesPedigree, PCOD, Pregnancy, Hypertension)<br>
SEQN: FK —-> PersonalInformation<br>
**Lifestyle (Lifestyle_ID,** SEQN, AlcoholConsumption, DietIntake, SmokingStatus, ActivityLevel,
SleepDuration)<br>
SEQN: FK —-> PersonalInformation<br>

**RESULTS:** <br>
**Data Distribution:** <br>
The visualizations of data obtained from NHANES show that diabetes and prediabetes are more prevalent in males, and when compared to other races, non-Hispanic whites are more affected by diabetes and prediabetes. In terms of age, the data suggests that the 51-70 age group is more affected by diabetes, while
the 31-50 age group is mostly in the prediabetic stage.<br>
![image](https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/15dbfa97-0984-4af6-b61e-7d9cd09514e3)<br>
The bar plot for distribution in Diabetic stages distribution of gender.<br>
![image](https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/c7689760-c02f-4dff-9f2a-ccd7e3ec6642)<br>
The bar plot for distribution in Diabetic stages distribution of race.<br>

**Machine learning model:**
The Decision Tree classifier used for prediction had an accuracy of 63% in predicting diabetes. Theaccuracy rate of 63% is promising and suggests that the decision tree classifier is effective in predicting diabetes. The precision values also indicate that the classifier is well-suited for predicting diabetes and
related conditions using the given features and data set.<br>

# These are the few of the visualizations that we have created using HTML and CSS.
<img width="337" alt="image" src="https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/998dc5eb-303e-45a6-9f9d-49808fd2ffdc"><br>
Homapage<br>
<img width="315" alt="image" src="https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/cc828aa2-8dd1-45d0-8382-4afcfcf6b9f1"><br>
Questionnaire<br>
<img width="482" alt="image" src="https://github.com/Anube9/A-data-driven-approach-for-diabetes-prediction-/assets/112353734/ac6ca083-5a06-4402-afc4-91720034e1e5"><br>
Statistics dashboard that has ben showed of the data that we have considered for the prediction model.<br>





