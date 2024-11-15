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

For senior citizens a significant difference can be observed. 1300/5300 *100 = **24.5% appx, non-senior citizen** are churned. 400/1000 *100 = **40% senior citizen** are churned appx.


![image](https://github.com/user-attachments/assets/26c8bdf7-ca04-4efd-b56e-a32946f532a8)


Its clear that those are not having partners are likely to churn, 1200/3600 * 100 = 33.3% appx.

![image](https://github.com/user-attachments/assets/43a51c2b-b5cd-427b-b334-6b09ef8ea140)


People with no dependants are churned much. 1500/3400 * 100% = 30.6% appx.


![image](https://github.com/user-attachments/assets/d64cfd3e-8383-4921-b2cb-29707736f060)



People **with no phone service churned by 200/700 * 100 = 28.5% appx**, and **with phone service are churned by 16/62 * 100 = 25.8% appx.**


![image](https://github.com/user-attachments/assets/34b4f22c-4ecb-4ab5-811b-6d37f757ef39)


Regarding the Internet service churn rate is high for **fiber optic user which is 250/2250 * 100 = 11.1% appx**.


 ![image](https://github.com/user-attachments/assets/a61d0dd3-d93e-4310-a26b-b8a7e12b4ea5)


**Montn to month contract** basis users are more churned among other contract tiers, which is **1650/3900 * 100 = 42.3% appx**


 ![image](https://github.com/user-attachments/assets/2765d245-57b8-4552-abf4-e3bfddeef3ce)


People with paperless billing are more churned with **1400/3950 * 100 = 35.44% appx**


![image](https://github.com/user-attachments/assets/b5fce90f-aece-49a7-b495-8bf2b70c6d04)

According to the payment method vs Churn analysis most users churned are with electronic payment method with **1050/2350 * 100 = 44.68% appx**


 ![image](https://github.com/user-attachments/assets/a8f59211-a5ba-427f-be54-83f01056e9a8)

 
1-12 months tenure group is most churned group of all with **1050/2200 * 100 = 47.72% appx**


**Bivariant Analysis**

Now for Bivariant Analysis feature encoding is required and for that there are multiple techniques , here Panda's get_dummies is used as One Hot Encoding Techniques.

For that Churn column has been converted to binary form. Also for finding correlation this is required.

![image](https://github.com/user-attachments/assets/b33f361f-21f7-446a-a249-5cdec2dac77d)


![image](https://github.com/user-attachments/assets/d8123d10-50ff-4946-94a0-a51a5c6756c0)


After the conversion, Correlation between monthly and Total charges are ploted.

![image](https://github.com/user-attachments/assets/65eb946b-41e8-4189-a24e-90998614c776)


![image](https://github.com/user-attachments/assets/db0f6910-c12b-4283-9280-3cdb9d3a87e8)

The correlation value is 0.65.
![image](https://github.com/user-attachments/assets/4cf5aa7e-5117-41b0-b61c-5fb908c26f19)



To understand the distribution of the Churned & Non-churned with Monthly charges KDE plot is used.

![image](https://github.com/user-attachments/assets/5d28d707-1620-4994-985a-24f2b00b99e4)

![image](https://github.com/user-attachments/assets/e0e54a96-95dc-4a65-806f-fe8cfcef78cd)

From the above plot its very clear that while monthly charges are increasing Churn is also high. It can be inferred that due to the monetary aspect the churns are high with high monthly charges.

Surprisingly while total charges are plotted different result came out.

![image](https://github.com/user-attachments/assets/da7f2f9b-8054-48b7-bc7a-fa1faf03b400)


![image](https://github.com/user-attachments/assets/e6b85981-4c7f-42a9-9ecf-137bd9aa923a)


Here even though monthly and total charges are highly correlated(>.6) still its observed that while Total charges are low churn is high and vice versa. It can be inferred that Tenure is a factor impacting the churn. **With less Tenure higher monthly charges is related to lower Total Charges and High churn.**

Now if we try to plot correlation with all the columns present in new data frame created by Dummy method we can find the factors which are or are not impacting the churn.

![image](https://github.com/user-attachments/assets/80598f84-1e17-4e4d-9a62-3856aabed794)

![image](https://github.com/user-attachments/assets/8c4fd755-9c79-4dfd-bc9f-10affe0168de)














 












