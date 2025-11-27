# CO₂ Emissions, GDP, HDI, Life Expectancy & Gender Inequality — Cross-Country Analysis

## Abstract
This project examines how countries’ **CO₂ emissions**, **Gross Domestic Product (GDP)**, **Human Development Index (HDI)**, **Life Expectancy**, and **Gender Inequality Index (GII)** are related.  
The aim is to understand whether industrial and economic growth lead to higher living standards and equality, or if they come at an environmental and social cost.  
Using open datasets and Python-based analysis, the project applies data cleaning, exploratory analysis, and correlation-based hypothesis testing to evaluate these relationships.  
After constructing a unified dataset for 2010–2019 and applying interpolation where necessary, a **clean 2019 cross-sectional dataset** is used for the analysis.

---

## Motivation
I chose this topic because I am genuinely interested in the connection between **economic growth, sustainability, and life expectancy**.  
While high-income countries often perform better in education, health, and living standards, they are also responsible for a large share of global CO₂ emissions.  
This led me to question whether **true development can occur without increasing environmental costs**, and whether sustainable countries can still achieve strong economic and social outcomes.  
This project helps me understand whether key global indicators—CO₂ emissions, GDP, HDI, life expectancy, and gender inequality—move together or diverge as countries develop.

---

## Objectives
1. Analyze the relationship between countries’ CO₂ emissions and GDP.  
2. Test whether higher GDP levels are associated with improvements in HDI and Life Expectancy.  
3. Examine if higher economic growth leads to more or less gender inequality.  
4. Compare economic, social, and environmental indicators across regions.  
5. Present findings through clear visualizations and statistical tests.

---

## Data Sources

All data are publicly available and ethically obtained.

| Dataset | Description | Source |
|----------|--------------|--------|
| CO₂ Emissions | Annual country-level CO₂ emission data |[Kaggle - CO₂ Emissions](https://www.kaggle.com/datasets/shreyanshdangi/co-emissions-across-countries-regions-and-sectors) |
| GDP (current US$) | Annual GDP values by country in current USD | [World Bank - GDP](https://data.worldbank.org/indicator/NY.GDP.MKTP.CD)  |
| Human Development Index (HDI) | HDI, Life Expectancy, GII | [UNDP / Kaggle](https://www.kaggle.com/datasets/shreyanshdangi/co-emissions-across-countries-regions-and-sectors) |

All datasets were merged using ISO3 country codes and aligned between **2010–2019**.

---

## Methodology

### Data Collection & Cleaning
- Collected datasets from official and publicly accessible sources.  
- Converted all datasets to consistent ISO3 country codes and year formats.  
- Removed regional aggregates such as “World”, “Europe & Central Asia,” etc.  
- **Interpolated missing values across 2010–2019** to address gaps in variables such as HDI, GII, and CO₂.  
- Merged all indicators into a unified panel dataset.  
- Extracted a **clean 2019 cross-sectional dataset** for hypothesis testing.  
- Saved the consolidated dataset as `master_cross_section.csv`.

### Exploratory Data Analysis
- Generated descriptive statistics (mean, median, variance, missing values).  
- Visualized distributions using histograms and kernel density plots.  
- Created correlation matrices and pairwise scatter plots for key variables.  
- Produced country-ranked bar charts (CO₂, HDI).  
- Compared continents using boxplots for CO₂ and HDI.  
- (Optional) Plotted global choropleth maps for CO₂ and HDI using Plotly.

### Statistical Testing
- Pearson and Spearman correlations were used to test the four main hypotheses.  
- Hypotheses were evaluated using the **clean 2019 cross-sectional subset** (complete cases).  
- Effect size, statistical significance, and expected directional relationships were considered.

---

## Hypotheses

| # | Hypothesis | Null Hypothesis (H₀) | Alternative Hypothesis (H₁) |
|---|-------------|-----------------------|-----------------------------|
| **1** | **CO₂–GDP Relationship** | CO₂ and GDP are not positively related. | Higher GDP is associated with higher CO₂ emissions. |
| **2** | **GDP–Life Expectancy Relationship** | GDP has no relationship with Life Expectancy. | Higher GDP increases Life Expectancy. |
| **3** | **GDP–Gender Inequality Relationship** | GDP has no effect on GII. | Higher GDP reduces GII. |
| **4** | **CO₂–HDI Relationship** | CO₂ emissions have no effect on HDI. | Higher CO₂ emissions reduce HDI. |

---

## Expected Findings
Originally, I expected:

- A clear **positive relationship** between GDP and CO₂ emissions.  
- A strong **positive link** between GDP and Life Expectancy.  
- **Lower gender inequality** (GII) in countries with higher GDP.  
- A **negative** relationship between CO₂ and HDI.

These expectations were only partially supported by the results.

---

## Results Summary
(See full results below.)

- **H1 (CO₂–GDP):** Weak but statistically significant positive correlation. GDP alone does not strongly predict CO₂.  
- **H2 (GDP–Life Expectancy):** Supported; positive relationship but influenced by high-income outliers.  
- **H3 (GDP–GII):** Not supported; gender inequality does not consistently decline with GDP.  
- **H4 (CO₂–HDI):** Not supported; CO₂ is not negatively related to HDI. Developed countries tend to show both high HDI and high emissions.

---

## Tools & Environment
- **Language:** Python  
- **Libraries:** pandas, numpy, seaborn, matplotlib, scipy, plotly  
- **Environment:** Google Colab  
- **Version Control:** GitHub  

---

## Ethical & AI Statement
All data sources are public and properly cited.  
AI tools were used only to improve clarity and structure, not for data manipulation or numerical analysis.  
All coding, cleaning, and statistical interpretation were conducted independently.

---

## Future Work
- Incorporating per-capita CO₂ and GDP variables for fairer comparisons.  
- Applying full panel-data methods (fixed effects) to use all years, not only 2019.  
- Adding renewable energy metrics, education indices, or carbon intensity variables.  
- Analyzing differences between OECD and non-OECD countries.  
