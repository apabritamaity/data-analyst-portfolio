## Customer Segmentation Methodology
Customer segmentation is performed based on key demographic, service, etc usage attributes to identify distinct groups with varying churn behaviors.

### 1. Tenure (Lifecycle Segmentation):
| Segment    | Rule                | Description         |
| ---------- | ------------------- | ------------------- |
| new    |  0 ≤ x<=6            | high risky as they are still evaluating the service |
| midterm | x<=24               | moderate risk as they have some experience with the service |
| longterm | 24+       | low risk as they have established loyalty to the service.|

<br/>

### 2. Contract Type (Categorical Segmentation)

* Month-to-Month
* One-Year
* Two-Year 

<br/>

### 3. Internet Service Type (Product Segmentation)

* Fiber optic
* DSL
* No internet service

<br/>

### 4. Number of Services (Engagement Segmentation)

* 0–1 services → Low engagement
* 2–3 services → Medium engagement
* 4+ services → High engagement

<br/>

### 5. Total Charges (Value-Based Segmentation)

* Low: Bottom 25%
* Medium: Middle 50%
* High: Top 25%

<br/>

## Rule for Segmentation of Customers
### Customer segment rule based on service provides:
| Filter     | Rule                |
| ---------- | ------------------- |
| Churn rate |  ≤ 15–20%           |
| Customers  | ≥ 100               |
| Complexity | ≤ 3 services        |