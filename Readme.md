# 🚢 Titanic Survival Analysis: Data Science Project

![Python](https://img.shields.io/badge/Python-3.14-blue)
![NumPy](https://img.shields.io/badge/NumPy-1.26-green)
![Pandas](https://img.shields.io/badge/Pandas-2.2-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8-red)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-purple)

A comprehensive data analysis project exploring survival patterns in the Titanic disaster using NumPy, Pandas, and advanced visualization techniques.

## 📊 Project Overview

This project analyzes the Titanic dataset (891 passengers) to uncover the factors that influenced survival during the 1912 disaster. Through hands-on exploration, I discovered that **gender, passenger class, and age** were the primary determinants of survival, with females having a **74.2%** survival rate compared to only **18.9%** for males.

### 🎯 Key Findings

- **Gender Impact**: 55.3 percentage point gap between female and male survival
- **Class Disparity**: First-class passengers had 2.6x better survival odds than third class
- **Women & Children First**: Policy was strictly enforced with 59.3% child survival rate
- **Family Dynamics**: Optimal family size was 2-4 people (best survival rates)
- **Predictive Model**: Developed scoring system with 0.54 correlation to actual survival

## 🛠️ Technologies Used

- **Python 3.14**: Primary programming language
- **NumPy**: Array operations and numerical computing
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical graphics
- **Jupyter Notebook**: Interactive development environment

## 📁 Project Structure
# Create a clean project folder
📁 titanic-survival-analysis/
├── 📓 titanic_analysis.ipynb           # Your Jupyter notebook
├── 📄 titanic_cleaned_analysis.csv     # Cleaned dataset (if exported)
├── 📄 titanic_executive_summary.txt    # Executive summary
├── 📄 README.md                        # Will create this
├── 📄 .gitignore                       # Will create this
└── 📁 images/                          # Screenshots of charts (optional)
    ├── age_distribution.png
    ├── survival_heatmap.png
    └── correlation_matrix.png


## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- - > python --version
- Install required packages
- - > pip install numpy pandas matplotlib seaborn jupyter scipy

### Installation

1. Clone the repository:
> git clone https://github.com/YOUR_USERNAME/titanic-survival-analysis.git
> cd titanic-survival-analysis

2. Launch Jupyter Notebook:
> jupyter notebook titanic_analysis.ipynb


3. Run all cells to reproduce the analysis

## 📈 Analysis Pipeline

### 1. **Data Loading & Exploration**
- Loaded 891 passenger records with 12 features
- Identified missing values (Age: 19.9%, Cabin: 77.1%)
- Generated statistical summaries

### 2. **Data Cleaning**
- Smart imputation: Group-based median for Age (by Pclass + Sex)
- Created binary features (Has_Cabin, Is_Alone)
- Handled missing Embarked (mode) and Fare (median)

### 3. **Feature Engineering**
Created 7 new predictive features:
- `FamilySize`: Total family members aboard
- `Is_Alone`: Binary indicator for solo travelers
- `Title`: Extracted from name (Mr, Mrs, Miss, Master, Rare)
- `Age_Group`: Categorical age bins
- `Fare_Group`: Fare quartiles
- `Has_Cabin`: Cabin information availability
- `Survival_Score`: Weighted predictive score (0-100)

### 4. **Exploratory Data Analysis**
- Survival rate by demographics (Sex, Pclass, Age)
- Multi-variable analysis (Sex × Pclass interactions)
- Family dynamics and optimal group size
- Fare distribution and correlation with survival

### 5. **Data Visualization**
- Distribution plots with KDE curves
- Correlation heatmaps
- Categorical survival analysis
- Interactive pairplots

### 6. **Predictive Modeling**
- Developed weighted survival scoring system
- Validated with 0.54 correlation to actual outcomes
- Risk assessment categorization

## 📊 Key Visualizations

### Survival by Gender and Class
![Survival Heatmap](images/survival_heatmap.png)
*Female passengers in first class had 96.8% survival rate*

### Age Distribution
![Age Distribution](images/age_distribution.png)
*Children had significantly higher survival rates*

### Correlation Matrix
![Correlation Matrix](images/correlation_matrix.png)
*Feature relationships and survival predictors*

## 🔍 Insights & Conclusions

### Primary Findings

1. **Gender Dominance**: Being female increased survival by 3.9x
2. **Socioeconomic Privilege**: First-class passengers had superior lifeboat access
3. **Maritime Protocol**: "Women and children first" was enforced
4. **Family Sweet Spot**: Families of 2-4 had 50-72% survival (optimal coordination)
5. **Predictability**: Survival was highly predictable from passenger attributes

### Statistical Evidence

| Factor | Impact | Survival Range |
|--------|--------|----------------|
| Gender | 55.3% gap | 18.9% (M) - 74.2% (F) |
| Class | 38.8% gap | 24.2% (3rd) - 63.0% (1st) |
| Age | 21.6% gap | 37.7% (Adult) - 59.3% (Child) |

### Best vs Worst Odds

- **Best**: Female + 1st Class = **96.8%** survival
- **Worst**: Male + 3rd Class = **13.5%** survival
- **Spread**: 7.2x difference between best and worst groups

## 🧠 Skills Demonstrated

### Data Science
- ✅ Exploratory Data Analysis (EDA)
- ✅ Statistical hypothesis testing
- ✅ Feature engineering
- ✅ Missing value imputation strategies
- ✅ Correlation analysis
- ✅ Predictive modeling

### Technical
- ✅ NumPy array operations and vectorization
- ✅ Pandas DataFrames and GroupBy operations
- ✅ Custom aggregation functions
- ✅ Apply/Lambda functions
- ✅ Pivot tables and cross-tabulations
- ✅ Advanced Matplotlib/Seaborn visualizations

### Analytical
- ✅ Pattern recognition
- ✅ Multi-variable analysis
- ✅ Risk assessment modeling
- ✅ Data storytelling
- ✅ Executive reporting

## 📚 Learning Outcomes

This project was completed as part of a **one-day intensive bootcamp** to learn NumPy and Pandas from scratch. Through hands-on analysis, I:

- Mastered fundamental data manipulation techniques
- Developed proficiency in data visualization
- Built a complete end-to-end analysis pipeline
- Created actionable insights from raw data
- Documented findings professionally

**Time Investment**: ~8 hours  
**Result**: Complete data analysis portfolio piece

## 🔗 References

- Dataset: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic)
- Historical Context: [Encyclopedia Titanica](https://www.encyclopedia-titanica.org/)
- Libraries: [NumPy Docs](https://numpy.org/) | [Pandas Docs](https://pandas.pydata.org/)

## 📫 Contact

**Your Name**  
- GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)
- LinkedIn: [Your LinkedIn](https://www.linkedin.com/in/your-profile)
- Email: your.email@example.com

## 🙏 Acknowledgments

- Dataset provided by Kaggle
- Inspired by the historical tragedy of RMS Titanic
- Built as a learning project to master data science fundamentals

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⭐ **If you found this project helpful, please give it a star!** ⭐

*Last Updated: October 25, 2025*

