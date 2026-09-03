# Global-Health-Supply-Chain-Analysis-Reporting-Period-2006-2015
Interactive Power BI dashboard and executive report analyzing a 10-year, $1.62B global health commodity supply chain dataset across 43 countries.
# Table Of Content
- Project Overview 
- Data Source
- Tools
- Data Cleaning/preparation
- Exploratory Data Analysis
- Data Analysis
- Result/Findings
- Recommendations
- Limitations

  ### Project Overview
This project looks at 10 years of global health supply chain data from 2006 to 2015. The goal was to track how $1.62 billion was spent, see how 189 million medical supplies reached 43 countries, check if shipments arrived on time, and spot risks like relying too much on a single supplier.

<img width="1205" height="675" alt="IMG-20260831-WA0025 (1)" src="https://github.com/user-attachments/assets/24cf99d4-c24e-43b0-a9ef-2923b9bdc524" />

  ### Data Source
The dataset used for this project contains supply chain and delivery data containing detailed information about orders, shipment dates, delivery costs, vendor details, and commodity categories across 43 countries.
### Tools
- Excel - Data Cleaning
- Power Query - Data Transformation
- Power BI - Data Analysis & Visualization

### Data Cleaning / Preparation
In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection
2. Handling missing values and data imputations
3. Data cleaning and formatting

### Exploratory Data Analysis
EDA involved exploring the supply chain data to answer key questions, such as:
- What is the total procurement spend trend over the 10-year period?
- Which countries received the largest volume of medical commodities?
- What is the overall on-time delivery rate across shipping corridors?
- Which product categories and vendors dominate the supply chain volume?

### Data Analysis
Includes fields, DAX measures, and analytical breakdowns used during the project:
- Total Spend = SUM(SCMS_Delivery_History[Total Spend])
- Total Units Shipped = SUM(SCMS_Delivery_History[Unit Quantity])
- On-Time Delivery Rate (%) = DIVIDE(CALCULATE(COUNT(SCMS_Delivery_History[Scheduled Delivery Date]), SCMS_Delivery_History[Delivery Status] = "On Time"), COUNT(SCMS_Delivery_History[Scheduled Delivery Date]), 0) * 100
- Average Unit Price = AVERAGE(SCMS_Delivery_History[Unit Price])

### Results / Findings
The results are summarized as follows:
1. Total procurement spend peaked significantly between 2011 and 2014, driven by donor program expansion.
2. Sub-Saharan Africa is the leading destination region, with Nigeria and South Africa receiving the highest shipment volumes.
3. Antiretrovirals (ARVs) are the top-performing commodity group in terms of volume and total spend.
4. SCMS Direct Procurement serves as the primary vendor handling the vast majority of commodity shipments.

### Recommendations
Based on the analysis, recommendations include:
1. Work with more suppliers so the supply chain does not rely on just one primary vendor.
2. Build regional shipping hubs in high-volume countries like Nigeria and South Africa to speed up deliveries.
3. Ship diagnostic test kits together with HIV medicines so health centers get everything they need at once.
4. Use long-term planning to smooth out big budget changes from year to year.

### Limitations
1. The data is older (2006–2015), so it may not reflect supply chain conditions today.
2. Some shipment records did not break down land transport costs separately from ocean shipping costs.

