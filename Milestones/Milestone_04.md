## Milestone 4 Report: Data Cleaning & Feature Engineering

### Missing Values Handled

| Column | Missing Count | Strategy | Result |
|--------|--------------|----------|---------|
| **Age** | 177 (19.9%) | Fill with group median (Pclass + Sex) | ✅ 0 missing |
| **Embarked** | 2 (0.2%) | Fill with mode ('S') | ✅ 0 missing |
| **Fare** | 1 (0.1%) | Fill with median | ✅ 0 missing |
| **Cabin** | 687 (77.1%) | Drop column, create Has_Cabin binary | ✅ Transformed |

### Why Group-Based Age Filling is Better

**Simple filling** (overall median): All missing ages → 28 years
**Smart filling** (group median): Respects demographic differences
- 1st class female: ~35 years
- 3rd class male: ~25 years
- Preserves age distribution better

### New Features Created

1. **Has_Cabin:** Binary (0/1) - passengers with cabin info had 67% survival vs 30%
2. **FamilySize:** SibSp + Parch + 1 - families of 2-4 had best survival
3. **Is_Alone:** 1 if alone, 0 if with family - families survived better
4. **Title:** Mr, Mrs, Miss, Master, Rare - strong survival predictor
5. **Age_Group:** Child, Teen, Young Adult, Adult, Senior - children survived best
6. **Fare_Group:** Low, Medium, High, Very High - higher fare = better survival
7. **Name_Length:** Number of characters - minimal correlation

### Key Insights from Feature Engineering

1. **Family size matters:** Optimal family size was 2-4 people
   - Solo travelers: 30% survival
   - Families of 2-4: 50-70% survival
   - Large families (7+): 16% survival

2. **Title predicts survival:** 
   - Mrs/Miss/Master: 70-80% (women & children)
   - Mr: 16% (adult males)
   - Rare titles: 35% (mixed group)

3. **Cabin information correlates with class:**
   - Having cabin info: 67% survival
   - No cabin info: 30% survival
   - Likely because 1st class had better cabin records

4. **Fare quartiles show clear pattern:**
   - Very High: 58% survival
   - Low: 31% survival
   - Wealth provided survival advantage

### Data Quality Improvements

**Before Cleaning:**
- 177 missing ages
- 687 missing cabins  
- 2 missing embarked
- Limited features

**After Cleaning:**
- ✅ 0 missing values in critical columns
- ✅ 7 new engineered features
- ✅ Better feature representations
- ✅ Ready for advanced analysis

### Decisions Made

1. **Dropped Age_Simple column** - kept Age_Smart as 'Age'
2. **Dropped Cabin column** - too much missing, created Has_Cabin instead
3. **Grouped rare titles** - reduces noise, improves signal
4. **Created binned features** - Age_Group and Fare_Group for categorical analysis

### Next Steps

With clean data and engineered features, ready for:
- Deep exploratory data analysis (Milestone 5)
- GroupBy operations and aggregations (Milestone 6)
- Visualization and correlation analysis (Milestone 7)
- Final insights and predictions (Milestone 8)
