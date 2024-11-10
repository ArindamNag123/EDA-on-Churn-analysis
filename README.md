# EDA-on-Churn-analysis

- **Exploring & understanding data**

 ![image](https://github.com/user-attachments/assets/e6adc10e-78a8-4961-842e-8605655884cd)
 
*Columns*

 ![image](https://github.com/user-attachments/assets/6b53b430-3b9d-48f9-b2a9-9589f5bab02c)
 
Data Types of Columns

![image](https://github.com/user-attachments/assets/6f8a551d-7f45-467e-be03-e246bef9943a)

Primary analysis from the column description
- Senior Citizen is categorical data hence numerical analysis is not correct
- 75% of the people have a tenure of 55 months(years cant be a possible unit)
- Upper 25% of people pay more than 89.85$

Churn data

  ![image](https://github.com/user-attachments/assets/9e612359-f9cc-46c1-b476-15506a66bc4c)

  ![image](https://github.com/user-attachments/assets/506271b3-1d99-49db-b1f5-5fd1e7b93906)

  Observation: The churn rate is high, as per the market's standard benchmark. We need to analyze it further using other columns.

  ![image](https://github.com/user-attachments/assets/f303d096-52b4-4f09-9766-2896bbfd65e0)

 ![image](https://github.com/user-attachments/assets/1bc43430-8c4a-4655-bbae-14f41e85b9a2)

Observation: Apparently, there is no non-null value since all columns have 7043 records. Here, the Total Charges column should be numeric. It also needs to be converted to numeric to determine the non-null value.

![image](https://github.com/user-attachments/assets/c7a2482b-81f5-4be8-b5d2-48eb60544f81)

After converting Total Charges to numeric, there are 11 null values. Two steps to handle these values. 
1) Drop them cuz the percentage is too low 11/7043*100 % = 0.15%
2) Imputing with mean/median/backward filling/ forward filling

Here dropping the null values will not cause a major effect

![image](https://github.com/user-attachments/assets/7492afaf-7c4f-4cf0-81b2-29a533d3328c)

 **Feature Binning **

 Feature binning can be done for better insights, Tenure column is selected for the same.

 ![image](https://github.com/user-attachments/assets/6ffd30a6-d776-4685-bdc3-2802a2b10b6a)

 For now customer ID column is not required, hence its dropped.

 **Univariate Analysis**

 Based on Churn analysis has been done. All the categorical columns have been used for the analysis

![image](https://github.com/user-attachments/assets/e8d94216-8eff-481a-a457-040ccb0e34aa)

From gender, no significant analysis can be done regarding churn. For male Churn looks little more than female.

![image](https://github.com/user-attachments/assets/d67bc323-3ad1-49b3-9bd7-cb9be07f286e)

For senior citizens a significant difference can be observed. 1300/4500*100 = **28.88% non-senior citizen** are churned. 400/600*100 = **66.66% senior citizen** are churned.


![image](https://github.com/user-attachments/assets/26c8bdf7-ca04-4efd-b56e-a32946f532a8)


![image](https://github.com/user-attachments/assets/43a51c2b-b5cd-427b-b334-6b09ef8ea140)


![image](https://github.com/user-attachments/assets/d64cfd3e-8383-4921-b2cb-29707736f060)


 ![image](https://github.com/user-attachments/assets/a61d0dd3-d93e-4310-a26b-b8a7e12b4ea5)


 ![image](https://github.com/user-attachments/assets/2765d245-57b8-4552-abf4-e3bfddeef3ce)


 ![image](https://github.com/user-attachments/assets/a8f59211-a5ba-427f-be54-83f01056e9a8)


 












