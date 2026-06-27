# Part 1: Business Data Cleaning, Validation & Excel Reporting

## 1. Problem Summary

The objective of this assignment was to clean, validate, and prepare a retail sales dataset for business analysis. The dataset contained inconsistent text formatting, mixed date formats, duplicate records, missing values, invalid discounts, and business rule violations. The cleaned dataset was prepared for reporting and decision-making.

---

## 2. Dataset Description

- Dataset Name: Raw Orders
- Domain: Retail Sales
- File Used:
  - data/raw_orders.xlsx
  - data/cleaned_orders.xlsx
- Total Records After Cleaning: 914
- Data includes customer, product, sales, shipping, payment, and order information.

---

## 3. Tools Used

- Microsoft Excel
- Pivot Tables
- Excel Functions:
  - TRIM
  - IF
  - COUNTIF
  - ISNUMBER
  - YEAR
  - TEXT
- GitHub

---

## 4. Cleaning Steps Performed

- Preserved the original dataset.
- Created cleaned_orders.xlsx.
- Cleaned text fields.
- Standardized date formats.
- Calculated shipping_delay_days.
- Created cleaned_discount.
- Calculated sales.
- Calculated profit.
- Calculated profit margin.
- Extracted order_month and order_year.
- Removed exact duplicate records.
- Flagged duplicate Order IDs.
- Validated discounts.
- Created data_quality_flag.

---

## 5. Business Rules Applied

- Missing Region values replaced with "Unknown".
- Missing Ship Mode values replaced with "Unknown".
- Missing Discount values treated as 0 where applicable.
- Negative discounts flagged as Invalid.
- Discounts above allowed range flagged as Invalid.
- Ship date before order date flagged as Invalid Shipping Record.
- Cancelled and Failed Payment orders excluded from completed sales summary.
- Refunded orders reported separately.

---

## 6. Summary of Data Quality Issues Found

| Issue | Count |
|------|------:|
| Missing Region | 25 |
| Missing Ship Mode | 21 |
| Missing Discount | 34 |
| Exact Duplicate Rows | 33 |
| Duplicate Order IDs | 13 |
| Invalid Discount Records | 23 |
| Invalid Shipping Records | 21 |

---

## 7. Summary of Pivot Reports

The following Pivot Reports were created:

- Sales and Profit by Region
- Sales and Profit by Category and Sub Category
- Order Count by Ship Mode
- Profit Margin by Customer Segment
- Refunded, Cancelled and Failed Orders by Region
- Monthly Sales Trend

---

## 8. Key Business Insights

- The West and East regions generated strong sales.
- Office Supplies and Furniture contributed significantly to total sales.
- Standard Class was the most frequently used shipping mode.
- Duplicate records and invalid discounts were identified and corrected.
- Data quality improved after cleaning and validation.

---

## 9. Assumptions and Limitations

### Assumptions

- Maximum valid discount is 100%.
- Unknown values were used for missing categorical data.
- Shipping delay equals Ship Date minus Order Date.

### Limitations

- Some flagged records require manual verification.
- Results depend on the quality of the source dataset.

---

## 10. Screenshots Included

- raw_data_preview.png
- cleaned_data_preview.png
- date_validation_preview.png
- duplicate_validation.png
- business_rules_validation.png
- pivot_summary_1.png
- pivot_summary_2.png