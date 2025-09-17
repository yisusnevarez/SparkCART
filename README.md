# SparkCART Sales Transactions Analysis

### 📌 Project Overview
This project analyzes a dataset of 50,000 e-commerce sales transactions from **Ecom360**, a fictional global e-commerce retailer.  
The dataset includes customer demographics, product categories, purchase amounts, payment methods, and transaction dates.  

The goal is to uncover trends in customer behavior, revenue drivers, and business insights that can guide data-driven decision-making.  

---

### 🎯 Business Task
**“We want to understand our customers’ purchasing behavior to optimize marketing campaigns and product offerings.”**

Key stakeholder questions:  
1. What is the total revenue per product category?  
2. Which age group spends the most?  
3. Which countries generate the most sales?  
4. What is the average purchase amount by payment method?  
5. Are there seasonal trends or sales spikes by month/quarter?  
6. What is the distribution of users by country and age group?  

---

### 📂 Dataset Description
The dataset contains the following columns:

- **Transaction_ID** → Unique identifier for each transaction  
- **User_name** → Customer’s anonymized name  
- **Age** → Customer age in years  
- **Country** → Customer country of residence  
- **Product_Category** → Category of product purchased  
- **Purchase_Amount (US)** → Transaction value in US dollars  
- **Payment_Method** → Method used (Credit Card, PayPal, etc.)  
- **Date** → Date of transaction  

---

### 🛠️ Data Preparation
- **Data Cleaning**  
  - Removed duplicates, handled missing values, standardized date formats.  
  - Verified numerical columns (e.g., `purchase_amount`) for accuracy.  

- **Feature Engineering**  
  - Extracted **Day, Month, and Year** from the `Date` column to analyze **seasonality and time-based trends**.  
  - Created an **Age_Group** column (e.g., `<18`, `18–24`, `25–34`, `35–44`, `45–54`, `55+`) to study **customer demographics**.  

---
### 📊 Exploratory Data Analysis (EDA)
- **PivotTables & Charts (Excel)**  
  - Aggregated sales by product category, country, payment method, and age group.  
  - Analyzed monthly/quarterly trends using the derived `Month` and `Year` columns.
    **ExcelPDF**
    [View Excel workbook](e-commerce/PDF/ecommerce_transactionsv2.pdf)

- **SQL Queries **  
  - Used SQL for grouping, filtering, and aggregation to validate Excel findings.  
  - Example:  
    ```sql
    SELECT Product_Category, SUM(Purchase_Amount) AS Total_Revenue
    FROM sales_data
    GROUP BY Product_Category
    ORDER BY Total_Revenue DESC;
    ```  
- **Power Point**
- [View PowerPoint Presentation](e-commerce/PDF/SparkCART_project_portfolio.pdf)
---

### 📊 Key Findings (Examples)
- **Top Product Categories**: Electronics and Apparel contributed the largest share of revenue.  
- **Age Groups**: Customers aged **25–34** spent the most on average.  
- **Country Insights**: USA and UK were the top-performing countries.  
- **Payment Methods**: Credit Card was the most common payment type, while PayPal showed strong adoption in younger age groups.  
- **Sales Trends**: Q4 consistently showed higher sales, suggesting strong holiday seasonality.  
- **Customer Demographics**: Majority of transactions came from age groups between **20–40 years old**.  

---

### 💡 Recommendations
- **Expand Electronics & Apparel** product offerings, as they are the largest revenue drivers.  
- **Target Seasonal Campaigns** around Q4 to maximize holiday sales.  
- **Promote Alternative Payments** (e.g., PayPal, mobile wallets) to younger demographics.  
- **Develop Country-Specific Strategies** for emerging markets with high growth potential.  

---

### 📈 Next Steps
- Perform customer segmentation for deeper insights.  
- Use predictive modeling to forecast future sales.  
- Build interactive dashboards with Power BI/Tableau for stakeholders.  

---

### 👨‍💻 Author
**Jesus Antonio Nevarez**  
Data Analyst Portfolio Project | Kaggle Notebook | 2025  
