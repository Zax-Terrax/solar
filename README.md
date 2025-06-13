# solar

UNDER CONSTRUCTION

**SOLAR FARM – Predict Output based on Weather and Dust levels.**

**Overview**

Imagine predicting how much energy a solar farm will generate, just like forecasting the weather. 
That’s what this machine learning model does—it uses past data like sunlight, weather, and dust levels to estimate future electricity output. It’s built using a smart algorithm called Random Forest Regressor, which combines many decision trees to make accurate predictions. 
One key insight: dusty panels produce less electricity. So, while cleaning them boosts performance, it also costs time and money. The model helps further to find the sweet spot—balancing maintenance efforts with maximum energy efficiency, so solar farms stay both green and cost-effective. 
                     

**Data**

Data is based on a Kaggle dataset.
It contains measurements from a Solar Farm in India. Data has been cleaned and enriched with synthetic data point that represents the Days since last Cleanup and the Yield Output which is dependant on the dust level in a non linear pattern.
Data is not sensitive.


**Model**

A number of ML models have been used for this exercise.
- Polynomial Regression
- Gradient Boost Regressor
- Random Forest Regressor
- KNN
Random Forest has been chosen based on RMSE performance and training time.

**Hyperparameter Optimisation**

The Selected model has been tuned using Byesian Optimisation.
- Number of estimators (158)
- Max Depth (25)
- Min Samples Split (4)
- Min Samples Leaf (2)
- Max Features (0.2582)
These parameters needs to be re-tuned regularly as Input data patterns changes.

**Results**

The model is accurate in predicting the Electricity Output.
It can be easily adapted to include even more predictors data points.
The aim is to find the sweet spot of in the balance between maintenance cost and electricity output.
Adding the Cost of Cleaning and Income from Electricity then the ML can become a Reinforcement Learning problem:
- State = current panel condition & weather
- Action = clean or not clean
- Reward = Net profit
Train a model to learn the policy that maximizes long-term gain
