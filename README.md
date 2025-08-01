# Data Analytics Customer Segmentation

## Goal of the Project
The purpose of this project is to conduct a Customer Segmentation Analysis for an automobile bike company. Customer segmentation is performed using an RFM (Recency, Frequency, Monetary) model — a behavior-based approach that groups customers based on purchase behavior. In this analysis, customers are divided into 11 groups. The goal is to help identify high-value customers and optimize marketing strategies to boost revenue.

A **Sales Dashboard** is developed using **Tableau**, and data cleaning and analysis is performed in **Python**.

---

## Tableau Dashboard

The Sales Dashboard for Customer Segmentation can be found [here](https://public.tableau.com/profile/abhishek.chowdhury#!/vizhome/CustomerSegmentationDashboard_16175595616510/RFMDashboard).  
<img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Sales%20Dashboard.gif" height="500">

---

## Jupyter Notebooks (via nbviewer)

If GitHub doesn't render Jupyter notebooks properly, view them here:
- [RFM Analysis.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/RFM%20Analysis.ipynb)
- [DQA and Data Cleaning CustomerDemographic.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20CustomerDemographic.ipynb)
- [DQA and Data Cleaning NewCustomerList.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20NewCustomerList.ipynb)
- [DQA and Data Cleaning Transactions.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20Transactions.ipynb)
- [DQA and Data Cleaning Customer Address.ipynb](https://nbviewer.jupyter.org/github/AbhishekGit-hash/Data-Analytics-Customer-Segmentation/blob/master/DQA%20and%20Data%20Cleaning%20Customer%20Address.ipynb)

---

## Analysis Approach

### 1. Data Quality Assessment & Cleaning

Data was cleaned and assessed across the following datasets:

- **CustomerDemographics**
  - Removed irrelevant columns and handled missing values.
  - Standardized `gender` entries.
  - Derived `Age` and `Age Group` from `Date of Birth`.
  - Removed outliers and verified for duplicates.

- **NewCustomerList**
  - Dropped irrelevant columns and treated missing values.
  - Derived age-related columns and verified consistency.
  - No duplicate or inconsistent data found.

- **Transaction_data**
  - Converted `product_first_sold_date` to datetime.
  - Created new `Profit` column.
  - Missing values treated, no duplicates found.

- **CustomerAddress**
  - Standardized state names.
  - Found mismatch in customer ID between demographics and address tables.

---

### 2. Exploratory Data Analysis

#### Age Distribution

| Old Customers | New Customers |
|---------------|----------------|
| <img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Old%20Customers%20Age%20Distribution.PNG" height="400"> | <img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/New%20Customers%20Age%20Distribution.PNG" height="400"> |

- Most customers (old & new) are aged 40–49.
- Lowest numbers are in age groups under 20 and over 80.

#### Gender-wise Bike Purchases

<img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Female%20vs%20Male%20Bike%20Purchases.PNG" height="400">

- Females account for slightly more purchases (51%) than males (49%).

#### Job Industry Distribution

| Old Customers | New Customers |
|---------------|----------------|
| <img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Old%20Customers%20Job%20Industry.PNG" height="400"> | <img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/New%20Customers%20Job%20Industry.PNG" height="400"> |

- Manufacturing and Financial Services dominate.

#### Wealth Segmentation by Age

| Old Customers | New Customers |
|---------------|----------------|
| <img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Old%20Customers%20Wealth%20Segment.PNG" height="400"> | <img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/New%20Customer%20Wealth%20Segment.PNG" height="400"> |

- Most customers are from the **Mass Customer** segment.

#### Car Ownership by State

<img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Car%20Owners%20by%20State.PNG" height="400">

- NSW has the most customers without a car; QLD shows higher car ownership.

---

### 3. RFM Analysis & Customer Segmentation

RFM analysis grouped customers into the following 11 segments:
- Platinum Customers
- Very Loyal Customers
- Recent Customers
- Potential Customers
- Lost Customers
- Losing Customers
- Late Bloomers
- High-Risk Customers
- Evasive Customers
- Becoming Loyal
- Almost Lost Customers

<img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Customer%20Segment%20Distribution.PNG" height="400">

---

### 4. RFM Analysis: Scatter Plots

**Recency vs Monetary**  
<img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Recency%20vs%20Monetary.PNG" height="400">

**Frequency vs Monetary**  
<img src="Customer%20Segmentation%20(RFM)%20Analysis/data%20visualization/Frequency%20vs%20Monetary.PNG" height="400">

---

## Datasets Used

- `Raw_data.xlsx`, including:
  - `Transactions_data.xlsx`
  - `NewCustomerList.xlsx`
  - `CustomerDemographic.xlsx`
  - `CustomerAddress.xlsx`

---

## Tools & Technologies

- **Python** (pandas, seaborn, matplotlib) — for EDA, data cleaning, and RFM analysis
- **Tableau** — for building the customer segmentation dashboard

---

## Built With

- Python 3.8.2  
- Tableau Public

