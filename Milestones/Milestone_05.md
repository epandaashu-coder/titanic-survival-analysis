## Milestone 5 Report: Exploratory Data Analysis Findings

### Top 3 Survival Factors (Ranked by Impact)

1. **Gender (PRIMARY FACTOR)**
   - Female: 74.2% survival
   - Male: 18.9% survival
   - Impact: **55.3 percentage points difference**
   - Females were **3.9x more likely** to survive

2. **Passenger Class (SECONDARY FACTOR)**
   - 1st class: 63.0% survival
   - 2nd class: 47.3% survival
   - 3rd class: 24.2% survival
   - Impact: **38.8 percentage points range**
   - First class had **2.6x better** survival than third

3. **Age Group (TERTIARY FACTOR)**
   - Children (<18): 59.3% survival
   - Adults (18-59): 37.7% survival
   - Elderly (60+): 36.2% survival
   - Impact: **21.6 percentage points for children**
   - Children were **1.6x more likely** to survive

### Surprising Discoveries

1. **Family Size Sweet Spot**
   - Solo travelers: 30.4% survival
   - Families of 2-4: 50-72% survival ⭐ OPTIMAL
   - Large families (7+): 16.1% survival
   - **Insight:** Having family helped, but too large was detrimental

2. **The Class-Gender Intersection**
   - Female + 1st class: **96.8% survival** 🎯
   - Male + 3rd class: **13.5% survival**
   - **7.2x difference** between best and worst groups!
   - Being a woman mattered more than being rich

3. **Title as Strong Predictor**
   - Mrs/Miss: 79-70% survival (married/unmarried women)
   - Master: 58% survival (boys)
   - Mr: 16% survival (adult men)
   - Rare titles: 35% survival (mixed)
   - **Title alone predicts survival better than age!**

4. **Cabin Information Correlation**
   - With cabin record: 67% survival
   - Without cabin: 30% survival
   - **Why?** Likely proxy for class and deck location

5. **Port of Embarkation Pattern**
   - Cherbourg (C): 55% survival
   - Queenstown (Q): 39% survival
   - Southampton (S): 34% survival
   - **Why?** Cherbourg had more 1st class passengers

### Visualizations Created

1. **Demographic Survival Charts**
   - Sex-based bar chart (clear 55-point gap)
   - Class-based comparison (linear decrease)
   - Combined heatmap (revealed intersections)

2. **Age Distribution Analysis**
   - Overlaid histograms (children peak visible)
   - Box plots (similar medians, but different distributions)
   - Violin plots (showed multi-modal age patterns)

3. **Family & Economic Factors**
   - Family size U-curve (optimal at 2-4)
   - Fare quartiles (linear relationship with survival)
   - Scatter plot (high fares clustered with survivors)

4. **Multi-Variable Heatmaps**
   - Sex × Class (women dominated all classes)
   - Age Group × Sex (children of both sexes did well)
   - Title distribution (clear social hierarchy)

### Hypotheses Formed

1. **"Women and Children First" was strictly enforced**
   - Evidence: 74% female vs 19% male survival
   - Children had 59% survival vs 38% for adults
   - Even male children (Master) had 58% survival

2. **Social class translated directly to survival privilege**
   - Physical evidence: 1st class closer to lifeboats (boat deck)
   - Economic evidence: Could afford better accommodation
   - Social evidence: Crew prioritized wealthy passengers

3. **Family dynamics affected decision-making**
   - Small families stayed together → organized evacuation
   - Large families struggled to coordinate → delayed escape
   - Solo travelers had flexibility but less help

4. **Deck location was life-or-death**
   - 1st class on upper decks → quick lifeboat access
   - 3rd class in steerage → structural barriers, longer path
   - Cabin records correlate with survival (deck proximity)

### Statistical Insights

**Survival Rate Rankings:**
1. Female + 1st Class: 96.8%
2. Female + 2nd Class: 92.1%
3. Female + 3rd Class: 50.0%
4. Male + 1st Class: 36.9%
5. Male + 2nd Class: 15.7%
6. Male + 3rd Class: 13.5%

**Key Correlations Found:**
- Fare ↔ Survival: +0.26 (moderate positive)
- Pclass ↔ Survival: -0.34 (moderate negative)
- Sex (female=1) ↔ Survival: +0.54 (strong positive)
- Age ↔ Survival: -0.07 (weak negative)

### Business/Historical Questions Answered

**Q: Was the disaster equitable?**
❌ NO - Clear economic and gender disparities

**Q: Did crew follow "women and children first"?**
✅ YES - 74% female vs 19% male survival proves it

**Q: Did money buy survival?**
✅ PARTIALLY - 1st class 2.6x better than 3rd, but gender mattered more

**Q: Were families prioritized?**
✅ YES, but with limits - Small families did well, large families struggled

**Q: Could survival have been predicted?**
✅ YES - Sex, class, and age predict with ~80% accuracy

### Next Steps for Deeper Analysis

1. **Correlation matrix** of all numerical features
2. **Feature importance ranking** for prediction models
3. **Deck-level analysis** (if we extract from cabin)
4. **Embarkation port deep dive** (why Cherbourg better?)
5. **Ticket pricing analysis** (fare anomalies and patterns)
