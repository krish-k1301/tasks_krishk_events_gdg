# Task 1 – Exploratory Data Analysis (EDA) – Abalone Dataset

## Overview

This task focuses on performing Exploratory Data Analysis (EDA) on the Abalone dataset. The objective was to explore the data structure, clean inconsistencies, generate insights, engineer features, and prepare the dataset for future machine learning tasks.

## What I Understood

The dataset was relatively clean and easy to work with. There were no missing values, which made the cleaning process simpler. A few instances where **Height = 0** were identified as invalid entries and removed.

Using the **YData Profiling** library was helpful in automating much of the exploratory analysis. It generated detailed profiling reports that saved significant time and provided a strong starting point for deeper manual EDA.

## Steps Performed

1. Loaded the dataset and inspected columns, data types, and basic statistics.
2. Removed rows with height equal to zero.
3. Created a new feature:

   ```
   Lost weight = Weight − (Shucked Weight + Viscera Weight + Shell Weight)
   ```
4. Visualized distributions using KDE, box plots, scatter plots, and violin plots.
5. One-hot encoded the “Sex” column.
6. Standardized numeric features (excluding the one-hot encoded columns).
7. Generated a correlation heatmap to understand feature relationships.

## Key Insights

### Distribution Insights

* **Age** has a right-skewed distribution, with most abalones around 9–11 years old.
* **Length, Diameter, and Weight** also show right-skewed distributions reflecting natural biological variation.
* The engineered feature **Lost weight** shows subtle differences across sexes.

### Group-Based Differences

* From violin and box plots, **Infant (I)** abalones are generally younger and smaller across all metrics.
* **Male (M)** and **Female (F)** abalones share similar distributions in Age, Length, and Weight with minor variations in spread.
* **Lost weight** differs slightly across sex categories but without extreme separation.

### Relationship Insights

* Scatterplots (e.g., **Age vs Diameter**) show positive relationships, suggesting older abalones tend to be larger.
* Heatmap reveals strong correlations among structural measurements:

  * Length, Diameter, Weight, Shell Weight, and Shucked Weight scale closely together.
* Age has weaker correlations with most features, implying multiple biological factors contribute to age prediction.

## Files Included in This Branch

* `KrishK_GDG_Task1.ipynb` – Full code and visualizations
* `README.md` – Task summary and documentation

## Conclusion

Task 1 provided a solid understanding of the dataset and prepared it for machine learning workflows. Through profiling, visualization, feature engineering, and scaling, the dataset is now clean, well-understood, and ready for modeling in future tasks.
