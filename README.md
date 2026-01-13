# Customer Churn Analysis

## 🧠 **Business Scenario**

A mid‑sized B2B digital services provider has noticed a decline in contract renewals.
Leadership suspects churn is driven by:
- Low customer engagement
- High acquisition costs
- Industry‑specific retention challenges
- Differences between customer types
  
The company wants:

- A clear understanding of churn drivers
- A financial estimate of revenue lost to churn
- A predictive model to identify at‑risk customers
- Actionable insights to guide retention strategy

## 🚀 **Project Overview**

This repository delivers a complete churn analytics workflow for a digital services company seeking to understand:

- Why customers churn
- Which segments are most at risk
- How churn impacts revenue
- Which features predict churn most strongly

## 📁 **Dataset**
The dataset contains customer records from a digital services provider with variables such as:
- Contract status (extended or not → churn)
- Customer Lifetime Value (CLV)
- Customer type (e.g., SME, Enterprise, etc.)
- Industry type
- Traffic / customer contacts (engagement)
- Cost per Click (CPC)
- Operating Income (OI)
- Other numeric and categorical customer attributes

- Source: Source: Proprietary business dataset supplied by the course professor.

## 🔧 **Tools & Libraries**
The analysis is performed in RStudio using:
- haven – import SPSS data
- dplyr – data manipulation and filtering
- ggplot2 – visualizations
- GGally – correlation and pair plots
- corrplot – correlation heatmaps
- gridExtra, grid – layout and table display
- DataExplorer – quick data exploration

  
## 📊 **Analysis Step**

**1. Data Loading & Exploratory Analasysis**
- Import the SPSS dataset using haven::read_sav()
- Inspect:
- Number of rows and columns
- Variable types (numeric, categorical, logical)
- Presence of missing values
- Basic metadata and distributions
This ensures the dataset is clean, consistent, and ready for modeling

**2.  Churn Setup**
- Create churn indicators:
- churn (logical TRUE/FALSE)
- churn_numeric (0/1)
- churn_label (“Churned” / “Retained”)
- Generate a churn summary table:
- Number of churned vs retained customers
- Overall churn rate (%)
- Total customer count
This establishes the foundation for all downstream analysis.

**3. CLV (Customer Lifetime Value) Analysis**
- Convert CLV to numeric
- Produce a boxplot comparing CLV between churned and retained customers
- Compute the correlation between CLV and churn
This step evaluates how long‑term customer value relates to churn behavior.

**4. Customer Type Analysis**
- Convert cust_type to a factor
- Create a proportional bar chart showing churn distribution across customer types
This highlights which customer segments are most at risk.

**5. Industry Type Analysis**
- Convert industry_type to a factor
- Visualize churn proportions across industries
This identifies industry verticals with elevated churn risk and informs segment‑specific strategies.

**6. Engagement Analysis (Traffic Model)**
- Convert Traffic_customercontacts_avg to numeric
- Fit a logistic regression model:
- churn_numeric ~ Traffic_customercontacts_avg
- Generate predicted churn probabilities across a traffic range
- Plot traffic volume vs predicted churn probability
This quantifies how customer engagement influences churn likelihood.

**7. CPC (Cost per Click) Analysis**
- Convert CPC to numeric
- Create a boxplot comparing CPC for churned vs retained customers
This assesses whether acquisition cost efficiency is linked to churn.

**8. Correlation Analysis**
- Select all numeric variables
- Compute:
- Pearson correlations with churn
- Spearman correlations with churn
- Rank features by absolute Spearman correlation
- Visualize the top 10 churn‑related features
This step identifies the strongest statistical drivers of churn.

**9. Financial Impact Assessment**
- Calculate total yearly operating income (OI)
- Estimate revenue lost due to churn:
- revenue_churn = churn_rate × total OI
- Print financial impact metrics
This quantifies the business cost of churn and supports ROI calculations for retention initiatives.

**10. Predictive Modeling**
- Ensure categorical variables (industry_type, cust_type) are factors
- Build a clean modeling dataset (remove missing values)
- Fit a logistic regression model using:
- CPC
- CLV
- Industry type
- Customer type
- Interpret model coefficients and significance, Refine the model by eliminating variables that do not show statistical significance. 

**11. Business Report**
