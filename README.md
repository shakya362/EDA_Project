📊 Industry Dataset – Exploratory Data Analysis (EDA)
A comprehensive Exploratory Data Analysis of a global industry dataset covering 15,000 companies across 5 industries, 4 countries, and 3 regions. The project performs end-to-end analysis — from data quality checks to multivariate business insights.

📁 Project Structure
EDA_Project.ipynb        # Main Jupyter Notebook with all analysis
INDUSTRY.csv             # Source dataset (not included in repo)
README.md                # Project documentation

📦 Dataset Overview
AttributeDetailsRecords15,000 companiesIndustriesFinance, Technology, Retail, Manufacturing, HealthcareCountriesUSA, Canada, Germany, IndiaRegionsNorth America, Asia, EuropeNumerical Colsemployee_count, annual_revenue_million, profit_margin_percent, founded_year, customer_count, market_ratingCategorical Colscompany_name, industry, country, regionDate Columncreated_date

🛠️ Libraries Used
pythonpandas        # Data manipulation
numpy         # Numerical computing
seaborn       # Statistical visualizations
matplotlib    # Plotting
scipy.stats   # Statistical tests (z-score, linregress)
math          # Grid layout calculations

🔍 Analysis Workflow
1. Data Loading & Initial Exploration

Loaded dataset from CSV
Inspected shape, columns, dtypes, and summary statistics (describe())

2. Data Quality Checks

Missing Values: No missing values found
Duplicate Records: No duplicates detected
Inconsistency Check: No inconsistent values in company_name, industry, country, or region
Transformation: created_date converted to datetime; id column dropped

3. Univariate Analysis

Numerical Variables: Descriptive statistics (mean, median, std, skewness, kurtosis) + histograms with KDE
Categorical Variables: Frequency tables + bar charts + pie chart for industry distribution

4. Outlier Detection

IQR Method: No outliers detected across all 6 numerical features
Z-Score Method (|z| > 3): Zero outliers confirmed
Boxplots: Visual validation of clean, stable distributions

5. Bivariate Analysis

Numerical vs Numerical: Scatter plots with regression lines and Pearson correlation coefficients for key pairs
Correlation Matrix: Heatmap showing near-zero correlations across all variable pairs
Numerical vs Categorical: Group-level bar charts (Industry × Revenue, Region × Employee Count, Country × Rating)

6. Multivariate Analysis

Industry × Revenue × Employee Count
Region × Market Rating × Profit Margin
Country × Customer Count × Revenue
Industry × Founded Year × Revenue

7. Skewness & Kurtosis Analysis

All variables show near-zero skewness (−0.02 to +0.03) → approximately symmetric distributions
All variables show negative kurtosis (~−1.19 to −1.21) → platykurtic distributions (light tails, no extreme outliers)


💡 Key Business Insights
MetricFinding🏆 Highest Revenue IndustryRetail (~$556.6M avg)💰 Most Profitable IndustryFinance (~25% avg margin)🌏 Most Profitable RegionAsia (25.08% margin)👥 Largest Workforce RegionEurope🇮🇳 Highest Revenue CountryIndia (~$551.9M)📈 Highest Customer Base CountryCanada (~51,453 avg)⚠️ Industry Needing Cost ReviewManufacturing (lowest margin)📊 Correlation StrengthNear-zero across all variable pairs🎯 Outliers DetectedNone (IQR + Z-Score confirmed)⚖️ Dataset BalancePerfectly balanced by industry & country

📈 Visualizations Included

Histograms with KDE for all numerical variables
Bar charts for industry, country, and region distributions
Pie chart for industry share
Boxplots for outlier detection
Scatter plots with regression lines for bivariate analysis
Pearson correlation heatmap
Grouped bar charts for multivariate analysis
Kurtosis bar chart


▶️ How to Run

Clone the repository

bash   git clone https://github.com/your-username/industry-eda.git
   cd industry-eda

Install dependencies

bash   pip install pandas numpy seaborn matplotlib scipy

Place the dataset
Put INDUSTRY.csv in the same directory as the notebook (or update the file path inside the notebook).
Launch Jupyter Notebook

bash   jupyter notebook EDA_Project.ipynb

Run all cells using Kernel → Restart & Run All


📌 Notes

The dataset is perfectly balanced across industries and countries (3,000 companies per industry; 3,750 per country), which is ideal for unbiased comparative analysis.
North America represents 50% of all records, so regional trends should be interpreted with this skew in mind.
All correlation coefficients are near zero, suggesting that business performance is multifactorial and cannot be attributed to a single variable — advanced modelling (clustering, regression) is recommended for deeper insights.

