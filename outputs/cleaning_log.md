# Cleaning Log

## Assignment
Part 1: Business Data Cleaning, Validation & Excel Reporting

---

## 1. Issues Found

- Inconsistent text formatting.
- Mixed date formats in order_date and ship_date.
- Duplicate records.
- Duplicate Order IDs with conflicting information.
- Missing Region values.
- Missing Ship Mode values.
- Missing Discount values.
- Negative discount values.
- Ship dates earlier than order dates.
- Inconsistent business data.

---

## 2. Cleaning Actions Performed

- Cleaned text fields using TRIM and standardization.
- Standardized all date formats.
- Created shipping_delay_days column.
- Created cleaned_discount column.
- Created calculated_sales column.
- Created calculated_profit column.
- Created profit_margin column.
- Created order_month and order_year columns.
- Created data_quality_flag column.
- Removed exact duplicate rows.
- Flagged duplicate Order IDs.
- Replaced missing Region values with "Unknown".
- Replaced missing Ship Mode values with "Unknown".
- Replaced missing Discount values with 0 where applicable.

---

## 3. Business Rules Applied

- Missing Region → Filled with "Unknown".
- Missing Ship Mode → Filled with "Unknown".
- Missing Discount → Treated as 0 when appropriate.
- Negative Discount → Flagged as Invalid.
- Discount greater than allowed range → Flagged as Invalid.
- Ship Date before Order Date → Flagged as Invalid Shipping Record.
- Cancelled Orders excluded from completed sales summary.
- Failed Payments excluded from completed sales summary.
- Refunded Orders summarized separately.

---

## 4. Assumptions Made

- Maximum valid discount = 100% (1.0).
- Unknown values were used for missing categorical fields.
- Shipping delay calculated as Ship Date minus Order Date.
- Original raw data remained unchanged.

---

## 5. Records Removed

- Exact Duplicate Rows Removed: 33

---

## 6. Records Flagged

- Duplicate Order IDs Found: 13
- Records Flagged for Review: 26
- Invalid Discount Records: 23
- Invalid Shipping Records: 21

---

## 7. Limitations

- Some business validations depend on available source data.
- Manual review may still be required for flagged records.
- Business rules were applied only according to the assignment instructions.
