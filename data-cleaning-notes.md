# 🧹 Data Cleaning & Preparation Notes

## 📊 Overview
This document outlines the data preprocessing steps taken to ensure accuracy, consistency, and reliability prior to analysis.

---

## 🔍 Initial Data Issues

The raw dataset contained several quality issues:

- Missing or null values in delivery timestamps  
- Duplicate shipment records  
- Inconsistent carrier and region naming conventions  
- Outliers in delivery times and distance metrics  
- Incomplete or misclassified shipment types  

---

## ⚙️ Cleaning Steps Performed

### 1. Data Validation
- Reviewed column types and formats  
- Verified consistency across key fields (dates, distances, carriers)

### 2. Handling Missing Values
- Removed records with critical missing fields (e.g., delivery timestamps)  
- Imputed minor missing values where appropriate  

### 3. Deduplication
- Identified duplicate shipment IDs  
- Removed redundant records to prevent skewed KPIs  

### 4. Standardization
- Normalized carrier names (e.g., formatting inconsistencies)  
- Standardized region and lane classifications  
- Unified truck type categories  

### 5. Feature Engineering
Created new fields to support analysis:

- **Delivery Delay** = Actual Delivery Date − Scheduled Delivery Date  
- **Distance Bands**:
  - 0–500 miles  
  - 501–1000 miles  
  - 1000+ miles  
- **Delay Severity Classification**:
  - On-Time  
  - Minor Delay  
  - Severe Delay  

### 6. Outlier Handling
- Flagged extreme delivery times and distances  
- Reviewed for data entry errors vs legitimate edge cases  

---

## 📈 Impact on Analysis

These steps ensured:

- Accurate delay rate calculations  
- Reliable carrier performance comparisons  
- Valid cost and efficiency insights  
- Confidence in executive-level recommendations  

---

## ✅ Final Outcome

The cleaned dataset provided a **trustworthy foundation** for identifying cost drivers, inefficiencies, and opportunities to improve Revenue Per Mile (RPM).
