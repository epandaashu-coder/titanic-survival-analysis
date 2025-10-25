# 🧭 Titanic Survival Analysis — Project-Based Learning with NumPy & Pandas

### **Dataset Taken:** *Titanic Survival*
#### **Tools:** Anaconda, Jupyter Notebook, NumPy, Pandas, Matplotlib, Seaborn
#### **Goal:** Clean data, analyze patterns, answer real questions, and build confidence

---

## 📝 Notes

1. **Why Titanic Dataset?**
   - Real Historical Data with mixed types (*Numerical + Categorical*)
   - Contains Missing Values
   - Clear objective: Understand survival patterns
   - Industry-standard beginner project for data science

---

## 🧩 Project Milestones

> **🗓️ Total:** 8 Milestones — Step-by-Step Learning Path

---

## 🚀 MILESTONE 1: Setup & First Look (45 min)

**Learn:** Environment setup, load dataset, inspect structure

### **Tasks:**
- Install libraries and load Titanic CSV
- Use the following commands:

```python
df.shape
df.head()
df.info()
df.describe()
```

**Answer:**
- How many passengers are there?
- What columns exist?
- What data types are present?

**Report:**  
Write initial observations in Markdown.

---

## ⚙️ MILESTONE 2: NumPy Fundamentals (60 min)

**Learn:** Arrays, numerical operations, boolean indexing

### **Tasks:**
- Convert DataFrame columns to NumPy arrays
- Calculate statistics — mean, median, std, min, max
- Boolean indexing — Find children (age < 18), expensive fares (>$50)
- Create age groups with `np.where()`

**Challenge:**  
Categorize fares as Low / Medium / High

**Report:**  
Document NumPy operations learned.

---

## 📊 MILESTONE 3: Pandas Basics (60 min)

**Learn:** DataFrame selection, filtering, missing values

### **Tasks:**
- Master `loc` and `iloc` selection methods
- Filter with conditions — survivors, female survivors, first-class passengers
- Calculate survival rates by gender
- Visualize missing data with heatmap

**Pattern Recognition:**  
Compare male vs female survival rates.

**Report:**  
Key filtering insights discovered.

⏸️ **Break (15–20 min)**

---

## 🧼 MILESTONE 4: Data Cleaning (60 min)

**Learn:** Handle missing values, feature engineering

### **Tasks:**
- Fill missing **Age** using group-based median (by `Pclass` + `Sex`)
- Handle **Embarked** (mode) and **Fare** (median)
- Create binary feature: `Has_Cabin`
- **Feature Engineering:**
  - `FamilySize = SibSp + Parch + 1`
  - Extract `Title` from Name (Mr, Mrs, Miss, Master)
  - Create `Age_Group` bins (Child, Teen, Adult, Senior)
  - Create `Fare_Group` quartiles

**Report:**  
Document cleaning strategy and new features.

---

## 🔍 MILESTONE 5: Exploratory Data Analysis (90 min)

**Learn:** GroupBy, aggregations, visualizations

### **Tasks:**
- Calculate survival rates by Sex, Pclass, Age_Group
- Create bar plots comparing survival across demographics
- Analyze family size impact on survival
- Cross-tabulation: `Sex × Pclass` survival heatmap

**Key Questions:**
- Was there a “women and children first” policy?
- Which class had best survival?
- Did larger families survive better?

**Report:**  
Top 3 survival factors and surprising discoveries.

⏸️ **Lunch Break (45–60 min)**

---

## 🧠 MILESTONE 6: Advanced Pandas (75 min)

**Learn:** GroupBy mastery, apply/lambda, pivot tables, string ops

### **Tasks:**
- Multiple aggregations with `agg()` dictionary
- Create custom functions with `apply()` and `lambda`
- String operations — extract last name, ticket prefix
- Pivot tables — survival by multiple dimensions

**Challenge:**  
Create risk categorization function.

**Report:**  
Advanced operations insights.

---

## 📈 MILESTONE 7: Visualization Deep Dive (60 min)

**Learn:** Matplotlib, Seaborn, storytelling with data

### **Tasks:**
- Distribution plots: Age and Fare by survival
- Categorical analysis: Bar plots for all features
- Correlation heatmap of numerical features
- Pairplot to see relationships

**Interpretation:**  
Which features correlate with survival?

**Report:**  
Visual insights and patterns discovered.

---

## 🏁 MILESTONE 8: Final Project (60 min)

**Synthesize & Deliver:**

### **Tasks:**
- Create survivor vs victim profiles
- Build survival score predictor
- Export cleaned dataset to CSV

### **Write Final Report Including:**
- Executive Summary
- Data Cleaning Process
- Key Findings (ranked)
- Surprising Discoveries
- Skills Acquired
- Next Steps

---

✅ **End of One-Day Project — Titanic Survival Analysis**
> Congratulations! You’ve built, cleaned, analyzed, and visualized your first real dataset using NumPy & Pandas!
