# Machine Learning Fairness Exploration using LFR, C-LR, and C-SVM

## Background: 
Machine Learning Fairness refers to correcting the unfairness for certain groups or individuals in machine learning powered predictions. Fairness is a 
critical consideration because machine learning systems have the potential to perpetuate and amplify existing societal biases if not designed and deployed carefully.
Some considerations in machine learning fairness include:
* Bias and Fairness: Bias can manifest in various forms, including disparate impact, disparate treatment, and algorithmic bias. Disparate impact occurs when a model's predictions or decisions disproportionately affect different groups. Disparate treatment refers to explicit bias, where the model treats different groups unfairly. Algorithmic bias refers to the systematic and unfair discrimination present in model predictions.
* Protected Attributes: These are attributes like race, gender, age, sexual orientation, or disability status that are protected by anti-discrimination laws. Machine learning models should not make decisions that discriminate against individuals based on these attributes.
* Fairness Metrics: Various fairness metrics are used to assess and measure bias in machine learning models. Common metrics include disparate impact, equal opportunity, and demographic parity. These metrics help quantify the fairness of a model's predictions.

## Summary: 
This project studies the machine learning fariness to gain a better understanding of the trade-off between accuracy and fairness by implementing the following methodlogies

* The algorithms of Learning Fair Representations (LFR) introduced in the paper [Learning Fair Representations](http://proceedings.mlr.press/v28/zemel13.html) 
* Constrained Support Vector Machines (C-SVM) and Constrained Logistic Regression (CLR) introduced in the paper [Maximizing accuracy under fairness constraints](https://arxiv.org/abs/1507.05259 ) 

We further evaluate those three algorithms by looking into four metrics to more comprehensively assess the fairness of the models: 
* Accuracy - measures the overall correctness of a model's predictions
* Calibration - Calibration assesses whether the predicted probabilities from your model align with the actual outcomes. In the context of fairness, it's important to ensure that the predicted probabilities are well-calibrated across different groups, so that, for example, a predicted 70% probability of recidivism actually corresponds to a 70% likelihood of recidivism for all racial groups
* Parity - Parity metrics aim to assess whether different groups are treated equally by the model
* Equality of odds -  It evaluates whether false positives and false negatives are balanced across different groups

## Dataset:
We use the [COMPAS dataset](https://www.propublica.org/datastore/dataset/compas-recidivism-risk-score-data-and-analysis) (Correctional Offender Management Profiling for Alternative Sanctions) for this project: 

This dataset contains  the criminal history, jail and prison time, demographics, and COMPAS risk scores for defendants from Broward County from 2013 and 2014. The ground truth on whether 
or not these individuals actually recidivated within two years after the screening is also being collected. Recidivism is defined as a new arrest within two years. ProPublica’s analysis shows that the COMPAS risk scores are discriminatory against race and gender.

* Binary class label (y): "two_year_recid" column, indicating whether the defendant recificated within two years
* Binary sensitive attribute (z): "race" column, Caucasian and African-American

## Result - LFR
|                  | African American                 | Caucasian       |
| ---------------  | ---------------------------------| --------------- |
| Calibration      | 83.4%                            | 84.5%           |
| Equality of odds | positive: 77.2%, negative: 91.1% | positive: 99.6%, negative:73.2% |
| Parity           | 46.8%                            | 57.9%           |


  
