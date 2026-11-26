# Customer Master EDA

Exploratory data analysis of **25,000 e-commerce customers** using Python (Pandas, Matplotlib, Seaborn) to understand customer segments, geography, demographics and customer acquisition cost.

## Project Overview

This project explores a customer master dataset to answer practical business questions: where are the customers, which segments do they belong to, who are they (age and gender), and how much does it cost to acquire them in different countries, regions and segments. The analysis also checks the data for duplicates and format problems before drawing conclusions.

## Dataset

- **Source:** [E-Commerce Sales and Customer Analytics (Kaggle)](https://www.kaggle.com/datasets/datascikhan/e-commerce-sales-and-customer-analytics/data)
- **File used:** `customer_master.csv`
- **Size:** 25,000 rows x 11 columns, with no missing values

| Column | Description |
|---|---|
| customer_id | Unique customer ID |
| customer_name | Customer name |
| customer_age | Customer age (18 to 74) |
| gender | Female, Male or Non-Binary |
| customer_segment | Consumer, Premium, VIP or Business |
| customer_city | City |
| customer_state | State or province |
| customer_country | USA, UK, Germany, Canada, Australia, India or UAE |
| region | Central, East, North, South or West |
| customer_postal_code | Postal code |
| customer_acquisition_cost | Cost of acquiring the customer |

## Tools and Libraries

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## Analysis Performed

1. Age and acquisition cost distribution
2. Customer distribution by gender and segment
3. Data integrity and duplicate check
4. Customer summary by country (count, average age, average acquisition cost)
5. Average acquisition cost by country
6. Gender distribution across customer segments
7. Acquisition cost matrix: region by segment (heatmap)
8. Postal code length audit
9. Customer footprint across countries and regions
10. Proportion of VIP customers by country

Each section of the notebook ends with a written conclusion.

## Key Findings

| Area | Finding |
|---|---|
| Data quality | No missing values, unique `customer_id`, 0 duplicate rows. 3,369 repeated names belong to different customers, not duplicates. |
| Geography | The USA holds 59.7% of customers (14,925), followed by the UK (14.8%) and Germany (8.2%). South is the largest region (32.0%) and North the smallest (12.1%). |
| Segments | Consumer is the largest segment (54.6%), then Premium (25.2%), VIP (10.2%) and Business (10.1%). |
| Demographics | Female 48.2%, Male 47.9%, Non-Binary 3.9%. Average age is about 46 in every country, and the gender mix is nearly the same in every segment. |
| Acquisition cost | Average cost is about 42 and stays between 40 and 43 across countries, regions and segments. Individual costs vary widely (5.01 to 79.99). |
| VIP customers | 59.4% of VIP customers are in the USA, which matches the overall country mix. |
| Postal codes | 90.5% have 5 digits, 9.0% have 4 and 0.5% have 3. Short codes likely lost their leading zeros. |

## Recommendations

- Plan marketing budgets by market size, since acquisition cost is nearly the same everywhere.
- Grow the smaller markets (Canada, Australia, India, UAE) and the North region.
- Build a path from Premium to VIP, since VIP is only about 10% of customers.
- Store postal codes as text and pad them to 5 digits.

## Limitations

- The dataset has no purchase, revenue or churn data, so the value of each segment cannot be judged.
- The `region` column does not follow geography (for example, Germany appears in four regions), so it should be read as a business or sales region.
- Averages hide a wide spread in individual acquisition cost.
- Results show relationships, not causes.

## Project Structure

```
├── ecommerce_eda.ipynb                              # Jupyter notebook with the full analysis
├── customer_master.csv                              # Customer master dataset
├── Customer_Master_EDA_-_Overall_Conclusion.pdf     # Report with overall conclusion
├── Data Source.txt                                  # Kaggle dataset link
└── README.md
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/akashrathore14/customer-master-eda.git
   cd customer-master-eda
   ```
2. Install the required libraries:
   ```bash
   pip install pandas matplotlib seaborn jupyter
   ```
3. Open the notebook:
   ```bash
   jupyter notebook ecommerce_eda.ipynb
   ```
4. Make sure `customer_master.csv` is in the same folder as the notebook, then run all cells.

## Report

The full summary of findings, insights, recommendations and limitations is in [`Customer_Master_EDA_-_Overall_Conclusion.pdf`](Customer_Master_EDA_-_Overall_Conclusion.pdf).

## Author

**Akash Rathore**
[GitHub](https://github.com/akashrathore14) | [LinkedIn](https://www.linkedin.com/in/akash-rathore-945459148)
