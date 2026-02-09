# Exploratory Data Analysis: Online Retail Transaction

## Project Overview
This project performs an **Exploratory Data Analysis (EDA)** on a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

The goal of this analysis is to uncover sales patterns, identify high-value products, and evaluate regional performance to provide actionable business recommendations.

## Business Questions
We aim to answer the following strategic questions:
1.  **Product Performance:** Which products generate the highest sales volume vs. the highest revenue?
2.  **Seasonal Trends:** What are the monthly sales trends? Are there specific seasonal patterns that require inventory planning?
3.  **Regional Analysis:** Which regions are underperforming and require strategic review?

## Dataset Description
The dataset consists of transactional data with the following features:
* `InvoiceNo`: Transaction ID.
* `StockCode`: Product code.
* `Description`: Product name.
* `Quantity`: The quantities of each product per transaction.
* `InvoiceDate`: The day and time when each transaction was generated.
* `UnitPrice`: Product price per unit (Sterling).
* `CustomerID`: Unique customer number.
* `Country`: The name of the country where each customer resides.

## Analysis Workflow
This project follows a structured data analysis framework:

1.  **Data Wrangling**:
    * Handling missing values (CustomerID).
    * Cleaning negative values in `Quantity` (Cancellations/Returns).
    * Correcting data types (`InvoiceDate`).
2.  **Feature Engineering**:
    * Creating `Total_Revenue` column (`Quantity` * `UnitPrice`).
    * Extracting `Month_Year` and `Year` for time-series analysis.
    * Segmenting data into **Retail** vs **Wholesale** categories (based on Quantity thresholds).
3.  **Exploratory Data Analysis (EDA)**:
    * Univariate Analysis (Distribution of Price and Quantity).
    * Outlier Detection using Boxplots.
4.  **Visualization & Interpretation**:
    * Explanatory charts to answer business questions.
5.  **Conclusion & Recommendation**:
    * Summarizing insights and proposing business actions.

## Key Insights & Findings

### 1. Product Polarization 
* **Retail Segment:** The **'Jumbo Bag Red Retrospot'** is the highest volume driver (traffic builder), but the **'Regency Cakestand 3 Tier'** generates the highest revenue.
* **Wholesale Segment:** The **'Jumbo Bag Red Retrospot'** dominates both volume and revenue.
* *Action:* Prioritize 'Jumbo Bag' stock availability as it is critical for both segments.

### 2. Seasonal Dynamics 
* **Wholesale:** Sales begin to rise in August and peak in **October**.
* **Retail:** Sales surge later, starting in September and peaking in **November**.
* *Action:* Inventory planning must start in Q3. wholesalers stock should be ready by October, while bulk stock for retail must be optimized for November.

### 3. Regional Performance
* **United Kingdom** dominates the market share.
* **Saudi Arabia** and **Bahrain** recorded the lowest transaction volumes.
* *Action:* Evaluate logistics costs for the Middle East region. If operational costs outweigh the thin margins, consider focusing resources on European markets instead.

## How to Run This Project
1.  Clone this repository:
    ```bash
    git clone [https://github.com/ChiefRz/Exploratory_Data_Analysis_on_the_Online_Retail_dataset.git](https://github.com/ChiefRz/Exploratory_Data_Analysis_on_the_Online_Retail_dataset.git)
    ```
2.  Install the required libraries:
    ```bash
    pip install pandas matplotlib seaborn numpy
    ```
3.  Open the notebook:
    ```bash
    jupyter notebook "Exploratory_Data_Analysis_on_the_Online_Retail_dataset.ipynb"
    ```
