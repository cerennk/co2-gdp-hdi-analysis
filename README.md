# CO₂ Emissions, GDP, HDI, Life Expectancy & Gender Inequality — Cross-Country Analysis

## Abstract
This project examines how countries’ **CO₂ emissions**, **Gross Domestic Product (GDP)**, **Human Development Index (HDI)**, **Life Expectancy**, and **Gender Inequality Index (GII)** are related. The aim is to understand whether industrial and economic growth lead to higher living standards and equality, or if they come at an environmental and social cost. Using open datasets and Python-based analysis, the project applies data cleaning, visualization, statistical testing, and regression modeling to identify significant relationships between these key indicators.

---

## Motivation
I chose this topic because I am genuinely interested in the connection between **economic growth, sustainability, and life expectancy**. While high-income countries often perform better in education, health, and living standards, they are also responsible for a large share of global CO₂ emissions. This led me to question whether **true development can occur without increasing environmental costs**, and if sustainable countries can still maintain strong economic and social outcomes. Through this project, I aim to explore whether **CO₂ emissions might be inversely related** to human development and equality — meaning that nations with lower emissions could still achieve high HDI and longer life expectancy. The project brings together my interests in **economics, sustainability, and data science**, and helps me strengthen my analytical skills by working with real, multi-source global datasets.


---

## Objectives
1. Analyze the relationship between countries’ CO₂ emissions and GDP.  
2. Test whether higher GDP levels are associated with improvements in HDI and Life Expectancy.  
3. Examine if higher economic growth leads to more or less gender inequality.  
4. Compare how economic and environmental indicators together reflect development levels across countries.  
5. Present findings through clear visualizations and statistical models.

---

## Data Sources
All data are publicly available and ethically obtained.

| Dataset | Description | Source |
|----------|--------------|--------|
| CO₂ Emissions | Annual country-level CO₂ emission data | (https://www.kaggle.com/datasets/shreyanshdangi/co-emissions-across-countries-regions-and-sectors) |
| GDP (current US$) | Annual GDP values by country in current USD | (https://data.worldbank.org/indicator/NY.GDP.MKTP.CD) |
| Human Development Index (HDI) | Composite measure combining education, health, and income | (https://www.kaggle.com/datasets/iamsouravbanerjee/human-development-index-dataset) |
| Life Expectancy | Average life expectancy at birth by country | (https://www.kaggle.com/datasets/iamsouravbanerjee/human-development-index-dataset) |
| Gender Inequality Index (GII) | Measure of gender inequality in health, empowerment, and labor | (https://www.kaggle.com/datasets/iamsouravbanerjee/human-development-index-dataset)   | 

All datasets will be merged using ISO3 country codes and aligned between **2010–2024**.

---

## Methodology

### Data Collection & Cleaning
- Collect datasets from the listed official sources.  
- Convert to consistent country codes and year formats.  
- Remove regional aggregates such as “World” and “Europe & Central Asia.”  
- Handle missing or mismatched years with interpolation or deletion.  
- Normalize data where necessary using log transformations.  
- Merge datasets into a single combined dataset (`master_cross_section.csv`).

### Exploratory Data Analysis
- Generate descriptive statistics (mean, median, variance, etc.).  
- Visualize distributions using histograms and density plots.  
- Plot correlation matrices and pairwise scatter plots (CO₂–GDP–HDI–Life Expectancy–GII).  
- Compare continents and income groups using boxplots.

### Statistical Testing & Modeling
- Pearson and Spearman correlation tests for continuous variables.  
- Simple linear regressions:
  - `HDI ~ CO2_total`
  - `GDP ~ CO2_total`
  - `LifeExp ~ GDP`
  - `GII ~ GDP`
- Multiple regression models controlling for per-capita adjustments.  
- Check assumptions (normality, multicollinearity, residual analysis).

### Visualization & Reporting
- Correlation heatmaps and pairwise scatter plots.  
- Country-ranked bar charts and continent-level comparisons.  
- Optional geographical map of CO₂ and HDI using Plotly or GeoPandas.

---

## Hypotheses

| # | Hypothesis | Null Hypothesis (H₀) | Alternative Hypothesis (H₁) |
|---|-------------|-----------------------|-----------------------------|
| **1** | **CO₂–GDP Relationship** | There is no positive relationship between CO₂ emissions and GDP. | There is a **positive relationship** between CO₂ emissions and GDP — higher economic activity tends to increase emissions. |
| **2** | **GDP–Life Expectancy Relationship** | GDP has no significant relationship with Life Expectancy. | GDP and Life Expectancy are **positively related** — economic growth contributes to longer average lifespans. |
| **3** | **GDP–Gender Inequality Relationship** | Economic growth has no effect on Gender Inequality. | Higher economic growth has a **negative effect** on Gender Inequality — as GDP rises, inequality tends to decrease. |
| **4** | **CO₂–HDI Relationship** | CO₂ emissions have no significant impact on HDI. | CO₂ emissions are **negatively related** to HDI — countries with lower emissions tend to achieve higher development and living standards. |

---

## Expected Findings
- A positive correlation between GDP and CO₂ emissions, reflecting that higher economic activity usually increases emissions.  
- GDP expected to positively correlate with HDI and Life Expectancy.  
- Gender Inequality Index likely to decrease as GDP rises, suggesting that higher economic levels may support greater equality.  
- Overall, results are expected to show that **economic growth improves living standards but increases environmental costs**.

---

## Tools & Environment
- **Language:** Python 3.9  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scipy, statsmodels, scikit-learn, plotly  
- **Development Environment:** Jupyter Notebook / VS Code  
- **Version Control:** Git and GitHub  

---

## Ethical & AI Statement
All data sources are **publicly available** and properly cited.  
No private, sensitive, or scraped personal data is used.  
AI tools were used only for **documentation clarity and structure**, not for data manipulation or model building.  
All analysis and interpretation will be done independently by me.

---

## Future Work
- Add **per-capita** versions of CO₂ and GDP for fairer comparisons.  
- Extend analysis to **time-series** or **panel data** for long-term trends.  
- Include **renewable energy share**, **education index**, or **carbon intensity** variables.  
- Compare results regionally (OECD vs developing countries).
- Data availability and temporal coverage (2010–2024) may limit the number of comparable countries.”
---
