# cafe-sales-data
Basic data handling in Python of a dataset of coffee shop

# Cafe Sales: Data Cleaning & Validation Pipeline

> **Resumen del proyecto:** Design of a Python project  to clean, standardize, and validate a dataset of coffee shop transactions containing corrupted data, transforming it into reliable information for decision-making.

---

## 1. Bussines Context 
this project is base in analyze historical sales data in order to optimize inventory and financial projections. The data extracted from the point-of-sale (POS) system contained critical anomalies: invalid text values ​​(`ERROR`, `UNKNOWN`), duplicate records, and mathematical inconsistencies between the quantities sold and the total amounts recorded. 

---

## 2. Tools y Tecnologies
* **Languaje:** Python
* **Librerías:** Pandas, NumPy
* **Entorno:** Jupyter Notebook
* **Control de Versiones:** Git & GitHub

---

## 3. Process and Methodology 

The project life cycle was divided into three key phases:

1. **Diagnosis and Audit:**
  * Detection of standard nulls and "false nulls" (text strings such as `'ERROR'` or `'UNKNOWN'`).
  * Identification of duplicate rows resulting from synchronization failures in the POS.
2. **Transformation and Cleansing:**
  * Replacing invalid strings with actual Pandas null values ​​(`NaN`).
  * Text standardization (removing extra spaces and applying consistent capitalization).
  * Data type conversion (dates to ISO format, monetary fields to floats).
3. **Validation and Mathematical Recalculation:**
   * Application of business rules to correct records where the relationship $\text{Total Spent} = \text{Quantity} \times \text{Price Per Unit}$ did not hold true.
---

## 📈 4. Results 

| Audited Metric| Initial State (Raw) | Final State (Clean) |
| :--- | :--- | :--- |
| **Total Records** | 10,000 rows | 9,850 rows (without duplicates) |
| **Anomalous Values (`ERROR` / `UNKNOWN`)** | 450 anomalies | 0 (Treated and cleaned) |
| **Mathematical Integrity** | 98.8% | 100% (Validated and recalculated) |
