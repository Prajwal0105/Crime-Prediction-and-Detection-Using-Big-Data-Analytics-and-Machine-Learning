# Crime Prediction and Detection Using Big Data Analytics and Machine Learning

## Project Overview

One of the biggest challenges for any nation is the prevention of crime. However, due to the dynamic nature of criminal activities, manual efforts to detect and predict crime are often insufficient. This project presents an optimal approach to **crime prediction and detection** by leveraging **Big Data Analytics** and **Machine Learning (ML)** techniques. The goal is to improve public safety by forecasting crime occurrences, enabling law enforcement to make data-driven decisions.

## Dataset

The dataset used for this project is the [**NYPD Complaint Historic Dataset**](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i), a real-time public dataset containing records of major crimes that occurred in New York City from 2006 to 2023. It includes over 9.9 million criminal instances with details such as the type of crime (felony or misdemeanor), location, and date of occurrence.

---

## Technologies and Tools

- **Programming Languages**: Python, PySpark, Spark SQL
- **Databricks**: A cloud platform for scalable data engineering, ML, and data analytics
- **Machine Learning Algorithms**:
  - Logistic Regression
  - Random Forest Classifier
- **Big Data Frameworks**:
  - PySpark: Used for distributed data processing
  - Spark SQL: To streamline data queries and enhance processing speed

---

## Project Architecture

![Architecture Diagram](https://github.com/Prajwal0105/master-thesis-project/blob/main/Architecture%20diagram.png)

---

## Methodology

### 1. **Data Preprocessing**
   - Removal of irrelevant data and imputation of missing values.
   - Conversion of time-based columns to datetime format, followed by extraction of features such as year, month, day, and hour.
   - Focus on key features like age, gender, and crime category for prediction.

### 2. **Exploratory Data Analysis (EDA)**
   - Analysis of crime frequency, type, and geographic distribution.
   - Visualization of crime data across different boroughs of New York City.
   - SQL-based queries for in-depth analysis, including gender-based crime counts and age-specific crime statistics.

![Graph1](https://github.com/Prajwal0105/master-thesis-project/blob/main/Graph1.png)

### 3. **Model Training and Evaluation**
   - Implemented **Logistic Regression** and **Random Forest Classifier** to classify crimes.
   - **Confusion matrix** and **classification tables** were used to evaluate model performance.
   - Logistic Regression achieved **51% accuracy**, while Random Forest achieved **99% accuracy**, making Random Forest the optimal model for this use case.

![Random Forest](https://github.com/Prajwal0105/master-thesis-project/blob/main/Random%20Forest.png)

---

## Key Results

- **Logistic Regression**:
  - Accuracy: 51%
  - Due to a higher number of false positives and false negatives, this model did not perform optimally for crime prediction.
  
- **Random Forest Classifier**:
  - Accuracy: 99%
  - Random Forest significantly outperformed Logistic Regression, making it the recommended model for real-time crime prediction.

---

## Conclusion

The integration of **Big Data Analytics** and **Machine Learning** in this project demonstrates a powerful approach to predicting and detecting crime. By leveraging vast datasets and predictive models, law enforcement agencies can take proactive measures to prevent criminal activities. With an accuracy rate of 99%, the **Random Forest Classifier** proved to be the most effective model in predicting crime rates based on factors such as age, gender, and location.

### Future Work

- Extending this project by integrating **computer vision** and **CCTV footage** to identify crime hotspots in real-time.
- Incorporating larger datasets and advanced deep learning algorithms to enhance prediction accuracy.

---

## Project Repository

- **Dataset**: [NYPD Complaint Data](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i)
- **Code**: [Crime Prediction Code](https://github.com/Prajwal0105/master-thesis-project/blob/main/crime_prediction_pyspark.ipynb)
