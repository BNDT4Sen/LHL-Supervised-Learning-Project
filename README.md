# Supervised Learning Project

## Part 1: EDA

Answers to the questions can be found near the top of the EDA.ipynb notebook in the Notebooks folder.


## Part 2: Preprocessing & Feature Engineering

The handling of missing values & outliers as well as scaling and normalization are labeled in the 'Feature Engineering.ipynb' notebook in the Notebooks folder.


## Part 3: Training ML Model

I trained PCA and Random Forest on the data set, comparing the predictor variables that were considered most important by either. Can be found in the 'Training ML Model.ipynb' notebook in the Notebooks folder.

## Part 4: Conclusion

- It seems as if pregnancy is one of the primary contributing factors. This was seen in the PCA, and makes sense intuitively. This does not quite align with what the random forest concluded, but the accuracy of that model is poor enough that it is likely wise to take it with a grain of salt. The PCA gave pregnancy a very high explained variance ratio, at just over 26%. Random forest was barely above 8% for pregnancies.

- Glucose was seen by both models to be either the largest or second largest factor correlating with incidences of diabetes. This also makes sense- insulin is used to control glucose levels. Impaired insulin production due to diabetes will probably result in higher blood sugar levels. The PCA contributed 21.7% of the variance to glucose levels. The random forest estimated over 25%.

- BMI and Age were the two factors that I initially thought would be the two most principal components, but this turned out to be quite wrong. PCA placed Age last, with less than 5% contribution, and BMI at under 7%.

- The diabetes pedigree function predicts the probability of diabetes depending on their family genetics. The PCA predicted that this explains 5.3% of the variation, and the random forest estimated 12.1%. At the very least genetics do not appear to be the largest factor when predicting if someone will have diabetes. This leaves controllable factors such as glucose levels and BMI as the most impactful. This knowledge can be used by individuals to mitigate their risk of developing diabetes later in life. But that isn't exactly a new revelation.