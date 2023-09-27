# Machine Learning Fairness Exploration using LFR, C-LR, and C-SVM

## Background: 
Machine Learning Fairness refers to correcting the unfairness for certain groups or individuals in machine learning powered predictions. Fairness could be introduced in common 
machine learning practices. For example, unfair sampling or labeling in the training data causes selection bias. If a bank has been refusing credit to minority people without 
assessing them, the records of minority people are less sampled in the training data set. 

## Fairness Approach:
Threre are many different ways to handle the fairness issue in different phases of machine learning:
1. Preprocessing: we can modiy the distribution of the training data
2. Inprocessing: we can modify the cost function of the constraint of the learning algorithm
3. Post-processing: we can modify the prediction outcomes
4. Causal reasoning: we can use the concepts of counterfactual and interventional fairness

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
  
