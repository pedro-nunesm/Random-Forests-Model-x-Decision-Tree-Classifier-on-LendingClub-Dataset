# Random Forest Model vs Decision Tree Classifier on LendingClub Dataset

![](img/lending_club.jpg)

### Using two Machine Learning Models to predict whether potential debtors will repay their loan based on historical data.
### For this, I will the Decision Tree Classifier, that is as classification model and the Random Forest model, that uses the Emseble Learning technique to compare several small decision trees and chose the best decision.


## 1- Business Problem
Lending Club is America's largest lending marketplace, connecting borrowers with investors since 2007. This company usually shares the dataset of operations history between clients. this data contains several characteristics of the customers who took out a loan, and in the end it shows whether or not there was default ("not.fully.paid").

The main objective of the project is to see which Classification Machine lLearning model behaves best with this dataset, to identify which would make a better prediction of a possible default.
The dataset has information about:

**Credit Policy, Purpose of the loan, Loan Interest Rate, Installment, FICO score, Public Rec, Not Fully Paid and others.**

The complete list is below: 
* credit.policy, int.rate, installment, log.annual.inc, dti, fico, days.with.cr.line, revol.bal, revol.util, inq.last.6mths, delinq.2yrs, pub.rec

## 2 - Tools
- Python
- LendingClub Dataset (2007 - 2010)

## 3- Solution (Step by step)
 **Step I** - Import Libraries;
 
 **Step II** - Load dataset (provided by ASIMOV ACADEMY);
 
 **Step III** - Analyze how the data is distributed;
 
 **Step IV** - Find correlation between the variables .
 
 **Step V** - Implement the Decision Tree Classifier and analyze the Classification Report and Consufion Matrix
 
 **Step VI** - Implement the Random Forest and analyze the Classification Report and Consufion Matrix;
 
 **Step VII** - Compare the two models and see which performed better;
 
 **Step VIII** - Make a conclusion.


## 4- Insights

### **4.1 - Analyzing Data**
- First of all, i used matplotlib to plot a graph and analyze how the defaulted transactions are split between trading purposes.
- Not Fully Paid = 0 (Paid Transactions) and  Not Fully Paid = 1 (Defaulted Transactions)
![](img/countbypurpose.png)
![](img/percentbypurpose.png)
- Its clear that the amount of Defaulted Transactions is much smaller than the amount of Paid Transactions, and most Paid Transactions are in purpose Debt Consolidation.,

- After this, i created a histrogram to analyze the  amount of data and correlation between FICO score and Credit Policy
  ![](img/ficoxcreditpolicy.png)


- Than, i did the same, but using Not Fully Paid Parameter

![](img/ficoxnotfullypaid.png)

- Apparently, the FICO score is not a good indicator to know if the person will be a defaulter or not, because the behavior of the data has a similar format.
 
- After this, i tried to find a correlation between Int.Rate and FICO
![](img/intratexfico.png)

![](img/implottendence.png)

- It is possible to check that the higher the FICO score, the lower the rates, something that makes sense, as these people represent a lower risk of default.
- Apparently, both for defaulters and for those who paid, the behavior of the data is not different analyzing only this aspect

### **4.2 - Get_Dummies**
- **Before implementing the models, i needed to convert the "Purpose" column of the Dataframe to binary form, creating new columns using "get_dummies" function.**
- **This was necessary as it would be difficult for the classification model to work with variables in this multi-string format.**

### **4.3 Decision Tree Classifier**
 - To begin, i separate dataset between X (Numeric Variables) and Y(Year Amount Spent)
 - So i used Sklearn to create X_train, X_test, Y_train, Y_test
 - The objective was to use the Trainning Dataset to train the Linear Regression Model, then, use the Test Dataset to measure the performance.

Then, I implemented Decision Tree Classifier model and got the following Confusion Matrix and Classification Report:
- 




### **4.4 - Random Forest**

### **4.5 - Checking the Coefficients**


## 5- Conclusion


## 6- Next-Steps

**Despite knowing that the project can still be improved a lot, I consider it finished.**


