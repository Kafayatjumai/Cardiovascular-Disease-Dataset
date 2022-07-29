# Cardiovascular disease dataset.
## by Kafayat Saka


## Dataset
 > Introduction 
 > Cardiovascular diseases (CVDs) are a group of disorders of the heart and blood vessels. CVDs are the leading cause of death globally.An estimated 17.9 million people died from CVDs in 2019,representing 32% of all global deaths. Of those deaths, 85% were due to heart attack and stroke.

   Most cardiovascular diseases can be prevented by addressing behavioural risk factors such as tobacco use, unhealthy diet and obesity,physical inactivity and harmful use of alcohol.
     
   As the leading cause of death globally, it is important to detect cardiovascular disease as early as possible so that management with counselling and medicines can begin.
   
   > The Cardiovascular disease dataset consists of 70,000 records of patients data.    
   
   This dataset is made up of 12 columns of patients records. 
   
   These columns are:
   
   1) AGE: This is the age of patients, a Quantitative variable.
   
   2) HEIGHT: This is the height of patients and is recorded in (cm) and a Quantitative variable.
   
   3) WEIGHT: This is the patients weight in (kg) and is a Quantitative variable.
   
   4) GENDER: This is the gender of the patient which can either be Male or Female. This is a Qualitative variable.
   
   5) SYSTOLIC BLOOD PRESSURE(ap_hi): This is one of two of the variables used in measuring blood pressure. This measures the pressure in your arteries when your heart beats. Its unit is in (mmHg). This is a Quantitative variable.
   
   6) DIASTOLIC BLOOD PRESSURE(ap_ho): This is the second of the variables used in measuring blood pressure. This measures the pressure in the period between heartbeats, when the heart rests. Its unit is in (mmHg).This is a Quantitative variable.
   
   7) CHOLESTEROL:This is a fat-like substance made in  the liver and found in the blood and in all cells of the body. High proportion of it is associated with an increased risk of heart disease. Its unit is in (mmol/L).This is a Qualitative variable.
   
   8) GLUCOSE: This is a simple sugar that is an important energy source in living organisms and is a component of many carbohydrates.Its unit is in (mmol/L).This is a Qualitative variable.
   
   9) SMOKING: This is an act of inhaling and exhaling fumes of burning plant materials. This is a Qualitative variable.
   
   10) ALCOHOL INTAKE: This is the act of ingesting-typically orally - a beverage containing ethanol.This is a Qualitative variable.
   
   11) PHYSICAL ACTIVITY: This is any bodily movement produced by skeletal muscles that require energy expenditure.This is a Qualitative variable.
   
   12) PRESENCE OR ABSENCE OF CARDIOVASCULAR DISEASE: This is the target variable of the dataset that indicates whether or not the patient has a cardiovascular disease.This is a Qualitative variable.
   
   >All of the dataset values were collected at the moment of medical examination.

## Preliminary Wrangling
   I obtained this dataset from kaggle https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset 

1) The age column came in days so i had to clean and round it up to years.

2) I change all the qualitative features of the dataset that were integer type to object type

3) I changed most of the column names to better naming conventions

4) I replaced values in the qualitative columns with their corresponding names as indicated on kaggle where i got the dataset from.

5) I Feature engineered a new column,BMI. By performing calculations with the weight and height column.

6) I converted categorical ordinal data types to CategoricalDataType.

At the end of my data wranging the structure of my dataset was 70,000 rows and 13 columns.

## Summary of Findings

> Univariate exploration:

 1) The dataset involves adults mainly from 30-65years.

 2) The largest distribution of patients fell into a height of 165cm and a weight of 70kg.

 3) Atleast 50,000 of the patients have both Normal Glucose and Cholesterol levels.

 4) The largest distribution of patients fell into a BMI score of 24.

 5) More than 90 percent of the patients do not drink alcohol

 6) More than 60,000 of the patients do not smoke and more than 50,000 of them perform physical activities.

 7) The highest distribution of patients fell into those with a systolic of 120-125mmHg and a diastolic of 80-85mmHg

 8) The patients diagnosed with cardiovascular disease was approximately equal to those without.

> Bivariate exploration:

 1) Majority of the patients fall between 100-175mmHg for systolic and 60-100mmHg for diastolic.

 2) Patients with normal cholesterol level have cardiovascular disease

 3) Most Patients in the distribution have have a high BMI.
 
 4) There was no significant relationship between smoking and weight.

> Multivariate exploration:

 1) Patients with BMI greater than 25kg/m2 have cardiovascular disease.

 2) Patients with a diastolic lower than 90mmHg and a systolic lower than 125mmHg do not have a cardiovascular disease.

## Key Insights for Presentation:

 1) The amount of Females that have cardiovascular diseases is about 14,000 more than the males that have this cardiovascular disease. 

 This was first explored by checking the general population plot where I discovered that approximately 50% of the population had and the other 50% did not have cardiovasculr disease. I furthered explored the distribution with gender where I observed and concluded that more females have cardiovascular diseases than the males.


 2) Most Patients in the distribution have a BMI greater than 25: 
 
   This was suspected from the first exploration of the bmi variable alone, After plotting the relationship with weight, it showed a large distribution of patients fell into the bmi greater than 25.

 3) Patients with BMI greater than 25kg/m2 and Weight above 80kg have cardiovascular disease:

This finding was concluded from exploring the individual variables, i.e the weight, bmi and cardiovascular disease,with plots, then the relationship between Bmi and weight and the final exploration of the relationship between all three variables using scattered plots.

  4) A large distribution of the patients have high blood pressure.

This finding was concluded from exploring the systolic and diastolic variables individually then their relationship together where a positive correlation was noticed too. A final scatter plot was plotted to see the relationship between all three variables.

> Changes made
 After the first review it was brought to my knowledge one of the scatter plots was overplotted. So i changed the plot using seaborns stripplot to better visualize the data and show the data distribution better for accuarate findings.