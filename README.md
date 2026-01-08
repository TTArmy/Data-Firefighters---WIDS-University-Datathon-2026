# Wildfires and Social Vulnerability: A Territorial Analysis Across the United States

## 📌 Project Overview
This project investigates the complex intersection between environmental hazards and socio-economic structures. By analyzing data from **962 territorial units (counties)** in the US, we explore how factors such as income inequality, digital poverty, and demographic vulnerability influence the impact of wildfires, measured by the burned area per 1,000 inhabitants.

The research moves beyond traditional firefighting metrics to examine how **Social Vulnerability** acts as a force multiplier for natural disasters.

---

## 🛠 Methodology
The analysis is structured into three distinct phases:

### Phase I: Descriptive Statistics
A comprehensive overview of the dataset, identifying:
* **Highly Skewed Distributions:** A small number of counties face extreme fire events ($max = 1331$ fires), while the median is much lower ($13$).
* **Economic Discrepancies:** Median household incomes range from approximately $26,000 to $160,000.
* **Data Transformation:** Applied log-transformation to variables like `acres_per_1000_people`, `median_income`, and `fires` to mitigate the effect of outliers.

### Phase II: Exploratory Data Analysis (EDA)
Using correlation matrices and multi-dimensional visualizations:
* **Digital Poverty & Risk:** A notable correlation between lack of internet access and fire exposure.
* **Material Exclusion:** Strong clusters of correlations between lack of vehicles, disabilities, and lower income levels.
* **Containment Dynamics:** Analysis suggests fire control effectiveness is driven more by local operational capacity than general socio-economic status.

### Phase III: Machine Learning Modeling
We employed advanced Ensemble methods to model non-linear relationships:
* **Regression Tree:** Provided an initial interpretability layer, identifying fire frequency as the primary split.
* **Random Forest ($R^2 \approx 0.49$):** Improved accuracy by capturing interactions between variables.
* **LightGBM ($R^2 \approx 0.55$):** Our best-performing model, utilizing gradient boosting to handle complex patterns.

---

## 🔍 Key Findings & Interpretability
We utilized **SHAP (SHapley Additive exPlanations)** to ensure model transparency.

* **Hazard vs. Vulnerability:** While the number of fires (`log_fires`) is the dominant predictor, socio-economic context dictates the severity.
* **The Income Effect:** Lower-income counties consistently show higher SHAP values for fire impact, suggesting lower recovery and prevention capacity.
* **Access to Resources:** Lack of internet and vehicle access are critical vulnerability markers.

---

## 🚀 Conclusions
Wildfire impact is a **socio-environmental** phenomenon. Effective disaster management must integrate:
1. **Environmental Management:** Outbreak control and fireline containment.
2. **Social Policy:** Addressing digital poverty and mobility limitations.
3. **Targeted Intervention:** Strengthening response capacities in counties with high Gini indices.
