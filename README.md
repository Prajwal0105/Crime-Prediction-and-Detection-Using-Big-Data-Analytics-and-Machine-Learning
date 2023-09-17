# MASTER THESIS PROJECT

# An Optimal Approach Towards Crime Prediction and Detection Using Big Data Analytics and Machine Learning

## DESCRIPTION
One of the major threats that a nation experiences is a threat resulting from crime. However, prevention of such happenings is a challenging task since a perfect mechanism to detect crime cannot be established due to the dynamic nature of criminal activity. In addition to this, it is difficult for humans to manually process large amounts of criminal data and perform a background check of the same. Therefore, the scenario is opted to be controlled through the computational algorithms wherein crime predictions and forecasting can be made in order to improve the safety of the populace and accurately detect crime rates. Hence, it can be concluded that such problems can be addressed by incorporating advanced technology with manual detection of crime.

## DATASET USED
The Dataset used for the implementation of this thesis is [NYPD complaint historic dataset ](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i).
This real time dataset is being made publically available and consist of all the major crimes that have taken place in the city of NewYork and keeps updating every three months. Validated crimes by the NYPD are reported and classified as felony or misdemeanour. The dataset contains historic criminal rates from 2006 to 2023. In addition to this; the dataset also consists spatio-temporal and geographical locations such as time, date and coordinates of the crime. A total of 35 columns are present in the dataset. The dataset obtained to implement the thesis is acquired from the NYPD Complaint Historic Data which comprises of 9,963,369 criminal instances.


## CODE USED
The Code file has been uploaded above in the repository - [Code](https://github.com/Prajwal0105/master-thesis-project/blob/main/crime_prediction_pyspark.ipynb)

## Architecture Diagram/ Proposed Methodology
![Architecture Diagram](https://github.com/Prajwal0105/master-thesis-project/blob/main/Architecture%20diagram.png)



## TECHNOLOGY USED

- **Programming Language:** PySpark, Python, Spark SQL
- **Databricks:**
  - It is a web-based platform that works in accordance with Spark and is therefore used to build, deploy, share and maintain various technical grade data at a larger scale.
  - It can be used as platform to create and deploy analytical models on cloud by using machine learning based algorithms.
  - Hence, we have used Databricks combined with Spark so that accurate results can be generated and an optimized model of the same can be built.
- **PySpark:**
  - The implementation of PySpark through the usage of ML library makes the entire process feasible and scalable to the user and thereby works through distributed systems.
  - PySpark is majorly used for data analysis wherein techniques of machine learning such as classification, regression and mining strategies are used.
- **Spark SQL:**
  - It is a combination of Spark with SQL is majorly done so as to streamline the process of querying user data.
  - It is specially designed to meet the requirements of cloud computing technology and tends to generate results at a faster pace.
- **Machine Learning Techniques:**
  - *Logistic Regression:* Logistic Regression is a statistical method used for classification tasks, which involve categorizing data points into distinct classes or categories.
  - *Random Forest Classifier:* Random Forest is a versatile and powerful ensemble machine learning technique used for both classification and regression tasks. It's an extension of the decision tree algorithm and is known for its high accuracy, robustness, and resistance to overfitting.


## IMPLEMENTATION DETAILS

### Data Cleaning and Pre-processing
- The removal and elimination of irrelevant data in the form of column attributes is performed in the data pre-processing stage.
- Following are the steps which are taken under the data pre-processing stage of this study:
  - Impute the missing values and drop all other NULL entries which are not required for the process of implementation.
  - Convert columns of “Start-Time” to datetime. The newly acquired datetime column is further expanded to year, day, month and hour.
- The presented research study aims to predict crime rates on the basis of age, gender and category. Therefore all the other columns are to be discarded in the data pre-processing stage.

### Exploratory Data Analysis and Visualization
- One of the major techniques used to extract features and trends from Machine Learning algorithms is the adoption of Exploratory Data Analysis (EDA).
- The dataset obtained to implement the thesis is acquired from the NYPD Complaint Historic Data which comprises of 9,963,369 criminal instances. The graph below depicts the most frequently occurring crimes in NY.
- There are more misdemeanour than felony and violation combined, reflecting that NYC is a lot safer than depicted by movies and TV dramas.
- The table below mentions the geographic coverage of crimes in NY based boroughs.
![Table](https://github.com/Prajwal0105/master-thesis-project/blob/main/Table.png)
- The EDA representation below illustrates the geographic coverage of the same
![EDA](https://github.com/Prajwal0105/master-thesis-project/blob/main/Graph.png)
- In the next stage, an SQL query is triggered using Spark SQL, to plot the offence level with respect to gender of the criminal. The count of offence is also calculated from the given number of instances.
![Table1](https://github.com/Prajwal0105/master-thesis-project/blob/main/Table1.png)
- In the next step; an SQL PySpark based query is triggered to give the number of criminal counts that took place within a specific range of age group.

![Table2](https://github.com/Prajwal0105/master-thesis-project/blob/main/Table2.png)

![Graph1](https://github.com/Prajwal0105/master-thesis-project/blob/main/Graph1.png)

### Performance Evaluation
- The performance of the suggested thesis must be assessed in relation to a number of characteristics before it can be put into practice. Evaluation of these variables aids in accurate crime rate forecasting in New York. 
- Training loss and validation loss are regarded as crucial assessment parameters that are necessary for assessing the effectiveness of the trained model. 
- Utilizing a confusion matrix as a basis for evaluation of a system model is another crucial component.

## EXPERIMENTAL ANALYSIS AND RESULTS

### Logistic Regression:
Logistic Regression is a statistical method used for classification tasks, which involve categorizing data points into distinct classes or categories.
- Below is a confusion matrix that has predicted and classified the crimes occurring is observed.

![Logistic Regression](https://github.com/Prajwal0105/master-thesis-project/blob/main/Logistic%20Regression.png)

The above confusion matrix has classified the offence level using the numbering as:
0 denotes felony
1 denotes misdemeanour
2 denotes violation

- Since a single line on the left is predicted and not a diagonal line; this prediction model of logistic regression has not performed efficiently. 
More number of wrong predictions in the form of false positive (FP) and false negative (FN) values are thus obtained which are indicated by the values 0.

- The classification table of the same is illustrated below:

![Table](https://github.com/Prajwal0105/master-thesis-project/blob/main/Logistic%20Reg-%20Classification%20table.png)

The target class of 0,1 and 2 are chosen to represent crime classification in the form of felony, misdemeanor and violation respectively. An accuracy and precision factor of 51% is observed through the implementation of logistic regression.

### Random Forest Classifier:
Random Forest is a versatile and powerful ensemble machine learning technique used for both classification and regression tasks.

- Below is a confusion matrix that has predicted and classified the crimes occurring is observed.
  
![Random Forest](https://github.com/Prajwal0105/master-thesis-project/blob/main/Random%20Forest.png)

The above confusion matrix has classified the offence level using the numbering as:
0 denotes felony
1 denotes misdemeanour
2 denotes violation

- The output generated using random forest as the classifier is observed to occur in a diagonal manner.
The right prediction as true positives and true negatives are presented diagonally; whereas the wrong prediction is represented as 0, 287 and 11.

- The classification table of the same is illustrated below:
  
![Table](https://github.com/Prajwal0105/master-thesis-project/blob/main/Random%20Forest-%20Classification%20table.png)

The target class of 0,1 and 2 are chosen to represent crime classification in the form of felony, misdemeanor and violation respectively. An accuracy and precision factor of 99% is observed through the implementation of Random Forest Classifier.

## RESULT

- Since the primary aim of the thesis is to classify various forms of crimes being taking place on the online platform; we have achieved this using two machine learning based algorithms; namely logistic regression and random forest. 
- On conducting experimental analysis of the same further followed by parameters of evaluation; their accuracy factors were generated. 
- As observed in this section confusion matrix and a classification table were used to determine the accuracy. 
- On implementation; logistic regression generated 51% accuracy whereas; random forest generated 99% accuracy. 
- Therefore, the designed model of random forest is narrated to be the optimized model with highest generating results.

## CONCLUSION

- Detecting the occurrence of crime is one of the most important factors used to monitor the crime rates of a city. On the other hand; predicting one is another significant challenge which must be fulfilled in order to decrease the occurrence of crime rates.
- As observed in the literature survey; ML and DL based algorithms have been adopted to eliminate crime rates in various cities based on geographical locations, age, gender, unemployment etc. 
- However, there are certain limitations of the existing systems and are highlighted as below:
- An automated and accurate system is required that can precisely detect and predict the occurrence of crime rate in real time
- A larger and validated criminal dataset is required so that crime rates in metropolitan areas can be detected.
- In conclusion, this research presents the integration of vast and diverse datasets, coupled with advanced predictive models, offers a powerful toolset for law enforcement agencies to proactively address criminal activities. 
- As big data analytics and machine learning continue to evolve, it is essential to further explore and refine these methods to stay ahead in the fight against crime.
- The same work can be extended when ML based algorithms can be combined with computer vision and CCTV can be used to detect hotspot areas of crime and further prevent the occurrence of the same.









