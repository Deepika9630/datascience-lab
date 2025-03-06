AIM
To apply row and column indexing using .loc and .iloc methods in Pandas to filter specific data from a dataset based on given conditions.

Explanation

In this activity, we use Pandas, a Python library for data manipulation, to filter rows and select specific columns from a dataset containing information about bank clients.
We use the .loc method to apply conditional filtering based on column values. Some key filtering operations include:

-- Selecting clients based on education level and deposit subscription status
-- Filtering clients based on loans, previous marketing outcomes, and employment status
-- Extracting specific columns like name and salary (balance) for clients under a certain age


Algorithm

Step 1: Load the dataset using Pandas.  
Step 2:  Inspect the dataset by checking the first few rows and column names.  
Step 3:  Apply filtering conditions using the .loc method:  
   - Select rows where clients with primary education have subscribed to a deposit.  
   - Select rows where clients have not subscribed to a deposit.  
   - Select rows where subscribed clients have a housing or personal loan.  
   - Select rows where secondary-educated clients have not subscribed to a deposit.  
   - Select rows where clients subscribed due to a successful marketing campaign.  
   - Select rows where unemployed clients have not subscribed to a deposit.  
   - Select columns 'age' and 'balance' where age is less than or equal to 30.  
Step 4:  Display the filtered results.  
Step 5:  Save or export the filtered data if needed.

Coding and Output
ACTIVITY 1
1. Write a Python program to select the 'name' and 'score' columns from the following DataFrame.
exam_data = {'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
'attempts': [1, 3, 4, 3, 5, 3, 6, 1, 7, 1] } 
2. For the above dataframe, Write a program to select the data who's attempt is greater than 3.
3. Write python code for indexing rows and columns based on the following conditions:
data = {'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
'age': [25, 35, 40, 28],
'gender': ['F', 'M', 'M', 'M'],
'salary': [50000, 70000, 60000, 80000]}
a. Select rows where age is greater than 30:
b. Select rows where name contains 'e':
c. Select rows where gender is 'M' and salary is greater than 65000:
d. Select columns 'name' and 'age'
![image](https://github.com/user-attachments/assets/4318b549-5d39-4381-9ee2-48a19fe2b8bc)
![image](https://github.com/user-attachments/assets/6ea71b78-1e8d-481d-84f6-ad16fe4bb541)
![image](https://github.com/user-attachments/assets/143c332a-27f0-4fbf-a7e9-ecfd98a2ca60)
![image](https://github.com/user-attachments/assets/8344a92d-c088-4265-b92b-fbc1859c0257)





ACTIVITY 2
 a. Select the rows where clients with primary education have subscribed to a deposit
primary_education_deposit = df.loc[(df['education'] == 'primary') & (df['deposit'] == 'yes')]
print("Clients with primary education who subscribed to a deposit:\n", primary_education_deposit)

 b. Select the rows where clients who have not subscribed to a deposit
not_subscribed_deposit = df.loc[df['deposit'] == 'no']
print("\nClients who have not subscribed to a deposit:\n", not_subscribed_deposit)

 c. Select the rows where clients who have subscribed to a deposit either have a housing or a personal loan
deposit_with_loans = df.loc[(df['deposit'] == 'yes') & ((df['housing'] == 'yes') | (df['personal'] == 'yes'))]
print("\nClients who subscribed to a deposit with either housing or personal loan:\n", deposit_with_loans)

d. Select the rows where a. Select the rows where clients with primary education have subscribed to a depositclients with secondary education who have not subscribed to a deposit
secondary_no_deposit = df.loc[(df['education'] == 'secondary') & (df['deposit'] == 'no')]
print("\nClients with secondary education who have not subscribed to a deposit:\n", secondary_no_deposit)

e. Select the rows where clients who have subscribed to a term deposit as an outcome of the successful marketing campaign
successful_campaign_deposit = df.loc[(df['deposit'] == 'yes') & (df['campaign_outcome'] == 'success')]
print("\nClients who subscribed to a deposit after a successful marketing campaign:\n", successful_campaign_deposit)

 f. Select the rows where unemployed clients who have not subscribed to a deposit
unemployed_no_deposit = df.loc[(df['job'] == 'unemployed') & (df['deposit'] == 'no')]
print("\nUnemployed clients who have not subscribed to a deposit:\n", unemployed_no_deposit)

 g. Select columns 'name' and 'salary' where age is less than or equal to 30
name_salary_age_30 = df.loc[df['age'] <= 30, ['name', 'salary']]
print("\nClients with name and salary where age is less than or equal to 30:\n", name_salary_age_30)
![Screenshot (65)](https://github.com/user-attachments/assets/08524e5f-764c-488d-b7d2-23cb9fd96927)
![Screenshot (66)](https://github.com/user-attachments/assets/93a44db8-9c53-4c6b-a23e-50111718a1b5)




