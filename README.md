# StirBank Customer Targeting Predictor :bank::dart:
This project applies machine learning techniques :robot: to predict the probability of a customer setting up a regular savings deposit :moneybag: after receiving a marketing call from StirBank. The goal is to streamline marketing strategies, minimize costs, and enhance customer experience by targeting those most likely to respond positively. The model is trained on data from 8000 customers, including their reactions to past marketing attempts.

# :bookmark_tabs: Table of Contents
1. Project Overview
2. Features Description
3. Installation & Usage
4. Methodology
   4.1 Business Understanding
   4.2 Data Summary
   4.3 Data Preparation
   4.4 Modelling
   4.5 Evaluation

# :dart: Project Overview <a name="project-overview"></a>
This project involves predicting customer behavior using data mining techniques. The task is to determine if a customer is likely to set up a savings deposit after a marketing call. The classification problem is addressed using machine learning models.

# :memo: Features Description <a name="features-description"></a>
The dataset consists of the following features:

- accountID: unique identifier for customer
- town: home town for customer
- country: country for customer's home address
- age: customer's age
- job: customer's job
- married: customer's marital status
- education: customer's highest educational qualification level obtained
- defaulted?: has the customer credit in default (i.e., failed to repay)?
- current_balance: current amount in the customer's account in pounds
- housing: has the customer a housing loan / mortgage?
- has_loan: has the customer got an unsecured personal loan?
- last_contact: type of communication used for previous call to the customer
- cc_tr: credit card tracking ID (meaning is confidential)
- last_contact_month: last contact month of the year
- last_contact_day: last contact day of the month
- campaign: number of contacts performed during this campaign and for this client
- days_since_last_contact: number of days that passed by after the client was last contacted from a previous campaign
- previous: number of contacts performed before this campaign and for this client
- poutcome: outcome of the previous marketing campaign
- made_deposit: has the client subscribed a term deposit? [target variable]

# :gear: Installation & Usage <a name="installation-usage"></a>
The project requires Python :snake: and the following libraries installed:
- Numpy
- Pandas
- Scikit-Learn
- Matplotlib
- Seaborn
- keras
- tensorflow
To run the project, download the repository and run the .ipynb file using a Python-enabled IDE or terminal.

# :chart_with_upwards_trend: Methodology <a name="methodology"></a>
The project follows the CRISP-DM framework.

# Business Understanding <a name="business-understanding"></a>
The task at hand is a classification problem, where we aim to predict whether a customer will respond positively to a marketing call and make a regular savings deposit. Given the nature of the problem and the provided data, machine learning (specifically supervised learning) is a suitable method for this task.

# Data Summary <a name="data-summary"></a>
The dataset contains a variety of information about the customers, such as demographics (age, job, marital status), financial standing (current balance, default status), and interaction with the bank (last contact, previous marketing campaign outcome). These variables will be treated as categorical or numeric based on their nature and analyzed to understand their impact on the target variable 'made_deposit'.

# Data Preparation <a name="data-preparation"></a>
The data was pre-processed before feeding it into the models. This process involved cleaning data entries, handling missing data, and encoding categorical variables. Histograms were plotted to visualize the distribution of data before and after the pre-processing steps.

# Modelling <a name="modelling"></a>
Three different machine learning techniques were used - a tree-based model, a logistic regression model, and a neural network model. The hyperparameters of these models were tuned to achieve optimal performance. The data was split into training, validation, and testing sets for robust evaluation.

# Evaluation <a name="evaluation"></a>
The models' performance was evaluated based on their accuracy, and the errors made were analyzed using confusion matrices. Further, ROC curves were plotted to understand the trade-off between the sensitivity (true positive rate) and specificity (false positive rate) for the models. This helped in understanding how the models performed across different thresholds and where they made the most mistakes. The models' results were compared, and the one yielding the best performance was selected for final testing.