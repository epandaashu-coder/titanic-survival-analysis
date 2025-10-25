### `.loc` (Label-based)

- Selects by row/column **labels**
- **Includes** the endpoint in slicing
- Example: `df.loc[0:4]` returns 5 rows (0, 1, 2, 3, 4)

### `.iloc` (Position-based)

- Selects by integer **positions**
- **Excludes** the endpoint in slicing
- Example: `df.iloc[0:4]` returns 4 rows (0, 1, 2, 3)

## Filtering Analysis Results

### Gender-Based Survival

| Gender | Total | Survived | Died | Survival Rate |
|--------|-------|----------|------|---------------|
| **Female** | 314 | 233 | 81 | **74.2%** |
| **Male** | 577 | 109 | 468 | **18.9%** |
| **Difference** | - | - | - | **55.3 points** |

**Critical Finding:** Females were **3.9x more likely to survive** than males!

### Class-Based Survival

| Class | Total | Survived | Died | Survival Rate | Avg Fare |
|-------|-------|----------|------|---------------|----------|
| **1st** | 216 | 136 | 80 | **63.0%** | $84.15 |
| **2nd** | 184 | 87 | 97 | **47.3%** | $20.66 |
| **3rd** | 491 | 119 | 372 | **24.2%** | $13.68 |

**Key Insights:**
- First class had **2.6x better survival** than third class
- Each class jump increased survival by ~15-20 percentage points
- Clear correlation between wealth and survival

### Age-Based Survival

| Age Group | Count | Survived | Survival Rate |
|-----------|-------|----------|---------------|
| **Children (<18)** | 113 | 67 | **59.3%** |
| **Adults (18-59)** | 554 | 209 | **37.7%** |
| **Elderly (60+)** | 47 | 17 | **36.2%** |

**Finding:** Children had significantly better survival rates, supporting the "women and children first" policy.

## Advanced Filtering Insights

### Combined Conditions Analysis

**Female Survivors:**
- Count: 233 women
- Survival rate: 74.2%
- Most were from 1st/2nd class

**First-Class Male Survivors:**
- Count: 45 men
- Only 36.2% of first-class males survived
- Still much lower than female survival rates

**Passengers Paying > $100 Who Survived:**
- Count: 52 passengers
- Average fare: $165.31
- Survival rate: 68.4%
- Money helped, but wasn't everything

**Children in Third Class:**
- Count: 79 children
- Survived: 30 (38.0%)
- Lower than overall child survival rate (59.3%)
- Class mattered even for children

## Pattern Recognition: Survival Factors

### Ranked by Importance

1. **Gender (Primary Factor)**
   - Female: 74.2% survival
   - Male: 18.9% survival
   - Impact: +55.3 percentage points

2. **Passenger Class (Secondary Factor)**
   - 1st class: 63.0%
   - 2nd class: 47.3%
   - 3rd class: 24.2%
   - Impact: ~39 percentage points range

3. **Age Group (Tertiary Factor)**
   - Children: 59.3%
   - Adults: 37.7%
   - Impact: +21.6 percentage points for children

4. **Fare/Wealth (Correlated with Class)**
   - > $100: 68.4% survival
   - < $10: 31.2% survival
   - Impact: +37.2 percentage points

### Combined Effects

**Best Survival Chances:**
- Female + First Class: **96.8% survival** (91/94)
- Female + Second Class: **92.1% survival** (70/76)

**Worst Survival Chances:**
- Male + Third Class: **13.5% survival** (47/347)
- Male + Third Class + Age 18-40: **11.2% survival**

**The "Women and Children First" Policy Was Real:**
- Overall female survival: 74.2%
- Child survival: 59.3%
- Adult male survival: 16.4%

## Missing Values Analysis

### Missing Data Summary

| Column | Missing Count | Missing % | Action Required |
|--------|--------------|-----------|-----------------|
| **Cabin** | 687 | 77.1% | Drop or convert to binary |
| **Age** | 177 | 19.9% | Fill with group median |
| **Embarked** | 2 | 0.2% | Fill with mode |
| **All Others** | 0 | 0.0% | Complete data |

### Missing Data Assessment

**Cabin Column:**
- 77.1% missing → Too much missing data
- Recommendation: **Drop column** OR create "Has_Cabin" binary feature
- Missing not random: Lower classes less likely to have cabin records

**Age Column:**
- 19.9% missing → Significant but manageable
- Recommendation: **Fill with median by Pclass + Sex**
- Pattern: Missing more common in 3rd class

**Embarked Column:**
- Only 2 missing (0.2%)
- Recommendation: **Fill with mode** (most common port: 'S')
- Minimal impact on analysis

### Data Completeness

- **Complete rows** (no missing values): 183 (20.5%)
- **Rows missing only Cabin**: 529 (59.4%)
- **Rows missing Age or Embarked**: 179 (20.1%)

**Decision:** We cannot drop rows with missing data as we'd lose 80% of the dataset!

## Key Pandas Operations Learned

### Functions Mastered
- `df['col']`, `df[['col1', 'col2']]` - Column selection
- `df.loc[]`, `df.iloc[]` - Row/column selection
- `df[condition]` - Boolean filtering
- `df.isnull()`, `df.dropna()` - Missing value handling
- `df.groupby()` - Not yet, coming in Milestone 5!

### Filtering Techniques
- Single condition: `df[df['Age'] < 18]`
- AND condition: `df[(df['Age'] < 18) & (df['Survived'] == 1)]`
- OR condition: `df[(df['Pclass'] == 1) | (df['Pclass'] == 2)]`
- NOT condition: `df[~df['Sex'].isin(['male'])]`

---

## 🎓 Overall Learning Summary (Milestones 1-3)

### Skills Acquired

**NumPy:**
- ✅ Array creation and manipulation
- ✅ Statistical calculations (mean, median, std, min, max)
- ✅ Boolean indexing and filtering
- ✅ Handling NaN values
- ✅ Array operations and broadcasting
- ✅ Conditional categorization with `np.where()`

**Pandas:**
- ✅ DataFrame inspection (`head`, `info`, `describe`)
- ✅ Column and row selection
- ✅ Label-based selection with `.loc`
- ✅ Position-based selection with `.iloc`
- ✅ Boolean filtering with conditions
- ✅ Missing value identification
- ✅ Data visualization with Seaborn/Matplotlib

**Data Analysis:**
- ✅ Exploratory data analysis workflow
- ✅ Pattern recognition in data
- ✅ Statistical interpretation
- ✅ Missing data assessment
- ✅ Feature importance identification

### Time Spent

- **Milestone 1:** 45 minutes (Setup & exploration)
- **Milestone 2:** 60 minutes (NumPy operations)
- **Milestone 3:** 60 minutes (Pandas filtering)
- **Total:** 2 hours 45 minutes

### Key Insights Discovered

1. **Gender was overwhelmingly the strongest predictor** of survival (55 point difference)

2. **"Women and children first" policy was clearly implemented:**
   - Female survival: 74.2%
   - Male survival: 18.9%
   - Child survival: 59.3%

3. **Socioeconomic class significantly impacted survival:**
   - First class: 63.0%
   - Third class: 24.2%
   - Wealth literally bought survival chances

4. **The intersection of factors was critical:**
   - Female + 1st class: 96.8% survival
   - Male + 3rd class: 13.5% survival
   - **7x difference between best and worst groups!**

5. **Data quality issues exist but are manageable:**
   - Cabin: Drop (too much missing)
   - Age: Fill strategically
   - Embarked: Simple imputation

---

## 📈 Next Steps

### Milestone 4: Data Cleaning
- Handle missing Age values
- Drop or transform Cabin column
- Create new engineered features
- Prepare clean dataset for analysis

### Milestone 5: Exploratory Data Analysis
- Deep dive into survival patterns
- Create comprehensive visualizations
- Answer complex business questions
- Generate insights for stakeholders

### Milestone 6-8: Advanced Analysis
- GroupBy operations and aggregations
- Correlation analysis
- Feature engineering
- Final comprehensive report

---

## 💡 Personal Reflections

### What I Learned

**Technical Skills:**
- NumPy is incredibly fast for numerical operations but requires manual NaN handling
- Pandas makes data exploration intuitive with automatic NaN handling
- Boolean indexing is powerful for answering complex questions
- Always check data shapes when combining arrays/conditions

**Analytical Insights:**
- Real-world data is messy (missing values, outliers, inconsistencies)
- Multiple factors interact to influence outcomes
- Visualization reveals patterns not obvious in numbers
- Domain knowledge (Titanic history) helps interpret findings

**Best Practices:**
- Write code incrementally and test each step
- Document findings as you go
- Use meaningful variable names
- Check for edge cases (NaN, zeros, outliers)
- Visualize before and after transformations

### Challenges Overcome

1. **Array shape mismatch error** → Learned to align arrays with common valid mask
2. **Understanding loc vs iloc** → Practiced with examples to internalize difference
3. **Boolean indexing syntax** → Mastered parentheses and `&`/`|` operators
4. **Missing value strategy** → Learned different approaches for different columns

### What's Next

Ready to move to **Milestone 4: Data Cleaning** where I'll:
- Implement smart missing value imputation
- Engineer new features from existing columns
- Create a clean, analysis-ready dataset
- Build features that improve predictive power

**Total time invested so far: ~3 hours**  
**Confidence level: High** ✅  
**Ready for advanced topics: YES** 🚀

---

*Report generated: October 24, 2025*  
*Dataset: Titanic Survival (891 passengers, 12 features)*  
*Tools: Python 3.x, NumPy, Pandas, Matplotlib, Seaborn*
