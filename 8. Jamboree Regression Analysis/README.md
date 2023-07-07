# Jamboree

Jamboree has helped thousands of students like you make it to top colleges abroad. Be it GMAT, GRE or SAT, their unique problem-solving methods ensure maximum scores with minimum effort.
They recently launched a feature where students/learners can come to their website and check their probability of getting into the IVY league college. This feature estimates the chances of graduate admission from an Indian perspective.

## Problem Statement :

- Help Jamboree in understanding what factors are important in graduate admissions and how these factors are interrelated among themselves. It will also help predict one's chances of admission given the rest of the variables.

### Column Profiling:

    Serial No. (Unique row ID)
    GRE Scores (out of 340)
    TOEFL Scores (out of 120)
    University Rating (out of 5)
    Statement of Purpose and Letter of Recommendation Strength (out of 5)
    Undergraduate GPA (out of 10)
    Research Experience (either 0 or 1)
    Chance of Admit (ranging from 0 to 1)

### Concept Used:
    
- Exploratory Data Analysis
- Linear Regression

### Insights and Recommendations

Insights, Feature Importance, and Interpretations and Recommendations: 

- The first column was observed as a unique row identifier which was dropped as it was not required for model building.
- University Rating, SOP and LOR strength and research seems to be discrete random Variables, but also ordinal numeric data remaining features are numeric, ordinal, and continuous.
- No null values were present in the dataset.
- No Significant amount of outliers were found in the data.
- Chance of admission(target variable) and GRE score(an independent feature) are nearly normally distributed. 
       - Independent Variables (Input data): GRE Score, TOEFL Score, University Rating, SOP, LOR, CGPA, Research 
       - Target/Dependent Variable: Chance of Admit (the value we want to predict)

- From the correlation heatmap,  GRE score, TOEFL score, and CGPA have a very high correlation with Change of admission as observed.
- University rating, SOP, LOR, and Research have comparatively slightly less correlated than other features.
- Chances of admission is a probability measure, which is within 0 to 1 which is good (no outliers or misleading data in column). 
- Range of GRE scores looks between 290 to 340, range of TOEFL scores is between 92 to 120 while university rating, SOP, and LOR are distributed between a range of 1 to 5. and  CGPA range is between  6.8 to 9.92.
- From boxplots (distribution of chance of admiration (probability of getting admission) as per GRE score ): with a higher GRE score, there is a high probability of getting admission.
- Students having high TOEFL score, has a higher probability of getting admission.
- From the count plots, we can observe, the statement of purpose SOP strength is positively correlated with the Chance of Admission.
- We can also discover a similar pattern in Letter of Recommendation strength and University rating, which have a positive correlation with Chances of Admission.
- Students having research has higher chances of Admission, but also we can observe some outliers within that category.

Actionable Insights and  Recommendations : 

- Educational institutes can not just help the student to improve their CGPA score but also assist them in writing good LOR and SOP thus helping them admit to a better university.
- The educational institute can not just help the student to improve their GRE Score but can also assist them in writing good LOR and SOP thus helping them admit to a better University.
- Awareness of CGPA and Research Capabilities: Seminars can be organized to increase awareness regarding CGPA and Research capabilities to enhance the chance of admission.
- Any student can never change their current state of attributes so awareness and marketing campaigns need to be surveyed hence creating a first impression on students at the undergraduate level, which won't just increase the company's popularity but will also help students get prepared for future plans in advance. 
- A dashboard can be created for students whenever they log in to your website, hence allowing healthy competition also to create a progress report for students.
- Additional features like the number of hours they put in studying, watching lectures, assignments solved percentage, and marks in mock tests can result in a better report for every student to judge themselves and improve on their own.

Regression Analysis : 

- From the regression analysis (above bar chart and REPORT file), we can observe that CGPA is the most important feature for predicting the chances of admission. 
- Another important features are GRE and TOEFL scores. 
- After the first Regression Model, checked for Multicolinearity. Getting all the VIF scores below 5, showing there's no high multicolinearity.
- All the residuals are not perfectly normally distributed. and so residual plot we can observe some level of heteroscedasticity.
- Regularised model ridge and lasso both give very similar results to Linear Regression Model. 
- Similarly, ElasticNet (L1+L2) also returns very similar results. along with the rest of the model metrics.

### Solution Link

Notebook Link: https://drive.google.com/file/d/11bdQePbL78mg-JfuRIu6J7rRCqJ-gSAF/view?usp=sharing
PDF: https://drive.google.com/file/d/1Ei4Ke_xDPxgj_4Tfjg5TPcpPScKa9ozf/view?usp=sharing
