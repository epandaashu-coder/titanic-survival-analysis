## Milestone 7 Report: Data Visualization Deep Dive

### Visualizations Created

**1. Distribution Plots (4 charts)**
- Age distribution with KDE curves (survivors vs victims)
- Fare distribution histogram (showing right skew)
- Family size bar chart (optimal size 2-4 highlighted)
- Embarkation port stacked bar chart

**2. Categorical Analysis (4 charts)**
- Gender survival (absolute counts + percentages)
- Class survival (proportional stacked bars)
- Title survival rates (horizontal bars with sample sizes)
- Age group × Gender interaction (grouped bars)

**3. Correlation Analysis (3 visualizations)**
- Full correlation heatmap (lower triangle masked)
- Survival correlation bar chart (ranked by strength)
- Scatter plot: Fare vs Survival Score

**4. Pairplot (Multi-panel)**
- 5 key features: Survived, Pclass, Age, Fare, FamilySize
- Corner plot for efficiency
- KDE on diagonal, scatter on off-diagonal

### Key Visual Insights

**From Distributions:**
1. **Age patterns:** Survivors slightly younger (mean 28.3 vs 30.6 years)
2. **Fare skewness:** Highly right-skewed; survivors paid median $26 vs $10 for victims
3. **Family sweet spot:** Families of 2-4 had best survival rates
4. **Port differences:** Cherbourg 55%, Queenstown 39%, Southampton 34% survival

**From Categorical Analysis:**
1. **Gender dominance:** Visual confirmation of 55-point gap (largest bars)
2. **Class stratification:** Clean linear relationship in proportional bars
3. **Title predictive power:** Mrs/Miss/Master cluster at 70%+ (green bars)
4. **Age-gender interaction:** Women outsurvived men in EVERY age group

**From Correlation Analysis:**
1. **Survival_Score validation:** +0.54 correlation proves scoring system works
2. **Top predictors:** Fare (+0.26), Has_Cabin (+0.32), Pclass (-0.34)
3. **Weak correlations:** SibSp (-0.03), Age (-0.07) - minimal direct impact
4. **Multi-collinearity:** Fare ↔ Pclass (-0.55) as expected (class determines fare)

### Visualization Techniques Mastered

**Matplotlib:**
- Subplots and grid specification
- Custom color schemes and alpha blending
- Annotations and text labels
- Axis formatting and limits
- Line styles and markers
- Legend positioning

**Seaborn:**
- Heatmaps with annotations
- Pairplots with hue
- Count plots and bar plots
- Violin plots and box plots
- KDE plots
- Color palettes (husl, coolwarm, Set2)

**Advanced Features:**
- Dual y-axes
- Stacked and grouped bars
- Masked correlation matrices
- Statistical overlays (mean lines, confidence intervals)
- Custom colormaps
- Figure-level and axes-level plots

### Design Principles Applied

1. **Color Psychology:**
   - Red for deaths/negative correlations
   - Green for survivors/positive correlations
   - Neutral colors for categories

2. **Clarity:**
   - Large, bold titles
   - Clear axis labels with units
   - Grid lines for reading values
   - Annotations for key points

3. **Information Density:**
   - Multi-panel figures (4-6 charts per figure)
   - Combined absolute + percentage information
   - Sample sizes noted where relevant

4. **Storytelling:**
   - Titles explain the insight, not just the data
   - Ordered by importance (strongest patterns first)
   - Comparisons highlighted visually

### Publication-Ready Features

✓ High resolution (300 DPI for exports)
✓ Consistent color schemes across charts
✓ Professional fonts and sizing
✓ White space and padding
✓ Clear legends and labels
✓ Grid lines for precision
✓ Statistical annotations

### Most Impactful Visualizations

**1. Gender Survival Bar Chart**
- Instantly shows 74% vs 19% gap
- Most powerful single chart
- Could stand alone in presentation

**2. Correlation Heatmap**
- Reveals all relationships at once
- Identifies multi-collinearity
- Guides feature selection for modeling

**3. Age Distribution with KDE**
- Shows nuanced differences
- Statistical rigor with density curves
- Beautiful and informative

**4. Title Survival Rates**
- Encodes both gender and age
- Sample sizes prevent misinterpretation
- Clear actionable insight

### Next Applications

These visualization skills enable:
- **Executive presentations** (board-ready charts)
- **Academic publications** (journal-quality figures)
- **Interactive dashboards** (Plotly/Dash foundation)
- **Data journalism** (compelling visual stories)
- **Portfolio projects** (showcase-quality work)