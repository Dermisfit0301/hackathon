# slackathon-for-simplilearn-Payment-Fraud-Detection
This repository has been created for a competition called a slackathon. We are given an imaginary business problem and we have to figure out a way to solve that problem.

I chose the topic of Payment Fraud Detection. I will be collecting data from various sources and would build an algorithm or you can say a layout to detect Payment frauds and block them. 

NOTE: This is just a model or a layout, not the real program with practical usage.

### **Contents**

1.[Project objective](#project-objective)

2.[Short description of the project](#short-description-of-the-project)

3.[What is the problem we are dealing with](#what-is-the-problem-we-are-dealing-with)

4.[How can technology help?](#how-can-technology-help)

5.[Why I chose this topic?](#why-I-chose-this-topic)

6.[Intro video](#intro-video)

7.[Long description](#long-description)

8.[The structure](#the-structure)

9.[Project roadmap](#project-roadmap)

10.[Acknowledgement](#Acknowledgement)


### **Project objective**

The objective here is to come up with an algorithm that detects a fraudulent transaction.

### **Short description of the project**
The fraudulent transactions are the one that are not made by the card owners but by scammers. The objective of the algorithm is to catch such transactions.
We are going to use past details of credit card transactions in order to see the patterns that leads to a fraudulent transaction. The patterns thus identified will help us form insights into the data and we will know which group of customers are more vulnerable and many more such facts. 

The identified patterns and insights will help us create a model which we will train through machine learning methods which will help us determine a fraudulent transactions. The trained machine will be implemented on the testing dataset which will help us know the effectiveness of the model.

### **What is the problem we are dealing with?**

Nowadays we live in a world that is now a global village. The era of technology has made the whole whorld a small digital village. You can get food, clothes and even a wife from the internet. There is a voluminous rise of internet commerce and hence transactions made online are increasing by the minute everyday. This has caught the eyes of the criminals who have gone online as well and are trying to get a piece of the pie. 
Fraudulent transactions are made by these criminals after they steal your credentials usually through fake apps, dating accounts etc. These are the transactions someone else makes and we end up paying for it. 
Fraudulent transctions not only harm the customer but also the company as they are the ones who face the music. They have to deploy manpower to track it and to handle customers which leads to loss of not only time and energy but also reputation. 

### **How can technology help?**

Technology can play a role in preventing such transactions by calling out such fraudulent transactions. Machine learning when deployed properly can take into account patterns that lead to a fraud transaction and notify the bank to cancel the transaction. ML can identify user spending habits, location, time of spending etc and can easily identify if the transaction was legitimate or not. 
The historical data of the users can be used to create a machine learning model and create an algortithm that can detect such frauds. The machine learning model will use classifier techniques to predict fraud transactions. Classifier techniques is to be used as they will tell whether a payment is fraud or not. 


### **Why I chose this topic?**

Machine Learning has a variety of applications and this application where I can use this to detect a fraudulent transaction seems intriguing as well as interesting. 
I think this topic needs to be addressed as I myself have been a victim of a fraudulent transaction and I had to pay for credit card transactions which I didnt make. This is a personal reason why I chose to do this topic. Now if I talk about the professional reason, I found this topic to be a playground for using Machine Learning techniques. You can use both supervised and unsupervised techniques for this topic either to draw insights or to create an algorithm. I can use clustering to create groups of customers who are more likely to face a fraud or use PCA to find important components affecting the transactions. The possibility is endless and I am bit to find out what it holds.

### **Intro video** 
https://youtu.be/xr1UDPmW_80


### **The working**
![image](https://user-images.githubusercontent.com/70942004/198704004-26d29f21-6eae-43e0-8951-dde1a0f5b1ec.png)

*This is just a  visual representation not a working diagram.*

1.The transaction details are generated by the bank and are stored in a repository.

2.Then the data cleaning takes place-useless columns removed. 

3.The data is then encoded and normalised and then sent for the next process.

4.In this process the data is passed through the algorithm.

5.The algorithm takes the data in groups of 20 as it is a prototype as of now.

6.The algorithm then decides whether the payment is fraud or genuine based on probability.

7.The 20 lines are returned and we see which payments are fraud and which one are not. 

![image](https://user-images.githubusercontent.com/70942004/201693234-8471cf1e-48f5-4576-bc40-81d312fb7521.png)


**Note:** This whole process as of now is manual and is in a very small scale. The model needs to be automated using skilled programmers. A full fledged program is not within the scope of the Hackathon. We are just giving a basic prototype for the purpose of submission. 




### **Long description**

Here I will summarize the whole process of creating my algorithm from scratch. I will cover every point in brief. 

**1.Dataset obtaining**

I had obtained the dataset from Kaggle. It had around 150000 transactions and was divided into two parts. I merged the two datasets into one and used the new dataset for analysis. I mounted the dataset in Google colaboratory as it was more convenient and easy to use than Jupyter Notebook which crashes. 

**2.Dataset description**

It had the following columns.

**trans_date_trans_time**: The date and time of the transaction.

**cc_num**: credit card number. 

**merchant**: Merchant who was getting paid.

**category**: In what area does that merchant deal.

**amt**: Amount of money in American Dollars. 

**first**: first name of the card holder.

**last**: last name of the card holder.

**gender**: Gender of the cardholder.Just male and female!

**street**:Street of card holder residence

**city**:city of card holder residence

**state**:state of card holder residence

**zip**:ZIP code of card holder residence

**lat**:latitude of card holder

**long**:longitude of card holder

**city_pop**:Population of the city

**job**:trade of the card holder

**dob**:Date of birth of the card holder

**trans_num**: Transaction ID

**unix_time**: Unix time which is the time calculated since 1970 to today.

**merch_lat**: latitude of the merchant

**merch_long**:longitude of the merchant

**is_fraud**: Whether the transaction is fraud(1) or not(0)




**3.Packages used**

Pandas used for data analysis and manipulation

Numpy for mathematical formulae and operations.

Seaborn for data visualization

Matplotlib will help us visualize the data.

Scipy for statistical functions.

Sklearn package will help us with Machine learning 

Ipywidgets for plotting.

Date time package is for date and time operations. 

Xgboost gives us their classifier.

**4.Data cleaning/organizing**

The unnecessary columns that have no relevance were removed in this section.
Also extremely high and low values were removed from the dataset.
These extreme values are called outliers. 
Outliers affect the machine learning procedure. 


**5.Feature engineering** 

Here I created new variables like Age using date of birth.
I split the trans date and time into two seperate columns like transaction date and transaction time. 
I created bins to categorize time of the incident and age groups. 
I removed the unnecessary columns that hamper analysis. 
These new columns created were added to the dataset.

**6.Exploratory data analysis** 

Summary statistics helped us get an idea about the data like the average age of the card holders, highest amount they spent etc. 
In this section we do hypothesis testing in the form of ANOVA (more than two vategories) and T-test(two categories). 
We did data visualization and did time series analysis and saw which time of day was fraud most likely to occur, so on and so forth. 

**7.Model building**

This is the main task of the whole exerice. The outliers have been removed and the data has been cleaned for usage. First we go for Principal Component Analysis to reduce the number of components so that the analysis is easier. The categorical variables are removed and only numerical variables are kept for analysis. 
After doing the PCA, I dropped the idea as 4 to 5 principal components have the same amount of weightage. If i cant reduce the dimensions to 2 components then the whole purpose stands defeated. 

Since the number of fraud cases are 13 in 10000 which is like looking for a needle in a haystack, this is an imbalanced dataset. We decided to subset the dataset where there would be equal number of fraud and genuine cases. Here the machine can clearly understand the difference between these two cases.

In this scenario we need to use classifier algorithms like decision trees, Random Forest classifier,XGB classifier, Logistic Regression etc. The dataset can not be used directly for analysis. Hence we first encode the variables using One hot encoder and then use scaler to convert them to a scale i.e. Normalize them. The dataset is then split into two parts Training and Testing. 80% data is used for training where the machine identifies the patterns and then we test it on 20% data where we see if the machine is able to identify fraud correctly or not. The dataset is using Features(x) which are the scaled variables and using it to predict the class(y) which is 0 or 1. 

We select the model with the highest F-score and AUC score. We select logistic regression as F-score is 1 and AUC score is 1. This means this model is the most accurate for use as a classifier algorithm. 

**8.Basic Algorithm**

A basic algorithm is made that accepts 20 entries in the form of an array. The algorithm then tells which transaction is a fraud and which one is not. The algorithm detects a fraud on the principle of probability. The array has two variables 0 and 1. If the probability value of 0 is higher than the payment is not a fraud or if 1 is higher than the payment is a fraud. 



### **Project roadmap**
![image](https://user-images.githubusercontent.com/70942004/198540840-f37aa793-a17e-45d9-8a0c-19187aebb978.png)
*Note:I am not a professional developer or a programmer. This is just a basic hackathon submission. Therefore i dont have any idea which application I would use for integration and further development of Fraudwatch. The basic algorithm is provided*  


### **Acknowledgement**

I would first of all like to thank IBM and simplilearn to provide me with this opportunity to learn. 

I would extend my thanks to Binu Midhun mam who has guided us newbies through the hackathon in a friendly and warm manner. 

Last but not the least i would thank the websites and platforms like youtube for providing me with guidance and reference. 



