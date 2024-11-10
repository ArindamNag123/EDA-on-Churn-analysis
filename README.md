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

****Feature Binning****






 






