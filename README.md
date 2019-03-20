# Predicting central line infections and length of stay in the ICU using the MIMIC-III database

### Please note: This is a work in progress - just beginning

## Data:
MIMIC-III is a publically available critical care database containing de-identified information from over 40,000 patients who stayed at the Beth Israel Deaconess Medical Center between 2001 and 2012. The database includes patient demographic information, admittance and discharge times, diagnostic and billing codes, laboratory test results, procedures, medications, caregiver notes, imaging reports, mortality (in and out of the hosptial) as well as vital sign measurements collected per hour at the bedside. While care has been taken to de-identify this data, additional considerations are needd when working with this data. Thus, to access the database, one must first complete a data research course and sign a Data Use Agreement (more information can be found here: https://mimic.physionet.org/gettingstarted/access/).  

The data is stored in a postgreSQL database in 26 tables. THe schema for the database can be found on the MIMIC website, linked here: 
https://mimic.physionet.org/mimictables/

## Design: 
I have 2 goals in mind for this project: 
  1. Predict length of stay for patients in the ICU
  2. Understand which features contribute most strongly to longer durations of ICU stays.
  
As interpretability of the model is essential for understanding which features contribute to long lengths of stay, I plan to use generalized linear models as well as some techniques for model interpretability such as LIME. 

## Tools: 
*	Jupyter Notebooks, Spyder IDE
*	Pandas, Pickles, Seaborn, Scikit learn 
*	AWS
* PostgreSQL 
*	WinSCP and Putty (tools for connecting to AWS)
* DataGrip (GUI for relational databases)
