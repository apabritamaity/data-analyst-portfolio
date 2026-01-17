## Dataset Description

The **IBM Telco Customer Churn dataset** contains customer-level information from a fictional telecommunications company. Each row represents a single customer, and each column describes an attribute related to the customer’s demographics, subscribed services, account details, billing information, and churn status.

The primary purpose of the dataset is to analyze customer behavior and identify factors that influence customer churn (i.e., customers who discontinue their service).

This dataset is widely used in the industry and academia for customer retention analysis, churn analytics, and business intelligence use cases.

<br/>

## Dataset Structure

The dataset can be broadly divided into **four categories**:



### 1. Customer Identification

These columns uniquely identify customers.

* `customerID` – Unique customer identifier

<br/>

### 2. Demographic Information

These attributes describe who the customer is.

* `gender` – Male or Female
* `SeniorCitizen` – Whether the customer is a senior citizen (0 = No, 1 = Yes)
* `Partner` – Whether the customer has a partner
* `Dependents` – Whether the customer has dependents

**Purpose:**
Used to analyze churn patterns across different customer demographics.

<br/>

### 3. Services Information (Core Business Services)

These columns describe **which telecom services the customer has subscribed to**.
This is the **most important section for business analysis**.

#### A. Phone Services

* `PhoneService` – Whether the customer has phone service
* `MultipleLines` – Whether the customer has multiple phone lines

<br/>

#### B. Internet Services

* `InternetService` – Type of internet service subscribed:

  * DSL
  * Fiber optic
  * No internet service

<br/>

#### C. Online & Security Services (Value-Added Services)

These services are typically offered as add-ons to internet service:

* `OnlineSecurity` – Online security service
* `OnlineBackup` – Online data backup
* `DeviceProtection` – Device protection plan
* `TechSupport` – Technical support service

<br/>

#### D. Streaming Services

Entertainment-related services:

* `StreamingTV` – Streaming television service
* `StreamingMovies` – Streaming movies service

<br/>

**Purpose:**
These service attributes help identify:

* Which services reduce churn (loyalty drivers)
* Which services are associated with higher churn
* Cross-sell and upsell opportunities

<br/>

### 4. Account & Billing Information

These columns describe **how long the customer has been with the company and how they are billed**.

* `tenure` – Number of months the customer has stayed with the company
* `Contract` – Contract type:

  * Month-to-month
  * One year
  * Two year
* `PaperlessBilling` – Whether the customer uses paperless billing
* `PaymentMethod` – Payment method used:

  * Electronic check
  * Mailed check
  * Bank transfer
  * Credit card
* `MonthlyCharges` – Monthly billing amount
* `TotalCharges` – Total amount charged to the customer

<br/>

**Purpose:**
Critical for analyzing:

* Early churn behavior
* Price sensitivity
* Contract-based retention

<br/>

### 5. Target Variable (Churn)

* `Churn` – Whether the customer left the company:

  * Yes → Customer churned
  * No → Customer retained

This is the **target variable** for churn analysis.

<br/>
