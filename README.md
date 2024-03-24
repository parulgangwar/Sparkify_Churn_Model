# Sparkify churn Model Project

As part of Data Science Nanodegree program by Udacity, This is my third project named “Sparkify churn Model Project”. Sparkify is a fictional music streaming service, and this project simulates real-world scenarios where understanding and predicting churn are critical for business success. Sparkify is a imaginary music based company that offer online music services to it's customers. Services can be free and paid. Aim of this project is to predict the churn of Customer.

In today’s business world, keeping customers engaged and preventing them from leaving is quite important. Predictive analytics is actually an important tool that helps businesses predict what customers can do next. By using this information, companies can offer special deals or loyalty programs to keep customers happy and loyal. With so much data available nowadays, businesses are relying more and more on data science to make smart decisions and to brow business successfully. The Sparkify project for churn prediction typically involves using Apache Spark, a distributed computing framework, to analyze user interactions and predict churn – the likelihood that a customer will cancel their subscription or stop using the service. 

In this project, I’ll create the process of managing large datasets to extract significant features for predicting customer churn. Additionally, I’ll demonstrate the development and testing of machine learning models using Apache Spark’s PySpark API and PySpark ML Package. Code used for this blog could be found at GitHub repository. Main dataset “mini_sparkify_event_data.json” is a JSON file. It has 286500 rows and 18 columns. This data is of a fictional music streaming service named Sparkify. This dataset has been provided by Udacity as part of a Data Science Nanodegree course. for this project, the notebook was executed in a Spark environment directly on the IBM Watson Studio platform.

**Defining Churn : **
The term “Churn” refers to the customers who have discontinued using a company’s service or those who cancel their subscription. Our aim is to identify users who are at risk of leaving before they actually leave, if we know they are about to leave in advance then we can take proactive actions to retain these customers. Retaining existing customer is more important than acquiring new customers.

**The Project is divided into the following Sections:**

1. **Data Loading** : Main dataset “mini_sparkify_event_data.json” is a JSON file. It has 286500 rows and 18 columns.
2. **Data Cleaning** : Removed missing values for Users where data is not present, also removed unneccesary variables like FirstName and LastName. Created new variables based on timestamp.
3. **Exploratory Data Analysis**: Performed exploratory data analysis to see the churning behaviour, used visual techniques to understand the distribution of variables and corelation.
4. **Feature Engineering** : Created new features from the dataset. These variables show substantial discrepancies between churned and active users, suggesting their potential significance in predicting customer churn.
    * Number of songs played per user.
    * Count of ‘Thumbs Up’ page interactions per user
    * Count of ‘Thumbs Down’ page interactions per user
    * Count of ‘Add to Playlist’ page interactions per user.
    * Count of ‘Add Friend’ page interactions per user.
    * Count of ‘Error’ per user
    * Count of ‘length’ of songs listened per user.
    * Number of sessions per user
    * Count of ‘status’ per user
    * Count of ‘level’ per user
    * Gender
6. **Modeling** : For model development, I’ve utilized three different algorithms: Logistic Regression, Support Vector Machine (SVM), and Gradient Boosting. These algorithms offer different approaches to classification tasks, allowing for a comprehensive evaluation of model performance.
7. **Evaluation** : To evaluate the effectiveness of each model, I’ve employed two common metrics: the F1 score and the Area under the Curve (AUC). The F1 score provides a balance between precision and recall, making it suitable for imbalanced datasets or situations where both false positives and false negatives are equally important. The AUC metric measures the ability of the model to discriminate between positive and negative classes, with a higher AUC indicating better performance.
8. **Results** : After running the Logistic Regression, SVM (Support Vector Machine) and Gradient Boost Model, here are the F1 and AUC scores for these models:

      Score for logistic regression model:
      F1 Score: 0.7844468769407186
      AUC Score: 0.7767963831727738
      
      Score for Support Vector Machine:
      F1 Score: 0.7690553807154255
      AUC Score: 0.7346460272296704
      
      Score for Gradient Boost Classifier:
      F1 Score: 0.9733338852798261
      AUC Score: 0.9992440779015909
      
      From the scores, the gradient boost classifier is the top-performing model among the three models.
9. **Preventive actions to stop churn in the future** : Once we’ve identified potential churn customers using a prediction model, we can implement strategies to prevent them from churning.
This may involve running targeted promotional offers to incentivize these users. We can also investigate the underlying reasons why these users are dissatisfied with our product and address those issues. For example, we may need to make changes to the user interface or adjust subscription pricing or we can also check our web services.


## [Detailed blog has been created at Medium.](https://medium.com/@parulgangwar/sparkify-churn-model-c838a4df9d49)

**Files:**
* Sparkify_Churn_Model_Code.ipynb
* README.md

# Sparkify churn Model Project at Github
## [Github Link for Project](https://github.com/parulgangwar/Sparkify_Churn_Model)

**Software and Data Requirements:**

* Python
* Apache Spark’s PySpark API
* PySpark ML Package
* Dataset:mini_sparkify_event_data.json


