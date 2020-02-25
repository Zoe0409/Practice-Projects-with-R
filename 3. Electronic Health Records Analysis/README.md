# About The Data

We will be working with a simulated data set related to electronic health records and long-run outcomes for cardiology patients.

**File**:  ../Data/Homework 2 Data.csv

**Delimiter**:  Each column of the data set is separated with a comma **,** delimiter.

**Header** The first row of the data set includes the column names, and each subsequent row includes one observation of values.  

The data is written in long format (e.g. panel data). Each patient’s records are collected over time in one or more rows. Each row corresponds to a period of time. During this time, the patient’s status is recorded in terms of medications, hospitalizations, and complications. Each patient is followed until either death or the end of the follow-up period.

Here is a brief description of each variable:

 - id: This is a unique identifier for each patient. Because of strict privacy regulations, this identifier is anonymous. All records with the same value of id correspond to the same patient. This patient’s medical history is recorded in all of the rows with this id value. Some patients may have only a single row, while others may have many rows of updates.

 - begin: This is the beginning of the observation interval. This is defined as the number of days since the patient entered the study (see the definition of age above). The patient’s age at the beginning of the interval is the age variable (in years) plus the begin variable (in days).

 - end: This is the end of the observation interval. This is defined as the number of days since the patient entered the study (see the definition of age above). The observation interval is half open. This means that the begin date is included, while the end date is excluded. For patients with more than one row of records, the beginning of the next row should correspond to the end of the previous row. Any mismatches between these values constitute gaps in coverage, when we lack records on a patient. (For instance, if a patient switches insurance companies and then switches back, then we might lose a year’s worth of records.) The length of an interval in one row is therefore end - begin days. The patient’s age at the end of the interval is the age variable (in years) plus the end variable (in days).

 - age: This is the patient’s age in (rounded) years at the time of entry into the study – at the first diagnosis of coronary heart disease. For patients with multiple records in different rows, the age should be the same in every entry. For the purpose of this study, all of the patients should be at least 18 years old.

 - diabetes: This is an indicator of whether the patient had a diagnosed case of diabetes mellitus.

 - hypertension: This is an indicator of whether the patient had a diagnosed case of hypertension.

 - kidney_disease This is an indicator of whether the patient had a diagnosed case of kidney disease.
 
 - ace: This is an indicator of adherence for ACE Inhibitors, a common cardiovascular drug. This information is recorded based on a self-reported log that tracks the patient’s daily usage of the medicine. Therefore, we have the following coding for the values of ace:
        
    - 1: Possession;
        
    - 0: No possession.

 - beta.blocker: This is an indicator for adherence of Beta Blockers, a cardiovascular medicine. It has the same coding as that of ace.

 - statin: This is an indicator for adherence of Statins, another cardiovascular medicine. It has the same coding as that of ace and beta.blocker.

 - hospital: This is an indicator of whether the patient was in the hospital during the interval. Its values are coded as:
    
    - 1: Hospitalized;
    
    - 0: Not Hospitalized.
    
 - heart.attack: This is an indicator of whether the patient suffered a heart attack. When this occurs, the patient is assumed to go to the hospital and stay for some period of time (e.g. 1-7 days). The heart attack is assumed to happen at the beginning of the interval, and the remainder of this time is considered a recovery period. The values are coded as:
    
    - 1: Suffered a heart attack;
    
    - 0: No heart attack.
    death: This is an indicator of the end of the patient’s life. Its values are coded as:

    - 1: End of life;
    
    - 0: Patient is still alive.

 - Each patient is followed until either death or the end of the observation. Many patients with coronary disease were still alive at the end of follow-up.

**Note:** The description above tells you the intended structure of the data set. However, it’s possible that there could be problems lurking in the records. In the course of doing this assignment, you may uncover some issues. For instance, you may find an erroneous value in some of the variables. In this circumstance, it will be necessary to resolve the situation. Here are some guidelines for doing so:

 - If the issue has an obvious solution, then you may recode the data. For instance, if you see a value of TRUE for the heart.attack variable, then you may safely assume that this value should have been coded as a 1.

 - If the issue does not have an obvious solution, then you can replace the erroneous value with NA to denote a missing value.

In either circumstance, note the problem in your solution and briefly describe the work you did to clean the data.
