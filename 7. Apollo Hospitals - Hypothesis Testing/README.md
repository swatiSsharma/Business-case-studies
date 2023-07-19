# Apollo Hospitals - Hypothesis testing

Apollo Hospitals was established in 1983, renowned as the architect of modern healthcare in India. As the nation's first corporate hospital, Apollo Hospitals is acclaimed for pioneering the private healthcare revolution in the country.

As a data scientist working at Apollo 24/7, the ultimate goal is to tease out meaningful and actionable insights from Patient-level collected data.

You can help Apollo hospitals to be more efficient, influence diagnostic and treatment processes, and to map the spread of a pandemic.

One of the best examples of data scientists making a meaningful difference at a global level is in the response to the COVID-19 pandemic, where they have improved information collection, provided ongoing and accurate estimates of infection spread and health system demand, and assessed the effectiveness of government policies.

#### Business Problem Statement

1. Clean, sanitize and manipulate data to identify which variables are significant in predicting the reason for hospitalization for different regions.
2. Analyze how well some variables like viral load, smoking, and Severity Level describe the hospitalization charges.

#### Dataset
https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/681/original/scaler_apollo_hospitals.csv

#### Column Profiling

Age: This is an integer indicating the age of the primary beneficiary (excluding those above 64 years, since they are generally covered by the government).
Sex: This is the policyholder's gender, either male or female
Viral Load: Viral load refers to the amount of virus in an infected person's blood
Severity Level: This is an integer indicating how severe the patient is
Smoker: This is yes or no depending on whether the insured regularly smokes tobacco.
Region: This is the beneficiary's place of residence in Delhi, divided into four geographic regions - northeast, southeast, southwest, or northwest
Hospitalization charges: Individual medical costs billed to health insurance

#### Concept Used

- Graphical and Non-Graphical Analysis
- 2-sample t-test: testing for differences across populations
- ANOVA
- Chi-square

#### Insights & Recommendations

> Insights

Non-smokers are approximately 5 times more in number than Smokers.
The number of patients with a Severity Level of 1 is less than the number of patients with a Severity Level of 0.
The number of patients with Severity Level 2 is less than the number of patients with Severity Level 1.
The number of patients with Severity Level 3 is less than the number of patients with Severity Level 2.
The number of patients with Severity Levels 4 and 5 is less than the number of patients with Severity Level 3.
The majority of the patients have low Hospitalization Charges.
Smokers have significantly higher Hospitalization Charges than Non-smokers.
There is no significant difference between Viral Loads for Males and Females.
The proportion of Smokers is significantly different across different regions.
The mean viral load is the same for women with different severity levels.
Patients with Severity Levels 4 and 5 are less than patients with Severity Levels 0, 1, 2, and 3.

> Recommendations

The smoker column should be used as a variable in predicting the Hospitalization Charges.
The gender column should not be used as a variable in predicting the Viral Loads.

#### Solution to Given Problem

Link: (https://drive.google.com/file/d/1zbxGWYVydS8IZap2XSpdvP8tZUurgug8/view?usp=sharing)
The smoker column should be used as a variable in predicting the Hospitalizations across different regions.
The severity Level column should not be used as a variable in predicting the Viral Loads for Women.
