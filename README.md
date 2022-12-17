# ML-Classification-Capstone-project
ML Classification Capstone project
## **EDA Conclusion**
* We found there are **95919** values are listed as **0**. Using some **google search** we found that **0**  meaning the **payment wasn't due**, which makes sense that most customers were using the revolving credit.
* Also we found **24415** values as **-2** which means **No consumption**.

* There are no **duplicate** IDs or rows.

* **30%** male have **default** payment while **26%** female have **defaul** payment, the difference is not significant.

* Also we can see **Female** have more **count** than **male**
* **'EDUCATION'** column: notice **5** and **6** are both recorded as **'unknown'** and there is 0 which isn't explained in the dataset description. 

* Since the amounts are so small, let's combine **0,4,5,6** to **0** which means**"other**'.

* **'MARRIAGE'** column: what does **0** mean in **'MARRIAGE'**? Since there are only  54 observations of 0, 

* we will combine **0** and **3** in one value as **'others'**.
* There was a huge jump from **May 2005**  to **July 2005** 

* when delayed payment increased significantly, then it peaked at **August 2005**.

* Things started to get better in **September, 2005** .

* Unsurprisingly, customers who had **higher credit** limits had **lower delayed** payment rates.
*  The minimals of those 6 bill columns are negative numbers. 

* In general, there are **590-688** bills with negative amounts each month, which is less than **2% **of total **30,000** records monthly.

* The common sense is that the bill statement amount shouldn't exceed credit limit.

*  However, there are **3931 customers** whose bill amounts are greater than credit limit. 

* Could the difference be late payment interest assuming these customers had **delayed payment**?

---

# **Conclusion:-**


### **Prepare for Modeling**

* we use **pairplots** for understanding the data.

* Also created **bins** for **AGE** columns.

* This dataset is also **imbalanced**, with **78%** non-default vs **22%** default.

* We use **SMOTE** because the class is highlly **Imbalance**

* There are **870 customers** whose bill amount was 0 in 6 months

* **317** **customers** had default payment next month which is against common sense

---




### **MODELS - 1**

* Using a **Logistic Regression** classifier, we can predict with **68.37%** accuracy, whether a customer is likely to default next month.

* Using **Decision Tree** classifier, we can predict with **73.83%** accuracy whether a customer is likely to default next month or not.

* Using **Random Fores**t, we can predict with **78.38%** accuracy whether a customer will be defaulter in next month or not.

* By applying **XGBoost Classifier** with recall **75%**, we can predict with 81.60% accuracy whether a customer is likely to default next month.
---
![image](https://user-images.githubusercontent.com/112492310/208240496-a7d5a09a-53c5-4f99-b770-3451ce5f6bce.png)
---
![image](https://user-images.githubusercontent.com/112492310/208240537-67056714-2c22-422d-935f-21dd59e3065c.png)

---
### **MODELS - 2**

* Rename default default payment next month to is defaulter
use smote because the data is imbalanced

* Create another feater named Payement_Value after adding all pay columns
* Create another feater Dues after adding all dues
* Replace 5,6,0 to 4 in education column
* Replace 0 with 3 in marrige column
* Using one hot encoding on Education, Marrige,column
* Using lavel encoding on  Sex column

* Using a **Logistic Regression** classifier, we can predict with **72%** accuracy, whether a customer is likely to default next month.

* Using **Decision Tree** classifier, we can predict with **83.83%** accuracy whether a customer is likely to default next month or not.

* Using **Random Fores**t, we can predict with **74.38%** accuracy whether a customer will be defaulter in next month or not.

* By applying **XGBoost Classifier** with recall **78%**, we can predict with 81.60% accuracy whether a customer is likely to default next month.
---
![image](https://user-images.githubusercontent.com/112492310/208240366-a01116f6-fe9f-46a9-a011-6b009b137146.png)
---

![image](https://user-images.githubusercontent.com/112492310/208240465-c2ccf98c-cbdb-418e-9f50-e75d7dc163f1.png)

---
### **Model Explaination**
![image](https://user-images.githubusercontent.com/112492310/208240574-4c4dd49b-43e8-4314-96eb-7508f933c196.png)
---
![image](https://user-images.githubusercontent.com/112492310/208240601-5ebaa969-eb13-4b47-ba3e-c83c8353340f.png)
---
* 'MARRIGE' is the most important features and pay_1 and SEX are also important.

* pay_amt4 is the least important feature.
