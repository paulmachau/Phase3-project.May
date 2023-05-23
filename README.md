# Phase3-project.May
Lessons Learned: H1N1 2009 Vaccination Campaign
Authors: Paul Ndungu Machau

Overview & Business Problem
Our task is to build a model that can use the patient health and demographics data collected following the 2009 H1N1 virus outbreak to predict which patients are likely to get the vaccine. Our focus will be the precision score. We wanted to use precision since it helps measure the true positives. In this case, maximizing the true positives and minimizing the false positives is paramount.

For this project, our stakeholder is the NYC Health. In the spring of 2009, a novel influenza A (H1N1) virus emerged. This new H1N1 virus contained a unique combination of influenza genes not previously identified in animals or people. Few young people had any existing immunity (as detected by antibody response) to the H1N1 virus, but nearly one-third of people over 60 years old had antibodies against this virus, likely from exposure to an older H1N1 virus earlier in their lives. We want to analyze this data in order to give future insights to predict vaccine rates in case something similar to another COVID outbreak happens.

DATA CONTRIBUTORS
Test_set_features
Training_set_lables.csv
Training_set_features.csv
submission_format.csv

Classification
Recall the distinction between classification and regression models:

Classification is used when the target variable is a category
Regression is used when the target variable is a numeric value
(Categorical data may be represented in the data as numbers, e.g. 0 and 1, but they are not truly numeric values. If you're unsure, ask yourself "is a target value of 1 one more than a target value of 0"; if it is one more, that is a regression target, if not, that is a classification target.)

You already practiced performing a regression analysis in Phase 2, and you will have additional opportunities to work on regression problems in later phases, but for this project, you must be modeling a classification problem.

DATA cleaning and Preparation
I then focused on doc_reccomendation, age-group, race, and health_insuarance. These attributes were converted to randomized strings, which did not help give any insights for our analysis.

 Focused more on health_insurance as we believed that this attribute would have had an impact on our model. I noted that there were a number of null values for this category and as such I also dropped the null values.

The remaining categories had a few nulls that could not be iterated, and were dropped as well. This resulted in a dataset of 20038 data points that we used for our model creation.

Modeling with the Dataset
Before i started our modeling, we utilized One Hot Encoder in order to classify categorical data as numerical values. I then used StandardScaler in order to scale our values to an appropriate range.

EVALUATION

Based on the results of the National 2009 H1N1 Flu Survey and the ML models developed, the findings suggest that the models had moderate performance in predicting the H1N1 vaccine status. The precision score of 0.81 indicates that a portion of individuals who received the vaccine was correctly identified by the models. However, there is still room for improvement in terms of accuracy.

One limitation of the study is that it only considered data from a single year, which may not capture the full complexity and variability of vaccine uptake over time. Moreover, the presence of imbalanced data and potential inaccuracies in the modeling process could have influenced the performance of the models. It is important to acknowledge that the findings are specific to the dataset and ML models used in this study.

Despite these limitations, the results highlight the potential of ML models in predicting vaccine uptake and informing public health interventions. Further research and refinement of the models are necessary to enhance their accuracy and generalizability. Additionally, considering data from multiple years and incorporating more comprehensive features may provide a more robust understanding of the factors influencing vaccine decisions.


