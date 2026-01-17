# Assumptions and Limitations

This document outlines the key assumptions made during the analysis and the limitations associated with the dataset and methodology.

<br/>

## Assumptions

### 1. Data Accuracy
It is assumed that the dataset provided by IBM accurately represents customer behavior and that all recorded values (e.g., churn status, tenure, charges) are correct and reliable.

<br/>

### 2. Churn Definition
The analysis assumes that the `Churn` variable correctly captures whether a customer has discontinued service. Customers labeled as “No” are assumed to be active at the time of data collection.

<br/>

### 3. Snapshot in Time
The dataset is treated as a snapshot rather than a time-series dataset. Customer attributes are assumed to represent their most recent state prior to churn or retention.

<br/>

### 4. Independent Customer Behavior
Each customer record is assumed to be independent. Interactions or dependencies between customers (e.g., family plans or shared accounts) are not explicitly modeled.

<br/>

### 5. Service Usage Representation
The presence or absence of services (e.g., online security, streaming services) is assumed to reflect actual customer usage, not just subscription status.

<br/>

### 6. Billing and Charges
Monthly and total charges are assumed to be correctly calculated and consistently recorded across all customers.

<br/>

## Limitations

### 1. Limited Temporal Information
The dataset does not provide detailed time-series usage data, limiting the ability to analyze churn trends over time or detect early warning signals.

<br/>

### 2. No External Factors
External influences such as competitor pricing, promotions, economic conditions, or regional market dynamics are not included in the dataset.

<br/>

### 3. No Customer Feedback Data
The dataset does not contain customer satisfaction scores, complaints, or qualitative feedback, which could provide deeper insights into churn motivations.

<br/>

### 4. Service Quality Not Measured
While service subscriptions are included, actual service quality metrics (e.g., internet speed, downtime, support resolution time) are not available.

<br/>

### 5. Synthetic / Sample Nature of Data
The dataset is a sample dataset provided for analytical purposes and may not fully reflect the complexity or scale of real-world telecom customer data.

<br/>

### 6. Correlation vs Causation
The analysis identifies associations between customer attributes and churn but does not establish causal relationships.

