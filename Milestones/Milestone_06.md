## Milestone 6 Report: Advanced Pandas Operations

### GroupBy Insights

**Multi-Level Aggregations Performed:**
- Survival statistics by Sex + Pclass (6 groups analyzed)
- Age and fare summaries by passenger class
- Embarkation port analysis with 4 different metrics
- Custom survival rate formatting for readability

**Key Findings from GroupBy:**
1. **Class 3 had highest passenger count** (491) but lowest survival (24%)
2. **Cherbourg passengers had best survival** (55%) - likely more 1st class
3. **Age range by class:** 1st: 0-80 years, 3rd: 0-74 years (similar spread)
4. **Fare disparity:** 1st class avg $84 vs 3rd class $14 (6x difference)

### Custom Functions Created

**1. Risk Assessment Function**
- Weighted scoring based on Sex (3 pts), Class (2 pts), Age (1 pt), Alone status (1 pt)
- Categories: High Risk, Medium Risk, Low Risk
- **Validation:** Predicted risk aligned with actual survival rates!
  - Low Risk → 74% survival ✅
  - Medium Risk → 38% survival ✅
  - High Risk → 9% survival ✅

**2. Fare Categorization**
- Budget (<$10), Standard ($10-$50), Premium ($50-$100), Luxury (>$100)
- Distribution: 27% Budget, 48% Standard, 16% Premium, 9% Luxury

**3. Family Category**
- Alone, Small (2-3), Large (4+)
- **Finding:** Small families had best survival (68%)

### String Operations Mastered

**Text Extraction:**
- Last names extracted from full name (surname)
- First names extracted (between comma and period)
- Ticket prefixes isolated for analysis

**Pattern Detection:**
- 517 passengers had "Mr." in name (adult males)
- 125 passengers had "Mrs." (married women)
- 182 passengers had "Miss." (unmarried women/girls)
- 36 names contained nicknames in parentheses

**Ticket Analysis:**
- 681 numeric tickets vs 210 alphanumeric
- Most common prefix: "CA" (96 passengers)
- No significant survival difference by ticket type

### Pivot Table Findings

**Key Pivot Insights:**

**1. Survival Matrix (Sex × Class):**
- Female advantage exists in ALL classes
- Class differences more pronounced for males

**2. Fare by Title × Class:**
- Master (boys): Class 1 avg $100, Class 3 avg $21
- Mrs: Highest fares across all classes
- Mr: Widest fare range (budget to luxury)

**3. Age × Sex Survival:**
- Female children: 69% survival
- Male children: 51% survival  
- Female adults: 75% survival
- Male adults: 16% survival

### Advanced Techniques Applied

**1. Lambda Functions:**
- Quick conditional categorizations
- Inline aggregations without function definitions
- Efficient data transformations

**2. Apply with axis=1:**
- Row-wise operations for risk assessment
- Multi-column conditional logic
- Custom feature engineering

**3. Method Chaining:**
- Streamlined data pipelines
- Cleaner, more readable code
- Reduced intermediate variables

**4. Named Aggregations:**
- Self-documenting aggregation operations
- Clear column names in output
- Better code maintainability

### Skills Progression

**Before Milestone 6:**
- Basic groupby operations
- Simple aggregations (mean, sum)
- Manual loops for custom operations

**After Milestone 6:**
✅ Complex multi-level groupby
✅ Custom aggregation functions
✅ Advanced pivot tables (3+ dimensions)
✅ String manipulation and extraction
✅ Apply/lambda for transformations
✅ Risk modeling with custom scoring

### Performance Insights

**Most Efficient Operations:**
1. Vectorized string operations (vs loops)
2. Built-in aggregations (vs custom functions)
3. Pivot tables (vs manual cross-tabs)

**Code Elegance Improvements:**
- Named aggregations >>> column renaming after agg
- Lambda functions >>> defining simple functions
- Method chaining >>> multiple separate operations

### Next Applications

These advanced Pandas skills enable:
- **Feature engineering** for machine learning models
- **Data pipelines** for automated reporting
- **Complex business queries** without SQL
- **Interactive dashboards** with real-time filtering
- **Text analytics** from unstructured data
