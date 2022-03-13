# Neural_Networks_Classification_problem_Heart_disease-and-Mortality



The Monica dataset from https://vincentarelbundock.github.io/Rdatasets/doc/DAAG/monica.html has been chosen.

This dataset has been chosen for several reasons:



* - for having categorical and numerical variables.
* - for having a number of variables greater than 10, a criterion that has been adopted to make the study representative.
* - for having a high number of observations, greater than 5000.


### **Structure**

This dataset has the following structure:



* Package: DAAG
* Item: Monica
* Title: WHO Monica Data
* Rows:6367
* Cols:12
* n_binary:3
* n_character:0
* n_factor:10
* n_logical:0
* n_numeric:2


## **Variables**

The variables are:



* outcome: mortality outcome, a factor with levels live, dead
* age:age at onset
* sex: m = male, f = female
* hosp:y = hospitalized, n = not hospitalized
* yronset:year of onset
* premi: previous myocardial infarction event, a factor with levels y, n, nk not known
* smstat: smoking status, a factor with levels c current, x ex-smoker, n non-smoker, nk not known
* diabetes: a factor with levels y, n, nk not known
* highbp: high blood pressure, a factor with levels y, n, nk not known
* hichol: high cholesterol, a factor with levels y, n nk not known
* angina: a factor with levels y, n, nk not known
* stroke: a factor with levels y, n, nk not known

    **Observations**


    The number of observations for each class is:

* dead: 2842
* live:3525

    The minority class, which is the dead class, is well represented enough so that it does not offer limitations to its study, modeling, and classification.


    Base Accuracy: 55.36% 


    Reference base failure rate: 44.64%



# Conclusions

1) Indeed, there are substantial divergences between the Failure Rate and the AUC, since it is obtained that in terms of Failure Rate the Xgboost model is the best, followed (as far as simple s models are concerned) by Gbm and Rf. However, given these divergences, the AUC was chosen as a diagnostic measure due to these inconsistencies, thus highlighting the logistic regression model as the one that behaves best.

2) The simple algorithms that work best with respect to AUC are logistic regression, Gbm and Xgboost.

3) The model that presents the highest AUC is the one formed after the assembly procedure by means of the combination (unipredi$logi+unipredi$gbm)/2, it is the predi11 model and it presents the values ​​of AUC =0.9198173 and failure rate =0.1202136

4) In these data, even though the pred11 model has better performance in terms of AUC, since the difference with the logistic regression is small (0.0001682), the logistic regression is chosen as the **best model to model the dataset in question**. This presents the values ​​of AUC =0.9196491 and failure rate =0.1206063
