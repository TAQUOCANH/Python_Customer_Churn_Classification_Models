# Python_Customer_Churn_Classification_Models
Check out the code file attached or view it at the given link:
<a href="https://colab.research.google.com/drive/19rlf50wUC1bZb3fX7ZOfNWdBfEHmuU4D">Click here</a>

## I. Introduction
### 1. Business Question
<p>An ecommerce firm is initiating a project aimed at predicting user attrition and planning to implement targeted promotions accordingly. The accompanying dataset provided by the company (<code>churn_predict.csv</code>) will be employed to address the following questions:</p>
<ul>
        <li>Identify patterns and behaviors of users who churn and suggest strategies for the company to mitigate user churn.</li>
        <li>Develop a Machine Learning model capable of predicting which users are likely to churn.</li>
</ul>

### 2. Dataset

<table>
        <tr>
            <th>Variable</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>CustomerID</td>
            <td>Unique customer ID</td>
        </tr>
        <tr>
            <td>Churn</td>
            <td>Churn Flag</td>
        </tr>
        <tr>
            <td>Tenure</td>
            <td>Tenure of customer in organization</td>
        </tr>
        <tr>
            <td>PreferredLoginDevice</td>
            <td>Preferred login device of customer</td>
        </tr>
        <tr>
            <td>CityTier</td>
            <td>City tier</td>
        </tr>
        <tr>
            <td>WarehouseToHome</td>
            <td>Distance between warehouse to home of customer</td>
        </tr>
        <tr>
            <td>PreferredPaymentMode</td>
            <td>Preferred payment method of customer</td>
        </tr>
        <tr>
            <td>Gender</td>
            <td>Gender of customer</td>
        </tr>
        <tr>
            <td>HourSpendOnApp</td>
            <td>Number of hours spent on mobile application or website</td>
        </tr>
        <tr>
            <td>NumberOfDeviceRegistered</td>
            <td>Total number of devices registered by a particular customer</td>
        </tr>
        <tr>
            <td>PreferedOrderCat</td>
            <td>Preferred order category of customer in the last month</td>
        </tr>
        <tr>
            <td>SatisfactionScore</td>
            <td>Satisfactory score of customer on service</td>
        </tr>
        <tr>
            <td>MaritalStatus</td>
            <td>Marital status of customer</td>
        </tr>
        <tr>
            <td>NumberOfAddress</td>
            <td>Total number of addresses added by a particular customer</td>
        </tr>
        <tr>
            <td>Complain</td>
            <td>Any complaint has been raised in the last month</td>
        </tr>
        <tr>
            <td>OrderAmountHikeFromLastYear</td>
            <td>Percentage increase in order amount from last year</td>
        </tr>
        <tr>
            <td>CouponUsed</td>
            <td>Total number of coupons that have been used in the last month</td>
        </tr>
        <tr>
            <td>OrderCount</td>
            <td>Total number of orders that have been placed in the last month</td>
        </tr>
        <tr>
            <td>DaySinceLastOrder</td>
            <td>Number of days since the last order by the customer</td>
        </tr>
        <tr>
            <td>CashbackAmount</td>
            <td>Average cashback received in the last month</td>
        </tr>
</table>

<img width="382" alt="Screenshot_6" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/8a786f2c-43a2-4528-8233-51f085e14348">

## II. Process
### 1. Data Handling and Cleaning
<ul>
        <li>Filling NaN values in the dataset using 0 for 'Tenure', 'CouponUsed', 'OrderCount' and median or mean values for other columns.
</li>
        <li>Remove those duplicate values</li>
        <li>Define type of data</li>
        <li>Feature Engineering and Scaling of the data</li>
</ul>

### 2. Important Features Influencing Model

<img width="800" alt="" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/d6ef24d4-4051-464d-8e1e-2ceb4fcf4a83">

Features selection
<ul>
        <li>Tenure</li>
        <li>DaySinceLastOrder</li>
        <li>CashbackAmount</li>
        <li>NumberOfAddress</li>
        <li>Complain</li>
        <li>WarehouseToHome</li>
</ul>

### 3. EDA
#### a. Tenure

<img width="800" alt="" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/3fd2dde8-b9c9-4754-8920-2afdec228df3">
<p>Churned users usually are new users → Provide more promotion for new users, or increase the new users experience </p>

#### b. Complain

<img width="800" alt="" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/e843cd6b-893c-4794-bb1d-ed8c0900f3c0">
<p>Churned users complain more → deep dive what these churned users complain about, and provide the solution  </p>

#### c. CashbackAmount

<img width="800" alt="" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/0d2b081a-5d0d-4c29-8072-c8714bee3822">
<p>Churned users usually receive less cashback than not churn → Increase the cashback ratio  </p>

#### d. WarehouseToHome

<img width="800" alt="" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/4fef624e-e406-46e3-bf29-e67083f96ea3">
<p>Shorter warehouse to home distances have a lower churn rate. Faster deliveries may improve satisfaction</p>

## III. Find the Best Model

<img width="800" alt="" src="https://github.com/TAQUOCANH/Python_Customer_Churn_Classification_Models/assets/135592751/d4f206bd-afd7-47be-bd87-0d07a507f691">


## IV. Conclusion

 **Best Model: RandomForestClassifier**

- **Reason**: It has the highest accuracy, precision, recall, and F1-score. Despite the higher training time, it provides the best overall performance.

**Alternative Model: KNeighborsClassifier**

- **Reason**: If training time and computational efficiency are critical, this model offers very good performance with minimal training time.

