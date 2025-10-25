# 🚀 Titanic Survival Analysis: Complete Learning Report
**One-Day NumPy & Pandas Intensive Journey**

**Date:** October 24, 2025  
**Dataset:** Titanic Survival Dataset (891 passengers)  
**Tools Used:** Python, NumPy, Pandas, Matplotlib, Seaborn, Jupyter Notebook

---

## 📊 Executive Summary

This project analyzed the Titanic disaster dataset to understand survival patterns and master fundamental data science skills. Through hands-on exploration using NumPy and Pandas, I discovered that **gender, passenger class, and age** were the primary factors influencing survival, with females having a 74% survival rate compared to only 19% for males.

**Key Achievement:** Successfully completed end-to-end data exploration from raw dataset to actionable insights in 3 hours.

---

# 🎯 MILESTONE 1: Setup & First Look (45 minutes)

## Dataset Overview

**Source:** Titanic Dataset from Data Science Dojo  
**Dimensions:** 891 rows × 12 columns  
**Target Variable:** Survived (0 = Died, 1 = Survived)

### Column Information

| Column | Type | Description | Non-Null Count |
|--------|------|-------------|----------------|
| PassengerId | int64 | Unique ID | 891 |
| Survived | int64 | Survival (0/1) | 891 |
| Pclass | int64 | Ticket class (1/2/3) | 891 |
| Name | object | Passenger name | 891 |
| Sex | object | Gender | 891 |
| Age | float64 | Age in years | 714 |
| SibSp | int64 | Siblings/spouses aboard | 891 |
| Parch | int64 | Parents/children aboard | 891 |
| Ticket | object | Ticket number | 891 |
| Fare | float64 | Passenger fare | 891 |
| Cabin | object | Cabin number | 204 |
| Embarked | object | Port of embarkation | 889 |

### Initial Statistical Summary

**Survival Statistics:**
- Total passengers: 891
- Survivors: 342 (38.4%)
- Non-survivors: 549 (61.6%)

**Age Statistics:**
- Mean age: 29.70 years
- Median age: 28.00 years
- Age range: 0.42 - 80.00 years
- Missing: 177 (19.9%)

**Fare Statistics:**
- Mean fare: $32.20
- Median fare: $14.45
- Fare range: $0.00 - $512.33
- Missing: 0

**Family Statistics:**
- Average siblings/spouses: 0.52
- Average parents/children: 0.38

### Key Observations

1. **Class Distribution:** 
   - 1st class: 216 passengers (24.2%)
   - 2nd class: 184 passengers (20.7%)
   - 3rd class: 491 passengers (55.1%)

2. **Gender Distribution:**
   - Male: 577 (64.8%)
   - Female: 314 (35.2%)

3. **Data Quality Issues:**
   - Age has 19.9% missing values
   - Cabin has 77.1% missing values
   - Embarked has 0.2% missing values

4. **Fare Distribution:**
   - Highly right-skewed (mean > median)
   - Indicates a few passengers paid very high fares
   - Suggests economic inequality among passengers

### Questions Raised

- Why is the median fare ($14.45) so much lower than mean ($32.20)?
- What factors influenced survival the most?
- Was there a "women and children first" policy?
- How did passenger class affect survival chances?
- Can we predict survival based on passenger characteristics?

---

# 🔢 MILESTONE 2: NumPy Fundamentals (60 minutes)

## NumPy Array Operations

### Arrays Created