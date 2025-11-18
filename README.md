#Teacher Churn Prediction Project 
-
* This project is to apply the concept of predicting customer churn to teacher churn. 
* This is a real situation where the project was for a pre-high school chain that was facing high teacher churn which reflected poorly on student score and parent dis-satisfaction
* Various factors were considered after discussing with the management and available data. Some of the attributes considered are:
  * Teacher Ethinicity	- **Chinese**, **Indian**, **Malay**, **European** (Management felt there was a higher churn from language teachers like Chinese, Malay)
  * Teacher Age	- Older teachers less likely to churn - **20-60**
  * Teacher Tenure - Newer teachers more likely to churn - **1-20**
  * Student Ratio	- More students lead to higher teacher stress and hence they leave - **10-50**
  * Education (teacher)	- Not Graduates (**NG**), Under Graduates (**UG**), Post Graudate (**PG**) (churn more for non graduates)
  * Teacher Rating	- Performance rating (lower performance teachers more likely to churn) - **1**(Best), **5**(Worst)
  * Teacher rating last year(consistently lower performance teachers more likely to churn)
  * Sick days	- by Teacher (teachers who take more leaves may churn earlier) - **0-10**
  * Marital status	- **Married**, **Single**, **Divorced** (Single teachers more likely to leave)
  * Gender - **Male**, **Female**, **Binary**
  * Student Grade	- **Pre-K**, **Primary**, **Secodnary** (teachers more stressed in lower level)
  * Subject	(**STEM**, **English**, **Language**, **Sports**) - Stem and Language teachers in more demand

 * Data is stored in [Teacher Churn Data ] - ['https://raw.githubusercontent.com/gconsulting78-debug/machine-learning-zoomcamp-midterm_project/refs/heads/main/Teacher-Churn_Mid_Term_Project1.csv']

* Data was separated between numeric and categorical data with missing values replace by **0** and **NA** respectively
* EDA was performed by calculating ROC_AUC and Mutual Information Score respectively for numeric and categorical data
  * EDA on Numerical attibutes reveals highest ROC_AUC score for student ratio followed by teacher rating last year
  * EDA on Categorical data reveals highest information value for education followed by marital status
 
* train.py [
  * Used 4 classification models for the binary churn prediction - Logistic Regression, Decision Tree Classifier, Random Forest Classifier and XGBoost Classifier. XGBoost Classifier performed the best with best AUC of 0.8973
* predict.py for prediciting single teacher churn behavior with the given attributes
