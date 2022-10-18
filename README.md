# Loan-Anomaly-Detection
Machine Learning Application with R (XGBoost, Random Forest, MLP)

Executive Summary (All figures and visualizations are shown in the PDF file)
[Anomaly Detection.pdf](https://github.com/EvanaZhang/Anomaly-Detection/files/9805307/Anomaly.Detection.pdf)


Business Objectives

This project’s objective is to build three different models (XGBoost, Random Forest, and MLP models) to predict and identify the default events of loan. In order to having a better understanding on the how the model works, here’re some steps to follow:
      
     • Identify anomaly events/cases and find out the anomaly rules for further business problem prediction.
     
     • Understand how each model work in different business cases
   

Key Findings 

• According to the results we got in the anomaly detection, there’re only 17 cases were identified as anomaly. Comparing to the total cases, it’s only 0.05% of the anomaly cases that chose to default their loans.

• By comparing all the importance plots in all three models, last_credit_pull_d, last_pymnt_amnt and last_pymnt_d are the top 3 variables that significantly impact all the models.

• In the variable loan_amnt, the percentage of default loan status is lower than 25%.


Model Performance Summary & Interpretation 

This dataset contains total 52 variables which includes 29 numeric variables and 23 character variables. The first step is check dataset profile by using the skim_without_chart() function, and then check the percentage of default loan status and current loan status. Next, explore the relationship between each of the categorical and numerical variables to see if each of them is being impactful and significant enough for building models and or for further predicting. Prior to the partition is to select the variables based on the exploratory plots.

      XGBoost Modeling
      
      • Set the number of trees as 20
      
      • Randomly tune three parameters (trees depth, min_n, learning rate) with different size of 10
      
      • The best and reasonable XGBoost model is the model with 10 tree depth, 8 minimum number of variables and a learning rate of 0.035251.

      Random Forest Modeling
      
      • Randomly tune 3 parameters to a total of 10 different size: trees values with a range of 100 to 200, min_n with no range, and a mtry of 11.
      • The best and reasonable Random Forest model is a model with 176 trees, and with a minimum number of variables of 8.
      
      Multilayer Perception Modeling
      
      • Tuned 3 parameters with 10 different sizes: epoch with a range between 10 to 20, penalty with a range of 0 to 1, and hidden_units with a range of 1 to 6
      • The best and reasonable multilayer perception model is a model with hidden units of 6, penalty of 5.056619, and a epochs of 20.
    

Conclusion 

• Tree depth determines the depth of the trees; the min_n indicates the minimum number of variables and the learning rate manifests the coefficient when tuning.

• Epoch indicates the number of times the dataset passes the model; penalty decides the model’s loss function; hidden units control the number of functions for the model’s input.

• By comparing the ROC_AUC and the accuracy from the Multilayer Perception, XGBoost and Random Forest models. XGBoost model will be the best model to fit the data. That’s why using the XGBoost model to do the kaggle prediction with the highest values on both accuracy and roc_auc.


Recommendations

• The company should consider focus on the number of payments on the loan with a 60 month more.

• The interest rate is also a focus point need to pay attention to.





