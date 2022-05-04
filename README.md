  The purpose of this project is to predict mortality in ICU patients, as well as determine which factors are most deterministic in predicting whether
an ICU patient will die or not. The data comes from kaggle, and was originally sourced from MIT. It includes data on over 91,000 ICU patients from various countries,
including 200 hospitals in the US. 
  For this project, random forest, gradient boosted model, and logistic regression were all used. The Random Forest produced the best results, with 93% and 74% precision
rates for surviving and deceased patients respectively. And 99% and 24% recall rates from surviving and deceased patients respectively. The low recall rate comes from the 
dataset being unbalanced, with nearly 90% of instances being patients that survived. Oversampling and undersampling were both attempted, but those led to precision rates
that were far too low for production once tested on the validation set.
  This random forest model could be useful in determining which patients have a very high risk of death, as a patient classified as dying would have a 74% chance of dying 
based on this model. Moreover the random forest model analysis showed that the main factors in predicting death were two scores that are common in ICU's. They are the 
hospital death probability and the ICU death probabilty which are scores outputted based on a number of raw medical stats such as blood pressure, blood oxygen levels, etc...
Out of the raw medical stats minimum temperature, minimum blood oxygen levels, maximum temperature, and minimum systolic blood pressure were all identified as highly 
important features in the decision trees of this random forest model, suggesting they are some of the best predictors of ICU mortality.
  
