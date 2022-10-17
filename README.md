# Improving Bank Marketing Campaigns with Machine Learning

### Project Status: Completed
  
### Project Objective
This project aims optimize the efforts of a Portuguese banking institutions direct marketing campaigns by predicting customer likelihood to subscribe to a term deposit. Such a solution has the potential to significantly reduce the labor cost of such a campaign.

### Partner(s)/Contributor(s)  
•	Hunter Blum - hunterblum
•	Jaqueline Urenda - jackieure
•	Gary Bair - garybair

### Methods Used
•	Data Mining 
•	Predictive Modeling 
•	Machine Learning
•	Data Visualization

### Technologies
•	Python

### Project Description

Term deposits are pivotal to the success of a bank and the overall economy. In these deposits, a customer lends cash to a bank for a set term in return for a small amount of interest. In return, the bank has the liquid assets it needs to give out larger and higher-interest loans, allowing the bank to profit (Kagan, 2020). Because of their importance, banks have been running more direct marketing campaigns in hopes of increasing their cash flow. However, because most customers do not want a term deposit or respond to telemarketing, these direct marketing campaigns that lack clear strategies, waste money, and frustrate uninterested customers (Moro et al., 2014). 

It is in this space that data mining presents a unique opportunity to optimize the organization's efforts when contacting individuals to subscribe to a term deposit and effectively reduce the prevalence of unproductive contacts, reducing labor costs and increasing profits from more successful calls. This analysis aims to validate a variety of industry-leading machine-learning algorithms to determine whether the bank's term deposit subscriptions can be effectively modeled using historical client, contact, and behavioral data.

### Dataset Description

The data for this study was collected by Moro et al. (2014), from a Portuguese retail bank direct marketing campaign spanning from 2008 to 2010. The original authors utilized a two-step feature selection, first having domain experts select relevant features, then employing a forward-feeding model to calculate which relevant features increased AUC (Moro et al., 2014). This feature-selected dataset was donated to the UCI Machine Learning Repository, containing 21 features and 41,188 observations. Our target feature was a binary variable describing if a client set up a term deposit. The predictors included demographic variables (age, job, etc.), banking information (credit defaults, loans, etc.), and other various indicators. 

### *Input variables*:
1. age: Customer Age (numeric)
2. job : Type of Job (categorical)
3. marital : Marital Status (categorical)
4. education: Level of Education (categorical)
5. default: Has credit in default? (categorical)
6. housing: Has housing loan? (categorical)
7. loan: Has personal loan? (categorical)
8. contact: Contact Communication Type (categorical)
9. month: Last Contact Month of Year (categorical)
10. day_of_week: Last Contact Day of the Week (categorical)
11. duration: Last Contact Duration, in seconds (numeric). 
12. campaign: Number of contacts performed during this campaign and for this client which includes last contact(numeric)
13. pdays: Number of days that passed by after the client was last contacted from a previous campaign (numeric)
14. previous: Number of contacts performed before this campaign and for this client (numeric)
15. poutcome: Outcome of previous marketing campaign contacts (categorical)
16. emp.var.rate: Employment Variation Rate - quarterly indicator (numeric)
17. cons.price.idx: Consumer Price Index - monthly indicator (numeric)
18. cons.conf.idx: Consumer Confidence Index - monthly indicator (numeric)
19. euribor3m: Euribor 3 Month Rate - daily indicator (numeric)
20. nr.employed: Number of Employees - quarterly indicator (numeric)

### *Output Variable*:
21. y - has the client subscribed a term deposit? (binary)

There are two significant things to note from the description of the data.
- The duration feature is highly affected by the output target (e.g., if duration=0 then y='no') therefore this feature should be discarded if the intention is to produce a realistic predictive model.
- For the feature pdays, 999 means client was not previously contacted which depending on the model implemented may affect the implementation of this analysis’s preprocessing.

