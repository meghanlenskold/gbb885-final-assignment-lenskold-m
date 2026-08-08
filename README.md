# gbb885-final-assignment-lenskold-m
# RUSH Sales Analysis
This repository is for the final assignment for GB885. Sales data cleaning and analysis for RUSH sportswear.

## Overview
RUSH stores its raw sales data across three tables: sales transactions, retailer locations, and product category. The purpose of this project is to clean, merge, and analyze this data to answer a set of business questions posed by the VP of US Sales.

## Data Cleaning
The raw data required several fixes before analysis:
  UNITS_SOLD was stored as text and converted to numeric
  INVOICE_DATE was converted from text to datetime
  Two rows were missing both PRICE_PER_UNIT and UNITS_SOLD - these were dropped
  A TOTAL_SALES column was calculated as PRICE_PER_UNIT x UNITS_SOLD
  An extreme outlier order was identified and removed after checking summary statistics
  One row failed to match during the merge (null RETAILER_ID) and was dropped

## Business Questions Answered
1. What product category had the highest sales (in dollars) in 2021?
2. What state had the highest sales (in dollars) of women's products in 2021?
3. What state had the highest sales (in dollars) of men's products in 2021?
4. What retailer purchased the most units in 2021? In 2020?
