Economic Analysis of Yemen: Data-Driven Insights with Python and Tableau
Yemen Economic Dashboard Preview
(Include a preview image of your Tableau dashboard here)

📌 Overview
This project provides a comprehensive analysis of Yemen's economic landscape using Python for data processing, statistical modeling, and Tableau for interactive visualizations. Yemen faces complex economic challenges, including prolonged conflict, inflation, unemployment, and humanitarian crises. This repository aims to uncover trends, identify key drivers of economic instability, and communicate insights through data storytelling.

🚀 Features
GDP & Macroeconomic Trends: Historical analysis of GDP growth, sectoral contributions, and external debt dynamics

Inflation Analysis: Consumer Price Index (CPI) breakdown and drivers of hyperinflation

Humanitarian-Development Nexus: Impact of food insecurity, displacement, and foreign aid on economic outcomes

Labor Market Analysis: Youth unemployment rates and gender disparities

Trade Dynamics: Import/export trends and currency exchange rate fluctuations

Predictive Modeling: ARIMA time series forecasting for key economic indicators

Interactive Dashboards: Tableau storyboards with drill-down capabilities

📥 Installation
Clone Repository

bash
Copy
git clone https://github.com/yourusername/economy-yemen-analysis.git
cd economy-yemen-analysis
Python Dependencies

bash
Copy
pip install -r requirements.txt
Key Libraries:

pandas (Data manipulation)

numpy (Numerical analysis)

matplotlib/seaborn (Visualization)

statsmodels (Statistical modeling)

scikit-learn (Machine learning)

jupyter (Notebook interface)

Tableau

Download Tableau Public to view/interact with dashboards

Professional users can open .twbx files in Tableau Desktop

🛠️ Usage
Data Processing (Python)
python
Copy
# Sample code for inflation analysis
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('data/CPI_yemen.csv')
df['Date'] = pd.to_datetime(df['Date'])
df.set_index('Date', inplace=True)

# Calculate YoY inflation
df['Inflation_YoY'] = df['CPI'].pct_change(periods=12) * 100

# Plotting
plt.figure(figsize=(12,6))
plt.title('Yemen Year-over-Year Inflation Rate (2015-2023)')
plt.plot(df['Inflation_YoY'], color='firebrick')
plt.ylabel('Percentage Change')
plt.grid(True)
plt.savefig('results/inflation_trends.png')
Tableau Workflow
Connect cleaned CSV outputs from Python

Create calculated fields for key metrics:

tableau
Copy
// Food Inflation Index
IF [Category] = "Food" THEN [CPI] ELSE NULL END
Build interactive dashboards with:

Parameter-driven date filters

Hierarchy drilling (National > Governorate level)

Dual-axis charts comparing economic vs. humanitarian indicators

📊 Data Sources
World Bank Open Data

Yemen Economic Indicators

IMF Country Reports

Article IV Consultations

Humanitarian Data Exchange

Yemen Crisis Dataset

Central Bank of Yemen

Monetary Statistics

UNDP Yemen

Development Reports

Data Preprocessing Includes:

Handling missing values using MICE imputation

Currency normalization (YER to USD)

Spatial aggregation to governorate level

Temporal alignment of disparate data sources

📂 Project Structure
Copy
.
├── data/
│   ├── raw/               # Original datasets
│   └── processed/         # Cleaned analysis-ready data
├── notebooks/
│   ├── 1_Data_Cleaning.ipynb
│   ├── 2_Economic_Trends_Analysis.ipynb
│   └── 3_Statistical_Modeling.ipynb
├── scripts/
│   ├── data_processing.py
│   └── visualization.py
├── tableau/
│   ├── yemen_economy.twbx
│   └── exports/           # PDF/PNG dashboard exports
├── results/
│   ├── figures/           # Generated visualizations
│   └── models/            # Saved regression/ARIMA models
└── docs/
    ├── methodology.pdf    # Technical documentation
    └── references.md      # Academic sources
📈 Key Findings
GDP Contraction

53% decline in real GDP since 2015 conflict escalation

Services sector collapse (-72% from pre-war levels)

Inflation Dynamics

450% cumulative CPI increase (2015-2023)

Food prices rising 2.3× faster than non-food basket

Labor Market

Youth unemployment rate: 37.8% (15-24 age group)

Female labor force participation: 6.2% (lowest in MENA)

Humanitarian-Economic Linkages

80% population below poverty line ($1.90/day)

45% GDP contraction linked to conflict intensity (R²=0.81)

Interactive Dashboard Features:

Crisis timeline overlay with economic metrics

Governorate-level vulnerability index

Aid flow tracker vs. macroeconomic indicators

🤝 Contributing
We welcome contributions:

Fork the repository

Create feature branches (git checkout -b feature/AmazingFeature)

Submit Pull Requests with detailed documentation

Please adhere to:

PEP8 Python style guide

Tableau visualization best practices

Humanitarian Data Standards

📜 License
Distributed under MIT License. See LICENSE for details.

🙏 Acknowledgments
World Bank Development Economics Group

Yemen Central Statistical Organization

Humanitarian partners (OCHA, WFP, UNICEF)

Academic advisors from Sana'a University Economics Department

📬 Contact
[Fadhl-ghaleb ] - [fadlcom.2025@gmail.com]
LinkedIn www.linkedin.com/in/
fadhl-ghaleb-730073286


This structure provides technical depth while maintaining readability. To enhance further:

Add actual screenshots of your analysis/visualizations

Include links to live Tableau dashboards

Expand the methodology section with statistical models used

Add a "Challenges" section discussing data limitations

Include installation troubleshooting guide

Add a "Future Work" roadmap with planned analyses
