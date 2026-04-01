# Aerofit Treadmill Customer Analysis

# Project Overview

This project analyzes customer data from Aerofit to understand purchasing patterns across three treadmill models — KP281, KP481, and KP781. The objective is to derive actionable business insights and provide data-driven recommendations for product positioning, customer segmentation, and revenue optimization.

# Objectives
Analyze customer demographics and behavior
Identify patterns influencing product purchases
Compare usage, income, and fitness levels across products
Provide business recommendations for each product category
Build a data-driven strategy for customer conversion and retention

# Dataset Description

The dataset contains customer information including:
Product → KP281, KP481, KP781
Age → Customer age
Gender → Male/Female
Education → Years of education
Marital_Status → Married/Single
Usage → Weekly treadmill usage
Fitness → Self-rated fitness level
Income → Annual income
Miles → Average miles walked/run per week

# Tools & Technologies Used
Python 
Pandas
NumPy
Matplotlib & Seaborn
Google Colab

# Exploratory Data Analysis (EDA)
1.  Univariate Analysis
Distribution of age, income, and fitness levels
Product-wise customer distribution
2. Bivariate Analysis
Income vs Product
Usage vs Product
Fitness vs Product
3. Multivariate Analysis
Correlation between income, usage, and miles
Customer segmentation patterns

 # Key Insights
🔹 KP281 (Entry-Level)
Highest sales volume
Preferred by low to mid-income customers
Lower usage and fitness levels
Suitable for beginners
🔹 KP481 (Mid-Range)
Balanced customer segment
Moderate income and usage
Acts as a transition product
🔹 KP781 (Premium)
High-income customers
Highest usage and fitness levels
Lower sales volume due to high price
Preferred by serious fitness enthusiasts
# Sample Visualizations
import seaborn as sns
import matplotlib.pyplot as plt

# Income vs Product
sns.boxplot(x='Product', y='Income', data=df)
plt.title("Income Distribution Across Products")
plt.show()
# Usage comparison
sns.barplot(x='Product', y='Usage', data=df)
plt.title("Usage Across Products")
plt.show()
# Correlation heatmap
sns.heatmap(df.corr(), annot=True)
plt.title("Correlation Matrix")
plt.show()

# Business Recommendations
🔹 KP281 (Entry-Level Strategy)
Position as beginner-friendly product
Use for customer acquisition
Provide bundled services (diet/workout plans)
Build upselling pipeline to higher models
🔹 KP481 (Growth Strategy)
Target customers upgrading from KP281
Highlight value-for-money features
Use personalized recommendations based on usage
🔹 KP781 (Premium Strategy)
Introduce EMI/payment options
Position as performance treadmill
Target high-income and high-usage customers
Expand female customer segment
🔹 Overall Strategy
Implement a product ladder approach:
KP281 → Entry
KP481 → Upgrade
KP781 → Premium
Focus on:
Customer lifetime value (CLV)
Data-driven upselling
Targeted marketing campaigns

# Key Learnings
Applied EDA techniques to real-world dataset
Understood customer segmentation strategies
Learned how to convert data insights into business recommendations
Strengthened storytelling for data-driven decision making


