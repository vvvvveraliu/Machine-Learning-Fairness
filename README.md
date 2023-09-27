# Machine Learning Fairness Exploration using LFR, C-LR, and C-SVM

## Background: 
Machine Learning Fairness refers to correcting the unfairness for certain groups or individuals in machine learning powered predictions. Fairness is a 
critical consideration because machine learning systems have the potential to perpetuate and amplify existing societal biases if not designed and deployed carefully.
Some considerations in machine learning fairness include:
* Bias and Fairness: Bias can manifest in various forms, including disparate impact, disparate treatment, and algorithmic bias. Disparate impact occurs when a model's predictions or decisions disproportionately affect different groups. Disparate treatment refers to explicit bias, where the model treats different groups unfairly. Algorithmic bias refers to the systematic and unfair discrimination present in model predictions.
* Protected Attributes: These are attributes like race, gender, age, sexual orientation, or disability status that are protected by anti-discrimination laws. Machine learning models should not make decisions that discriminate against individuals based on these attributes.
* Fairness Metrics: Various fairness metrics are used to assess and measure bias in machine learning models. Common metrics include disparate impact, equal opportunity, and demographic parity. These metrics help quantify the fairness of a model's predictions.

## Project Summary:
This project studies the machine learning fariness by implementing the algorithms of Learning Fair Representations (LFR), Constrained Support Vector Machines (C-SVM) and Constrained Logistic Regression (CLR) on the COMPAS dataset. We further evaluate and compare those three algorithms by looking into four matrices: accuracy, calibration, parity and equality of odds.

## Dataset:
We use the COMPAS dataset (Correctional Offender Management Profiling for Alternative Sanctions) for this project: 
(https://www.propublica.org/datastore/dataset/compas-recidivism-risk- score-data-and-analysis) 
This dataset contains  the criminal history, jail and prison time, demographics, and COMPAS risk scores for defendants from Broward County from 2013 and 2014. 
The ground truth on whether or not these individuals actually recidivated within two years after the screening is also being collected.
Recidivism is defined as a new arrest within two years. ProPublica’s analysis shows that the COMPAS risk scores are discriminatory against race and gender.
* Binary class label (y): "two_year_recid" column, indicating whether the defendant recificated within two years
* Binary sensitive attribute (z): "race" column, Caucasian and African-American





This project focuses on implementing, 
evaluating and comparing algorithms for handling the fairness problem. 

* The Learning Fair Representations (LFR) methods from Zemel et.al
* Constrained Support Vector Machines (C-SVM) and Constrained Logistic Regression (CLR) from Zafar et.al.
  
