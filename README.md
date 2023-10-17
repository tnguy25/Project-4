# Project-4 Proposal

## Analyzing the Impact of Predictive Analytics on Student Success in Post-Secondary Education

## Project Scope and Purpose:
Our project aims to investigate the impact of predictive analytics on student success. Predictive analytics is increasingly being used in the education sector to identify at-risk students, optimize educational resources, and improve learning outcomes. However, it is essential to understand the efficacy of different student data as predictors and the the societal implications of setting education policy based on predictive analytics.

## Key Questions:
1. How effective are predictive analytics models in identifying successful and at-risk student in post-secondary education, when looking at non-academic performance related demographic data as predictors? 'Successful' and 'at-risk' for our purposes are defined as likely to graduate or drop out, respectively. Factors we will look at:
   - Students' parent background: Martital status, educational qualification, & occupation
   - Students' Nationality (National vs International & country of origin)
   - Unemployment & Inflation Rate at time of Student Enrollment
   - Student Scholarships

2. What policy recommendations can be made to ensure the responsible use of predictive analytics in education?

3. What are the ethical considerations and potential biases associated with using predictive analytics in education?

## Data Sources:
To conduct this analysis, we initially wanted to look at Canadian or US data, but found that student-centric data is generally not publically available. Therefore, we used a dataset from the **UC Irvine Machine Learning Repository** collected from institutions in Portugal

## Project Milestones:
### 1. Data Collection and Cleaning:
   - Acquire data from U Irvine
   - Perform data preprocessing, including handling missing values, removing duplicates, and standardizing data formats.
### 2. Exploratory Data Analysis (EDA):
   - Explore student demographic data
   - Create visualizations to understand trends and relationships within the data.
### 3. Predictive Analytics:
   - Select relevant features from the dataset
   - Choose machine learning models to predict student success and identify at-risk students.
   - Split data into training and testing sets, train models, and evaluate their performance:
     - Objective 1: Build predictive models that can classify students as likely to graduate or drop out based on historical data.
     - Objective 2: Evaluate the models' performance using appropriate metrics to assess their accuracy in identifying at-risk students.
     - Objective 3: Understand which features are most important in predicting student success and risk.
### 4. Dashboard Creation:
   - Create an dashboard using HTML/CSS.
   - Test the dashboard to ensure functionality and user-friendliness:
     - Objective 11: Create an interactive dashboard showcasing project findings.
     - Objective 12: Test the dashboard to ensure functionality and usability.
---

## Conclusions

### Parent background: Martital Status, Educational Qualifications, & Occupation
Based on the analysis of various classification models, including Random Forest Classifier, Logistic Regression, Support Vector Machine (SVM), and Multi-layer Perceptron (MLP) Classifier, it can be concluded that while they have some efficacy as predictors, Marital Status, Mother's Qualification, Father's Qualification, Mother's Occupation, and Father's Occupation, are not strong enough predictors for achieving high accuracy in predicting student success.

None of the models were able to achieve an accuracy above approximately 63%, which falls short of the acceptable 75% target accuracy. This suggests that our data on parents' background may not be sufficient to reliably predict the target variable or that other unconsidered factors may be influencing the outcome more significantly.

In summary, based on the models tested, these particular features alone may not be highly effective predictors for the given classification task. Further feature engineering or the inclusion of additional relevant features may be necessary to improve prediction accuracy.

### Student age at enrollment

### Student Nationality
Iin measuring the international and national background of a student against the target of outcome, graduation and dropout, there is a lack of correlation between the values with a p-value of 0.75. This tells an almost obvious but also important story that the national background of a student and their status, international or domestic, does not negatively or positively affect creating more graduates or dropouts. In creating the model using a decision tree for these values, there was difficulty in achieving an optimal or high accuracy score in isolating these features. The score achieved was only that of 0.47. The problem mainly comes from the data for nationality and international status being imbalanced data and the sample size for international and national students, as domestic students occupy the majority of the student body and foreign and international students make up a tiny percentage of students. 
   
The features of the nationality of students are not indicative of the model, but also, the features of the nationality of students are not indicative of ability and outcome.

### Unemployment & Inflation Rate at time of Student Enrollment
It is unsurprising to know that the the lower the unemployment rate is, the less likely that a student will drop out. It makes sense because if unemployment is low, which means the demand of labour is high, a job seeker has higher chance to have a job. This undermines the need of earning a degree. When unemployment is high, a job seeker is expected to be more competitive to be able to have a job. Using Random Forest, a 79% accuracy was attained.

After implementing efficient feature engineering (eliminating outliers and deleting repeating features) and deploying Deep Learning with the support of Dropout and Early Stopping, I was able to increase the accuracy from 79% to 90%

### Policy Recommendations

- **Balanced Feature Selection:** Emphasize the importance of selecting relevant and non-biased features for prediction, such as economic conditions, while being cautious about using sensitive or biased features like nationality or scholarships.

- **Transparency and Fairness:** Promote transparency in the model-building process and ensure that models are evaluated for fairness, mitigating any biases that may emerge.

- **Continuous Monitoring:** Implement ongoing monitoring of predictive models to assess their effectiveness and fairness, making necessary adjustments over time.

- **Privacy Protection:** Safeguard student data and ensure compliance with data privacy regulations to protect the rights and privacy of students.

### Ethical Considerations

- **Bias in Data:** Biases present in historical data can lead to biased predictions. Efforts should be made to identify and mitigate such biases.

- **Transparency:** Lack of transparency in model algorithms can make it difficult to understand how predictions are made, raising concerns about fairness and accountability.

- **Privacy:** Collecting and storing student data for predictive analytics must be done with strict adherence to privacy regulations and guidelines.

- **Discrimination:** Predictive models may inadvertently discriminate against certain groups of students, reinforcing inequalities in education.

- **Feedback Loops:** Overreliance on predictions can create self-fulfilling prophecies, where students are treated differently based on predictions, affecting their actual outcomes.

- **Stakeholder Involvement:** Ensure that students, educators, and parents are involved in the decision-making process regarding the use of predictive analytics in education to address concerns and foster transparency.

- **Algorithmic Accountability:** Establish mechanisms for holding institutions and algorithms accountable for their predictions and decisions.

- **Constant Monitoring:** Continuously monitor and audit predictive models for biases and fairness, correcting issues as they arise.

---
## Data Sources

**Predict students' dropout and academic success - UC Irvine Machine Learning Repository**
- https://archive-beta.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success
