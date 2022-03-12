# Loan Status Prediction

### Introduction
According to Canadian Anti Fraud Centre, Loan Fraud was among top 10 frauds in 2021, in which 570 cases were registered and there were 434 victims who lost total of $6.9 million dollars.

The problems we're solving here is:
- How risky is the brrower?
- Given the borrower's risk, should we lend him/her

### Objective
The goal of this project is to automate the loan eligibilty process to predict whether a loan would be approve or not.

#### Explore the problem in following stages:
1. Hypothesis Generation – understanding the problem better by brainstorming possible factors that can impact the outcome
2. Data Exploration – looking at categorical and continuous feature summaries and making inferences about the data.
3. Data Cleaning – imputing missing values in the data and checking for outliers
4. Feature Engineering – modifying existing variables and creating new ones for analysis
5. Model Building – making predictive models on the data

## 1. Hypothesis Generation

Generating a hypothesis is a major step in the process of analyzing data. This involves understanding the problem and formulating a meaningful hypothesis about what could potentially have a good impact on the outcome. This is done BEFORE looking at the data, and we end up creating a laundry list of the different analyses which we can potentially perform if data is available.

#### Possible hypotheses
Which applicants are more likely to get a loan

1. Applicants having a credit history 
2. Applicants with higher applicant and co-applicant incomes
3. Applicants with higher education level
4. Properties in urban areas with high growth perspectives

Do more brainstorming and create some hypotheses of your own. Remember that the data might not be sufficient to test all of these, but forming these enables a better understanding of the problem.

## 2. Data Exploration
Let's do some basic data exploration here and come up with some inferences about the data. Go ahead and try to figure out some irregularities and address them in the next section. 

### Distribution analysis
Study distribution of various variables. Plot the histogram of ApplicantIncome, try different number of bins.

### Categorical variable analysis
Try to understand categorical variables in more details using `pandas.DataFrame.pivot_table` and some visualizations.

## 3. Data Cleaning

This step typically involves imputing missing values and treating outliers. 

### Extreme values
Try a log transformation to get rid of the extreme values in `LoanAmount`. Plot the histogram before and after the transformation

## 4. Building a Predictive Model
Logistic Regression Model
Accuracy : 80.945%
Cross-Validation Score : 80.946%

### Build Pipelines

## 5. Using Pipeline
If you didn't use pipelines before, transform your data prep, feat. engineering and modeling steps into Pipeline. It will be helpful for deployment.

The goal here is to create the pipeline that will take one row of our dataset and predict the probability of being granted a loan.

`pipeline.predict(x)`

## 6. Deploy model to cloud and test it with PostMan, BASH or Python

### Conclusion
Now, coming to the scope of improvements and modifications, We can improve the accuracy score, by doing some of the following, though it is not guaranteed, that the results will change for the better.

1)Taking a bigger dataset with versatile and large training data. But keep in mind while taking a large dataset, the bigger the dataset, the more processing time will the execution take.

2) Checking for various algorithms. There is no such convention, that we must use a specific algorithm, for a specific problem set. We chose the algorithm based on the type of dataset. You might even have to opt for the method of “trial & error”.

The practicality of this Project
Now let us refer to the elephant in the room. Is the above code ready to be deployed in the banking systems?

A straightforward answer will be NO.

The reasons are:

- I have used an extremely small dataset. Thus the training dataset is not enough for the model to predict for the various kinds of people that dwell on this earth, with various backgrounds.

-  Real-life scenarios are quite different than what we discuss in theory. There arise many exceptions, that need to be dealt with, and even, the decision-making supremacy, whether a person can be sanctioned a loan or not, cannot be given to a machine that predicts on the basis of these few lines of codes. Humans do have to intervene in those exceptional cases.

But does this mean, all that we did was a sheer waste?

Well, No again. We can use this concept to act as a parallel decision-making feature in the banks, that might be used to second the decisions of the bank people. But it must not be used solely, without the intervention of humans.


