# Red-Wine-Classification
A survey of machine learning methods and SMOTE oversampling to classify imbalanced data

Data source (Kaggle): https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009

## ABSTRACT
Many data analysis tasks are complicated by a very common phenomenon, the tendency of samples to group toward certain values or classes which can result in imbalanced models if not properly considered.  The Red Wine Quality dataset is an example of this; there are 1599 rows corresponding to wine samples, judged on an ordinal scale for quality, each accompanied by 11 columns of physiochemical characteristics.  Naturally, most of the wines receive an average score, with only select samples earning a .7-.8 and a “fine” classification.  In this analysis, domain knowledge of wine chemistry and model balancing techniques were combined to find the model with the best ability to distinguish “fine” from “regular” wines, primarily using precision and recall metrics due to the imbalance in classes.  Two approaches were used on appropriate models for their implementation: threshold tuning was utilized to choose features in a logistic regression framework, and the Synthetic Minority Oversampling Technique (SMOTE) was used within cross-validation selection of random forests and extreme gradient boosted trees.  Logistic regression, even after variable selection and tuning, showed inferior performance to the tree methods.  Tree methods with classes fully balanced with SMOTE performed worse on test data than those with no oversampling, indicating overfitting was an issue, but the best model proved to be extreme boosted trees with the minority class oversampled only 300% with SMOTE.  This model along with its equivalent random forest showed that the best predictors for fine wine quality were alcohol and sulfate levels.


<img src ="https://github.com/stephc027/Red-Wine-Classification/blob/main/images/xgboost%20wine%20variables.png?raw=true" width="500">
<img src ="https://github.com/stephc027/Red-Wine-Classification/blob/main/images/xgboost%20pd%20plots.png?raw=true" width="500">
