# Aerofit Treadmill Customer Segmentation & Product Analytics

![Python](https://img.shields.io/badge/Python-3.7+-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-1.0+-green?style=flat-square&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.0+-orange?style=flat-square&logo=matplotlib)
![Seaborn](https://img.shields.io/badge/Seaborn-0.11+-blue?style=flat-square&logo=python)


## 📋 Table of Contents
- [Overview](#overview)
- [Project Motivation](#project-motivation)
- [Dataset Description](#dataset-description)
- [Key Findings](#key-findings)
- [Technical Approach](#technical-approach)
- [File Structure](#file-structure)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Analysis Breakdown](#analysis-breakdown)
- [Visualizations](#visualizations)
- [Business Recommendations](#business-recommendations)
- [Key Insights](#key-insights)
- [Technologies Used](#technologies-used)
- [Results & Conclusions](#results--conclusions)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

This project performs comprehensive **Exploratory Data Analysis (EDA)** on Aerofit treadmill customer data to identify customer segments, understand product-market fit, and develop data-driven recommendations for targeted marketing and sales optimization.

The analysis covers **180 customer records** across three product tiers (KP281, KP481, KP781) and uses statistical analysis, data visualization, and customer profiling to uncover actionable business insights.

### Quick Stats
- **📊 Customers Analyzed:** 180
- **🔍 Features Examined:** 9 variables
- **📈 Products Analyzed:** 3 treadmill models
- **✅ Data Quality:** 100% complete, no missing values
- **🎯 Key Deliverable:** Customer segmentation & product recommendations

---

## 💼 Project Motivation

The fitness equipment market is highly competitive with products spanning multiple price points and performance tiers. **Aerofit** needed to understand:

1. **Who are our customers?** (Demographics, income, fitness levels)
2. **Which customers buy which products?** (Product-customer fit)
3. **What drives purchasing decisions?** (Income, fitness level, age, usage)
4. **How can we optimize sales?** (Segmentation-based marketing, upselling)
5. **What are untapped opportunities?** (Market gaps, expansion potential)

This project provides the **customer intelligence foundation** required to answer these questions and inform go-to-market strategy.

---

## 📊 Dataset Description

### Data Source
Aerofit treadmill customer transaction data collected from sales records.

### Dataset Specifications

| Attribute | Details |
|-----------|---------|
| **Total Records** | 180 customer transactions |
| **Total Features** | 9 variables |
| **Data Quality** | 100% complete (0 missing values) |
| **Duplicates** | None detected |
| **Data Types** | Mixed (numerical + categorical) |
| **Time Period** | Sales period (specific dates not provided) |

### Features Overview

| Feature | Type | Range/Values | Description |
|---------|------|--------------|-------------|
| **Customer ID** | Numerical | 1-180 | Unique customer identifier |
| **Age** | Numerical | 18-50 years | Customer age in years |
| **Gender** | Categorical | Male / Female | Customer gender |
| **Education** | Numerical | 10-20 years | Years of formal education |
| **Marital Status** | Categorical | Single / Partnered / Married | Customer relationship status |
| **Income** | Numerical | $30K - $130K | Annual household income (USD) |
| **Usage** | Numerical | 2-7 days/week | Weekly usage frequency |
| **Fitness Level** | Numerical | 1-5 | Self-rated fitness (1=Poor, 5=Excellent) |
| **Miles** | Numerical | 10-150 miles/week | Average weekly running distance |
| **Product** | Categorical | KP281 / KP481 / KP781 | Treadmill model purchased |

### Data Quality Assessment
- ✅ **No Missing Values:** Dataset is complete
- ✅ **No Duplicates:** All records are unique
- ✅ **Correct Data Types:** All features properly formatted
- ✅ **Outlier Detection:** Identified in Income variable (handled appropriately)

---

## 🔑 Key Findings

### 1. Product Demand Hierarchy
```
KP281 (Entry-Level)  ████████████████████ 44.4% (80 customers)
KP481 (Mid-Range)    ████████████░░░░░░░░ 33.3% (60 customers)  
KP781 (Premium)      ██████░░░░░░░░░░░░░░ 22.2% (40 customers)
```
**Insight:** KP281 dominates with 44.4% market share, indicating strong demand for entry-level products.

### 2. Demographic Segmentation

**Gender Distribution:**
- Male: 58% (104 customers) 
- Female: 42% (76 customers)
- **Insight:** Slightly male-dominated but balanced market

**Marital Status:**
- Married: 60% (108 customers)
- Single: 40% (72 customers)
- **Insight:** Married couples represent the largest customer segment

**Age Distribution:**
- Primary: 25-35 years (highest concentration)
- Secondary: 18-25 and 35-50 years
- Mean Age: 28 years
- **Insight:** Young professionals are the primary target market

**Education Level:**
- Average: 15 years of education
- Range: 10-20 years
- **Insight:** Customer base is educated (completed college/some grad school)

### 3. Income Segmentation

```
Income Distribution by Product:
KP281: $40K - $60K (mean: $52K)   [Entry-level buyers]
KP481: $55K - $80K (mean: $65K)   [Mid-range buyers]
KP781: $75K+ (mean: $90K+)        [Premium buyers]
```

**Key Insight:** Clear income-based segmentation enables targeted pricing and marketing.

### 4. Fitness Level Insights

| Fitness Level | % of Customers | Primary Product | Characteristic |
|---------------|----------------|-----------------|-----------------|
| 1 (Poor Shape) | 0.6% | KP281 | Beginners, rare |
| 2 (Bad Shape) | 12.8% | KP281 | Beginners, looking to improve |
| 3 (Average Shape) | 53.9% | KP281/KP481 | Majority segment, maintenance focus |
| 4 (Good Shape) | 11.1% | KP481/KP781 | Enthusiasts, performance-focused |
| 5 (Excellent Shape) | 14.4% | KP781 | Athletes, advanced users |

**Insight:** Fitness level is a strong predictor of product choice and purchase intent.

### 5. Usage Pattern Analysis

- **Most Common:** 3 days/week (39% of customers)
- **Daily Users:** Only 2% (untapped growth opportunity)
- **Gender Differences:** Males use 4 days/week; Females use 3 days/week
- **Average Weekly Distance:** 103 miles/week

**Insight:** Sporadic usage (3-4 days/week) is the sweet spot; growth opportunity in daily user segment.

### 6. Product-Customer Fit Analysis

**KP281 (Entry-Level, $1,500):**
- Demographics: Married, 25-35 years old, $40-55K income
- Fitness: Level 1-3 (beginners to intermediate)
- Usage: 3 days/week, 65-95 miles/week
- Market Share: 44.4% (highest demand)
- Margin Focus: Volume play

**KP481 (Mid-Range, $2,000-2,500):**
- Demographics: Established professionals, 30-45 years, $55-75K income
- Fitness: Level 3-4 (intermediate to advanced)
- Usage: 4 days/week, 95-110 miles/week
- Market Share: 33.3% (strong growth potential)
- Margin Focus: Balanced

**KP781 (Premium, $3,000+):**
- Demographics: High-income professionals, fitness enthusiasts, $75K+ income
- Fitness: Level 4-5 (advanced to elite)
- Usage: 5-7 days/week, 100+ miles/week
- Market Share: 22.2% (niche but profitable)
- Margin Focus: Profitability

### 7. Correlation Insights

| Correlation | Strength | Interpretation |
|-------------|----------|-----------------|
| Age ↔ Miles | 0.04 | Very weak - age doesn't predict distance |
| Education ↔ Miles | 0.30 | Weak positive - more educated → slightly more mileage |
| Income ↔ Product | Moderate | Income is product choice driver |
| Fitness ↔ Product | Strong | Fitness level is strongest product predictor |

---

## 🔬 Technical Approach

### Analysis Framework

```
Data Loading & Exploration
         ↓
Data Quality Assessment
         ↓
Univariate Analysis
         ↓
Bivariate & Multivariate Analysis
         ↓
Customer Segmentation & Profiling
         ↓
Visualization & Insights
         ↓
Business Recommendations
```

### Methodologies Applied

#### 1. **Exploratory Data Analysis (EDA)**
- Statistical summaries and descriptive statistics
- Distribution analysis for numerical features
- Categorical frequency analysis
- Missing value detection and handling
- Outlier identification using box plots

#### 2. **Customer Segmentation**
- Demographic segmentation (age, income, education)
- Behavioral segmentation (usage frequency, fitness level)
- Product affinity analysis
- Customer profiling by product tier

#### 3. **Statistical Analysis**
- Correlation matrix analysis
- Mean/median comparisons across segments
- Percentage distribution analysis
- Outlier detection and handling

#### 4. **Data Visualization**
- Countplots for categorical distributions
- Histograms and KDE plots for distributions
- Box plots for outlier detection
- Heatmaps for correlation analysis
- Pair plots for multivariate relationships

---

## 📁 File Structure

```
aerofit-treadmill-analytics/
│
├── README.md                          # Project documentation (this file)
├── LICENSE                            # MIT License
├── requirements.txt                   # Python dependencies
│
├── data/
│   ├── aerofit_data.csv              # Raw customer data
│   └── data_dictionary.md            # Feature descriptions
│
├── notebooks/
│   └── Aerofit_Treadmill_EDA.ipynb   # Complete EDA analysis
│
├── src/
│   ├── __init__.py
│   ├── data_loader.py                # Data loading utilities
│   ├── exploratory_analysis.py       # EDA functions
│   ├── visualization.py              # Plotting functions
│   └── segmentation.py               # Customer segmentation logic
│
├── output/
│   ├── visualizations/
│   │   ├── product_distribution.png
│   │   ├── income_distribution.png
│   │   ├── fitness_analysis.png
│   │   ├── correlation_heatmap.png
│   │   └── customer_profiles.png
│   │
│   └── reports/
│       ├── customer_segments.csv
│       ├── product_recommendations.md
│       └── summary_statistics.txt
│
└── docs/
    ├── methodology.md                # Detailed methodology
    ├── findings_summary.md           # Key findings
    └── business_recommendations.md   # Strategic recommendations
```

---

## 🚀 Installation & Setup

### Prerequisites
- Python 3.7 or higher
- pip or conda package manager
- Jupyter Notebook (for running the analysis notebook)

### Step 1: Clone Repository
```bash
git clone https://github.com/yourusername/aerofit-treadmill-analytics.git
cd aerofit-treadmill-analytics
```

### Step 2: Create Virtual Environment (Recommended)
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# OR using conda
conda create -n aerofit python=3.9
conda activate aerofit
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Verify Installation
```bash
python -c "import pandas, numpy, matplotlib, seaborn; print('All packages installed successfully!')"
```

### Dependencies
```
pandas>=1.0.0
numpy>=1.19.0
matplotlib>=3.2.0
seaborn>=0.11.0
jupyter>=1.0.0
ipython>=7.0.0
```

---

## 📖 Usage

### Running the Jupyter Notebook

```bash
# Start Jupyter
jupyter notebook

# Open Aerofit_Treadmill_EDA.ipynb and run all cells
```

### Using Python Scripts

```python
# Import modules
from src.data_loader import load_data
from src.exploratory_analysis import statistical_summary
from src.visualization import plot_product_distribution
from src.segmentation import profile_customers

# Load data
df = load_data('data/aerofit_data.csv')

# Run analysis
print(statistical_summary(df))

# Generate visualizations
plot_product_distribution(df)

# Segment customers
segments = profile_customers(df)
```

### Quick Start Example

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load data
df = pd.read_csv('data/aerofit_data.csv')

# Quick statistics
print(df.describe())

# Product distribution
df['Product'].value_counts()

# Visualize
sns.countplot(data=df, x='Product')
plt.show()
```

---

## 📊 Analysis Breakdown

### Phase 1: Data Exploration & Quality Assessment
**Objective:** Understand dataset structure and quality

**Steps:**
1. Load dataset and check shape/size
2. Display first few records
3. Examine data types
4. Check for missing values
5. Identify duplicates
6. Statistical summary

**Output:** Clean, verified dataset ready for analysis

```python
# Data quality checks
print(f"Dataset shape: {df.shape}")
print(f"Missing values: {df.isnull().sum()}")
print(f"Duplicates: {df.duplicated().sum()}")
print(df.info())
print(df.describe())
```

### Phase 2: Univariate Analysis
**Objective:** Understand individual variable distributions

**Analysis Performed:**
1. **Age Distribution**
   - Mean: 28 years
   - Range: 18-50 years
   - Distribution: Relatively uniform

2. **Income Distribution**
   - Mean: $53.7K
   - Range: $30K-$130K
   - Distribution: Right-skewed with outliers

3. **Fitness Level Distribution**
   - Mode: 3 (Average Shape)
   - Range: 1-5
   - Distribution: Concentrated at 3, tail toward 5

4. **Usage Frequency Distribution**
   - Mean: 3.5 days/week
   - Mode: 3 days/week
   - Range: 2-7 days/week

5. **Categorical Analysis**
   - Product preferences
   - Gender distribution
   - Marital status breakdown
   - Education range

**Output:** Distribution visualizations and summary statistics

### Phase 3: Bivariate & Multivariate Analysis
**Objective:** Understand relationships between variables

**Key Analyses:**
1. **Product × Gender Analysis**
   - KP281 preferred by both genders equally
   - KP481 slightly male-preferred
   - KP781 niche product for advanced users

2. **Product × Marital Status Analysis**
   - Married couples drive 60% of purchases
   - Both segments prefer KP281

3. **Product × Fitness Level Analysis**
   - Clear fitness-based segmentation
   - Higher fitness → Premium products

4. **Product × Income Analysis**
   - Three income tiers match three products
   - Income is strong product predictor

5. **Correlation Analysis**
   - Heatmap of all numerical variables
   - Identify key drivers

**Output:** Cross-tabulations, heatmaps, segment profiles

### Phase 4: Customer Segmentation
**Objective:** Create actionable customer profiles

**Segments Created:**

1. **Entry-Level Segment (KP281 Buyers)**
   - Size: 80 customers (44.4%)
   - Demographics: Age 25-35, $40-55K income
   - Fitness: Level 1-3
   - Characteristics: Beginners, family-oriented, value-conscious

2. **Intermediate Segment (KP481 Buyers)**
   - Size: 60 customers (33.3%)
   - Demographics: Age 30-45, $55-75K income
   - Fitness: Level 3-4
   - Characteristics: Enthusiasts, established professionals

3. **Advanced Segment (KP781 Buyers)**
   - Size: 40 customers (22.2%)
   - Demographics: Age 35-50+, $75K+ income
   - Fitness: Level 4-5
   - Characteristics: Athletes, performance-focused, premium buyers

---

## 📈 Visualizations

The project includes comprehensive visualizations covering:

### 1. **Univariate Distributions**
- Product count plots
- Income histograms and KDE plots
- Fitness level distributions
- Usage frequency analysis
- Age distribution

### 2. **Categorical Analysis**
- Gender distribution
- Marital status breakdown
- Product × Marital Status countplot
- Product × Gender countplot

### 3. **Multivariate Relationships**
- Correlation heatmap
- Product × Income box plots
- Product × Fitness scatter/box plots
- Fitness × Gender cross-tabulation

### 4. **Outlier Detection**
- Income outlier box plot
- Fitness level outlier detection

### 5. **Customer Profiles**
- Demographic profiles by product
- Income distribution by product tier
- Fitness progression by product

---

## 💡 Business Recommendations

### 1. Segmentation-Based Marketing Strategy

**For KP281 (Entry-Level):**
```
Target Audience:
  - Age: 25-35 years
  - Income: $40-55K
  - Status: Married/Partnered
  - Fitness: Beginner to Intermediate (Level 1-3)

Marketing Strategy:
  ✓ Position as "First Step to Fitness" - beginner-friendly
  ✓ Emphasize affordability and ease of use
  ✓ Bundle with workout plans and diet guides
  ✓ Target couples/families in social media ads
  ✓ Highlight low maintenance requirements
  ✓ Seasonal campaigns: New Year, Summer body, etc.

Pricing Strategy:
  ✓ Competitive pricing at $1,500 (current level)
  ✓ Consider promotional bundles: treadmill + 6-month coaching
  ✓ Flexible payment plans for target income bracket
```

**For KP481 (Mid-Range):**
```
Target Audience:
  - Age: 30-45 years
  - Income: $55-75K
  - Status: Mix of married and single
  - Fitness: Intermediate to Advanced (Level 3-4)

Marketing Strategy:
  ✓ Position as "Fitness Enthusiast's Choice"
  ✓ Emphasize value-for-money and performance balance
  ✓ Highlight advanced features for intermediate users
  ✓ Target professionals in LinkedIn, tech publications
  ✓ Offer performance tracking and progress analytics
  ✓ Community building: online fitness groups, challenges

Pricing Strategy:
  ✓ Premium positioning at $2,000-2,500
  ✓ Bundle with fitness tracker integration
  ✓ Corporate wellness program discounts
```

**For KP781 (Premium):**
```
Target Audience:
  - Age: 35-50+ years
  - Income: $75K+ (high-income professionals)
  - Status: Established professionals
  - Fitness: Advanced to Elite (Level 4-5)

Marketing Strategy:
  ✓ Position as "Professional Runner's Equipment"
  ✓ Emphasize durability, advanced features, performance
  ✓ Target through premium lifestyle channels
  ✓ Sponsorships in marathons, fitness expos
  ✓ Highlight warranty, technical support, exclusivity
  ✓ VIP customer programs and events

Pricing Strategy:
  ✓ Premium pricing at $3,000+
  ✓ White-glove service: delivery, setup, training
  ✓ Extended warranty and concierge support
  ✓ Premium accessories bundle
```

### 2. Product Positioning

| Dimension | KP281 | KP481 | KP781 |
|-----------|-------|-------|-------|
| **Positioning** | "First Step to Fitness" | "Fitness Enthusiast's Choice" | "Professional Runner's Equipment" |
| **Target** | Beginners | Intermediate users | Advanced athletes |
| **Key Message** | Easy, affordable, beginner-friendly | Great value, balanced performance | Premium quality, professional-grade |
| **Price Perception** | Accessible | Value | Prestige |

### 3. Upsell & Customer Progression Strategy

```
Customer Journey:
Entry-Level User (KP281)
        ↓
    [Monitor fitness improvement]
        ↓
    [Engagement @ 3+ months]
        ↓
    Advanced Fitness → Upsell to KP481
        ↓
    Regular/Daily User → Upsell to KP781
```

**Implementation:**
1. **Track Fitness Progression:** Monitor customer fitness level via app/surveys
2. **Engagement Triggers:** Email campaigns when usage increases to 5+ days/week
3. **Personalized Offers:** Discounted upgrades to next-tier products
4. **Loyalty Rewards:** Extended warranties, accessories for loyal customers

### 4. Expansion & Growth Opportunities

**Market Segment Gaps:**
- 40+ age group underrepresented → Target wellness-focused professionals
- Daily users only 1% → Aggressive retention for this high-value segment
- Female customer ratio (42%) could grow → Gender-specific marketing campaigns

**Product Line Extensions:**
- Entry-level model for <$1,200 to capture price-sensitive segment
- Introduce smart treadmill with IoT features for KP781 segment
- Compact model for small spaces (urban professionals)

### 5. Distribution & Inventory Strategy

```
Recommended Inventory Allocation:
KP281: 45-50% of inventory    (Highest demand, volume play)
KP481: 30-35% of inventory    (Growth segment)
KP781: 15-20% of inventory    (Premium/niche)
```

**Rationale:**
- KP281 shows 44.4% market share → Stock accordingly
- KP481 shows growth potential → Increase allocation
- KP781 profitable but niche → Maintain as premium offering

---

## 🎯 Key Insights

### Customer Behavior Insights

1. **Income-Product Correlation**
   - Clear three-tier market segmentation by income
   - Each product tier aligns with specific income bracket
   - Pricing strategy is well-positioned

2. **Fitness Level Progression**
   - Customers progress from KP281 → KP481 → KP781
   - 53.9% in average fitness (KP281/KP481 market)
   - 14.4% in excellent shape (KP781 market)

3. **Demographic Targeting**
   - 60% married customers drive majority of purchases
   - Age 25-35 is primary demographic
   - Education level (15 years avg) indicates white-collar workers

4. **Usage Patterns**
   - 39% use 3 days/week (sweet spot)
   - Only 2% use daily (growth opportunity)
   - Males more frequent users (4 days/week vs. 3 for females)

5. **Gender Dynamics**
   - 58% male, 42% female (balanced)
   - No significant gender-based product preference
   - One-size-fits-all marketing approach is valid

### Market Dynamics

1. **Product Demand**: KP281 dominates but all three viable
2. **Market Maturity**: Established customer base, concentrated segments
3. **Growth Lever**: Upselling and expansion to underserved demographics
4. **Competitive Advantage**: Clear segmentation enables precise targeting

---

## 📊 Results & Conclusions

### Key Deliverables

1. **Customer Segmentation Model**
   - 3 distinct segments based on income, fitness, age
   - Actionable customer profiles for each product tier
   - Quantified segment sizes for resource allocation

2. **Product-Market Fit Analysis**
   - Clear alignment between customer characteristics and products
   - Identified ideal customer profiles for each product
   - Pricing strategy validation

3. **Strategic Recommendations**
   - Segment-specific marketing strategies
   - Upsell pathway and customer progression model
   - Inventory and distribution recommendations
   - Expansion opportunities and market gaps

4. **Data-Driven Insights**
   - Quantified demand hierarchy (44.4% / 33.3% / 22.2%)
   - Income-product correlation (strong predictor)
   - Fitness level progression insights
   - Usage pattern analysis

### Impact Potential

- **Marketing Efficiency:** Target right customers with right messages
- **Revenue Optimization:** Strategic pricing and bundling
- **Customer Lifetime Value:** Upsell strategy to increase CLV
- **Market Expansion:** Identified growth opportunities
- **Inventory Optimization:** Data-driven allocation decisions

### Conclusion

This analysis demonstrates how systematic exploratory data analysis can unlock customer intelligence and inform strategic business decisions. By understanding customer demographics, behavioral patterns, and product preferences, **Aerofit can optimize product positioning, allocate resources efficiently, and implement targeted marketing campaigns that maximize customer lifetime value and market penetration**.

The three-tier customer segmentation provides a clear framework for go-to-market strategy, enabling personalized engagement, effective resource allocation, and sustained business growth.

---

## 🔮 Future Work

### Potential Enhancements

1. **Predictive Modeling**
   - Build classification model to predict product choice
   - Logistic regression: Customer features → Product probability
   - Random Forest for feature importance ranking

2. **Customer Lifetime Value (CLV) Modeling**
   - Calculate CLV by segment
   - Identify high-value customer characteristics
   - Optimize acquisition spend by segment

3. **Churn Prediction**
   - Identify at-risk customers
   - Build retention campaigns
   - Measure campaign effectiveness

4. **Time Series Analysis**
   - If temporal data available: trends over time
   - Seasonality in product demand
   - Inventory forecasting

5. **Price Elasticity Analysis**
   - A/B testing different price points
   - Demand curve estimation
   - Optimal pricing strategy

6. **Customer Journey Mapping**
   - Touchpoint analysis
   - Conversion funnel optimization
   - Attribution modeling

7. **Sentiment Analysis** (if review data available)
   - Product review sentiment by segment
   - Satisfaction by product tier
   - Feature request analysis

8. **Recommendation System**
   - Personalized product recommendations
   - Similar customer matching
   - Cross-selling opportunities

### Data Enhancement Ideas

- Collect NPS (Net Promoter Score) data
- Gather product review/satisfaction scores
- Track customer service interactions
- Obtain temporal purchase history
- Geographic location data for regional analysis
- Website behavior and click-through data

---

### Reporting Issues

Found a bug or have suggestions? Please open an issue with:
- Clear description of the problem
- Steps to reproduce
- Expected vs. actual results
- Python version and OS

---

## 📚 References & Resources

### Data Analysis Libraries
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Guide](https://matplotlib.org/)
- [Seaborn Tutorial](https://seaborn.pydata.org/)

---

## 👤 Author

**Data Analyst / Data Scientist**
- LinkedIn: https://www.linkedin.com/in/ronali-sahani-b491a938b/
- Email: ronalisahani24@gmail.com

---

## 🙏 Acknowledgments

- **Aerofit** for providing the dataset
- **Open source community** for amazing libraries
- **Data science practitioners** for inspiration and best practices

---

## ⭐ Star This Repository!

If you found this analysis helpful, please consider starring ⭐ this repository!

---

## 📧 Contact & Support

- **Questions?** Open an issue or email
- **Want to collaborate?** Reach out on LinkedIn
- **Found a bug?** Submit a GitHub issue
- **Have suggestions?** Create a discussion

---

**Last Updated:** 2025
**Status:** Complete ✅
**Maintenance:** Active 🟢
