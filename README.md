# 📊 Trends in Fruit and Vegetable Affordability: A Cost Analysis Over Time

This project analyzes the **USDA Economic Research Service (ERS) Fruit and Vegetable Prices dataset**, focusing on retail price changes of over 150 fresh and processed items in the U.S. across 2013, 2016, 2020, and 2022. The study examines whether fruits and vegetables have become more or less affordable over time, with attention to the impact of the COVID-19 pandemic period on price fluctuations.


## 📖 Overview

- **Goal**: Assess affordability trends of fruits and vegetables and their implications for food security and dietary access.  
- **Dataset**: USDA ERS — retail scanner data from grocery stores, supermarkets, and convenience stores.  
- **Scope**: Price trends, statistical testing (ANOVA, regression), and model diagnostics to determine significance of cost changes over time.  


## 📂 Project Structure
```
Fruits-and-Vegetables-Affordability/
├── Project.Rmd                # Main RMarkdown analysis
├── Project.html               # Knit HTML file
├── Report.docx                # Narrative report with results & visuals
├── data/                      # Source data files 
│   ├── ProjectData.xlsx
│   ├── Fruits_Retail_Cost.xlsx
│   ├── Veg_Retail_Cost.xlsx
│   ├── Fruits_Retail_Cost_reshaped.xlsx
│   └── Veg_Retail_Cost_reshaped.xlsx
├── plots/
│   ├── Fruit_2013_Barplot.png
│   ├── Fruit_2016_Barplot.png
│   ├── Fruit_2020_Barplot.png
│   ├── Fruit_2022_Barplot.png
│   └── Vegetable_2013_Barplot.png
│   └── Vegetable_2016_Barplot.png
│   └── Vegetable_2020_Barplot.png
│   └── Vegetable_2022_Barplot.png
└── README.md
```


## ⚙️ Requirements

Install R (≥ 4.0) and the following R packages:

```r
install.packages(c("tidyverse", "ggplot2", "dplyr", "readr", "knitr", "rmarkdown"))
```


## ▶️ How to Run
1. Open `Project.Rmd` in **RStudio** and run all chunks.
2. Use `Project.html` to review pre-conducted analysis.


## 📊 Analysis Workflow
- **Data Cleaning** – Separate fruit and vegetable datasets, reshape wide → long format.
- **Descriptive Statistics** – Summary tables for mean, quartiles, min/max prices.
- **Visualization** – Boxplots and line graphs showing price distributions and trends.
- **Statistical Tests**:
  - ANOVA → initial test (no significant mean differences across years, p > 0.05).
  - Linear Regression → stronger evidence of significant price trends (R² = 69.6% fruits, 78.8% vegetables).
- **Model Diagnostics** – Normality testing (Shapiro-Wilk, Q-Q plots), residual-leverage plots.


## 📈 Key Insights
- **Overall Increase**: Prices for fruits rose ~22.7% from 2013–2022; vegetables rose ~19.5%.
- **Pandemic Spike**: Largest jumps between **2020 → 2022** for both fruits and vegetables.
- **Fruits vs Vegetables**: Fruits show wider price disparities (e.g., dried papaya +63%) compared to vegetables.
- **Statistical Evidence**:
  - ANOVA suggested no significant average differences across years.
  - Regression models confirmed significant time trends, with vegetables showing stronger explanatory power.
- **Limitations**: Residuals deviated from normality, suggesting transformations or robust regression could improve model reliability.


## 📜 License
MIT License © Harsh Patel


## 🙌 Acknowledgments
- Dataset: [USDA Economic Research Service — Fruit and Vegetable Prices](https://www.ers.usda.gov/data-products/fruit-and-vegetable-prices)
- Conducted as part of **Data Analysis and Visualization 2 (Sheridan College)** course project under **Professor Farah Huassien** guidance.
