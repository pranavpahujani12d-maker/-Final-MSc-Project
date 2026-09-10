# Dynamic Markdown Optimisation: Predictive Analytics for Markdown Decision Support
This repository contains the code and analysis for a Master's-level dissertation project submitted to the University of Exeter. The project provides a proof-of-concept comparison of predictive machine learning models designed to support markdown and clearance decisions in online retail. Rather than mathematically optimising profit or waste, this project classifies product-days as high-demand to assist category managers in evaluating potential discount depths.
# Dataset
The empirical analysis utilizes the publicly accessible UCI Online Retail II dataset.
The dataset consists of transaction records from a UK-based, online giftware and wholesale retailer
The data used in this study focuses on Q4 2010 (October 1 to December 23).
The raw transaction logs were cleaned and aggregated to the product-day level, yielding a dataset of 77,528 observations across 2,598 unique stock keeping units (SKUs).
# Technologies & Libraries Used
Language: Python
Data Processing: pandas
Machine Learning: scikit-learn and XGBoost
Business Intelligence: Microsoft Power BI Desktop (used for the operational dashboard
#Power BI Dashboard Prototype
To bridge the gap between backend analytics and frontline operations, the model's outputs were translated into a decision-support dashboard designed for retail category managers. Following Stephen Few’s clarity criteria for visual design, the prototype consists of three interlinked views:
Overview Page: A scorecard-style view displaying the current number of items flagged for high demand, the assortment's average demand probability, and a four-week trend line of high-probability days to track clearance performance.
Product-Level Detail Page: A comprehensive table of individual SKUs showing current stock, discount levels, and predicted demand probabilities. This allows managers to quickly identify where current markdowns are either insufficient or excessive.
# Key Findings & Project Highlights
Top Performing Algorithm: XGBoost proved to be the most efficient model, outperforming both Random Forest and the Logistic Regression benchmark.
Feature Importance: The analysis revealed that the depth of the discount and the breadth of transactions (n_transactions) are the strongest determinants of clearance-style demand
Robustness Checks: To ensure the model reflects real-world deployment, a strict robustness check (Specification C) was conducted by removing leak-prone, same-day variables (qty and n_transactions), which still yielded a highly predictive AUC-ROC of 0.752 and an F1 score of 0.629
Dashboard Translation: The predictive outputs were translated into a Power BI dashboard design specification, featuring an overview scorecard, a product-level detail table, and a discount sensitivity "what-if" chart
# Ethical Considerations
The project was built exclusively using secondary, anonymized transaction data.
The report acknowledges the ethical risk of algorithmic pricing targeting price-sensitive consumers, recommending that any real-world deployment include a human-controlled "minimum-discount floor
The model is strictly designed as a decision-support tool for human category managers, not an automated pricing execution engine.
