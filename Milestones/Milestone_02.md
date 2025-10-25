### Statistical Analysis Results

#### Age Analysis

| Statistic | Value |
|-----------|-------|
| **Mean** | 29.70 years |
| **Median** | 28.00 years |
| **Std Deviation** | 14.52 years |
| **Minimum** | 0.42 years |
| **Maximum** | 80.00 years |
| **Range** | 79.58 years |
| **25th Percentile** | 20.12 years |
| **75th Percentile** | 38.00 years |
| **IQR** | 17.88 years |

**Interpretation:** The age distribution is fairly normal with a slight right skew. The mean (29.70) being slightly higher than median (28.00) indicates some older passengers pulling the average up.

#### Fare Analysis

| Statistic | Value |
|-----------|-------|
| **Mean** | $32.20 |
| **Median** | $14.45 |
| **Std Deviation** | $49.69 |
| **Minimum** | $0.00 |
| **Maximum** | $512.33 |
| **Range** | $512.33 |

**Interpretation:** Highly right-skewed distribution! The mean ($32.20) is more than double the median ($14.45), indicating extreme outliers. A few wealthy passengers paid exceptionally high fares, pulling the average up significantly.

## Boolean Indexing Discoveries

### 1. Children Analysis (Age < 18)

- **Count:** 113 children (15.8% of passengers with known age)
- **Age range:** 0.42 - 17.00 years
- **Average child age:** 8.95 years
- **Youngest passenger:** 0.42 years (approximately 5 months old)

### 2. Expensive Fares (> $50)

- **Count:** 213 passengers (24.4%)
- **Average expensive fare:** $116.83
- **Most expensive ticket:** $512.33
- **These passengers likely traveled in first class**

### 3. Young Adults (20-40 years)

- **Count:** 468 passengers (65.5% of known ages)
- **This was the dominant age group on the ship**
- **Average age:** 29.15 years

### 4. Class-Based Fare Analysis

| Class | Avg Fare | Median Fare | Count |
|-------|----------|-------------|-------|
| **1st** | $84.15 | $60.29 | 216 |
| **2nd** | $20.66 | $14.25 | 184 |
| **3rd** | $13.68 | $8.05 | 491 |

**Key Finding:** First-class passengers paid **6.3x more** than third-class passengers on average!

### 5. Fare Categories Distribution

| Category | Range | Count | Percentage |
|----------|-------|-------|------------|
| **Low** | < $10 | 244 | 27.9% |
| **Medium** | $10-$50 | 417 | 47.7% |
| **High** | > $50 | 213 | 24.4% |

## Advanced NumPy Operations

### Multi-Condition Filtering Results

**Children with High Fares (< 18 years, > $30):**
- Count: 28 children
- Average fare paid: $72.58
- Highest fare: $263.00
- These were likely first or second-class children

**Elderly OR Cheap Fare (>60 OR <$10):**
- Total: 294 passengers
- Elderly only: 39 passengers
- Cheap fare only: 181 passengers
- Both conditions: 74 passengers

## NumPy Skills Mastered

### Functions Used
- `np.mean()`, `np.median()`, `np.std()`
- `np.min()`, `np.max()`, `np.percentile()`
- `np.isnan()`, `np.where()`
- `np.unique()` with `return_counts=True`
- Boolean indexing with `&`, `|`, `~`

### Key Learnings

1. **Array Alignment:** Always ensure arrays have the same shape before combining conditions
2. **NaN Handling:** Must explicitly remove NaN values for calculations
3. **Boolean Operations:** Use `&` (AND), `|` (OR), `~` (NOT) for conditions
4. **Efficiency:** NumPy operations are 4-5x faster than Pandas for pure numerical work
5. **Broadcasting:** NumPy excels at vectorized operations on entire arrays

### Critical Insight

**Why median ≠ mean for fare?**
The fare distribution is heavily right-skewed due to wealthy passengers:
- 50% of passengers paid ≤ $14.45
- But the top 25% paid $30+, with some paying over $500
- This pulled the mean ($32.20) significantly higher than the median

---

# 🐼 MILESTONE 3: Pandas Data Inspection (60 minutes)

## Selection Methods Mastered

### Column Selection

