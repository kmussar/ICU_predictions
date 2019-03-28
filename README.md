# Predicting central line infections and length of stay in the ICU using the MIMIC-III database

### Please note: This is a work in progress

## Motivation: 
Approximately half of all patients in critical care settings will need a central line for their care1. Central lines are catheters placed into a large vein near the center of the body and are used for delivering medications that can be damaging to peripheral veins, for long-term administration of antibiotics, pain medications, nutrition, and/or chemotherapy, and for patients that require frequent blood draws or frequent IV access. However, central lines can cause serious adverse effects including pneumothorax, an abnormal collection of air in the space between the lung and chest wall, thrombosis, blood clots, and bloodstream infections. Bloodstream infections are easily the most expensive healthcare-associated infection costing between $17,000 and $95,000 per case2. It is estimated that per year 250,000 cases of central line-associated bloodstream infections occur, with a mortality rate of 10%3.  Fortunately, however, these infections are preventable with proper aseptic techniques, surveillance, and maintenance. A recent study recently showed that the nurse-to-patient ratio was the strongest predictor in compliance to proper infection prevention guidelines. However, hospitals often do not have enough nurses so that every patient has a dedicated nurse. Thus, I aimed to predict which patients were at high risk of developing central line-associated bloodstream infections and what factors contributed to this risk. Knowing this, hospital staff could prioritize dedicated nurses for high-risk patients so that infections could be avoided. 


## Data:
MIMIC-III is a publicly available critical care database containing de-identified information from over 40,000 patients who stayed at the Beth Israel Deaconess Medical Center between 2001 and 2012. The database includes patient demographic information, admittance and discharge times, diagnostic and billing codes, laboratory test results, procedures, medications, caregiver notes, imaging reports, mortality (in and out of the hospital) as well as vital sign measurements collected per hour at the bedside. While care has been taken to de-identify this data, additional considerations are needed when working with this data. Thus, to access the database, I first completed the required data research course and signed the Data Use Agreement (more information about how to access this dataset can be found here: https://mimic.physionet.org/gettingstarted/access/). Due to the nature of this data, I will not be able to share any raw data on github. 
The data is stored as postgreSQL database in 26 tables. The schema for the database can be found on the MIMIC website, linked here: https://mimic.physionet.org/mimictables/. I worked with this data through a local version of the PostgreSQL database that I set up on AWS. 

## Design: 
I have 3 goals in mind for this project: 
  1. Predict if patients are likely to get a central line-associated bloodstream infection (CLABSI) during their stay in the ICU. 
  2. Predict length of stay for patients in the ICU
  3. Understand which features contribute most strongly to both CLABSI and longer durations of ICU stays.
  
As interpretability of the model is essential for understanding which features are contributing the most, I plan to use generalized linear models as well as some techniques for model interpretability such as LIME. 

## Tools: 
*	Jupyter Notebooks, Spyder (IDE)
*	Pandas, Pickles, Seaborn, Scikit learn 
*	AWS
* PostgreSQL 
*	WinSCP and Putty (tools for connecting to AWS)
* DataGrip (GUI for relational databases)

## References:
1.	https://www.ncbi.nlm.nih.gov/pubmed/14700410
2.	https://www.ahrq.gov/professionals/quality-patient-safety/pfp/haccost2017-results.html 
3.	https://www.ncbi.nlm.nih.gov/pubmed/27481738/

