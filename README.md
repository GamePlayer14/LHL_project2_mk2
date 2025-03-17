# **Final Project: Statistical Modeling with Python**

## **Project Overview**
This project aimed to determine if there is a correlation between **bike availability** at bike-sharing stations and surrounding location factors such as **distance to points of interest (POIs) and business ratings**. The goal was to test this hypothesis using data from **CityBikes**, **Yelp**, and **Foursquare APIs** and apply a **linear regression model** to see if these features could predict bike availability.

## **Process**
1. **Data Acquisition**
   - Collected **bike station data** from the **CityBikes API**.
   - Retrieved **restaurant and bar data** from **Yelp** and **Foursquare**.
   - Merged datasets using **station names**.
   - Stored the processed data in an **SQLite database** for analysis.

2. **Exploratory Data Analysis (EDA)**
   - Checked for **missing values**, **duplicates**, and **naming inconsistencies**.
   - Created **visualizations** for bike availability, distances, and ratings.
   - Used **correlation heatmaps** to explore relationships between features.

3. **Statistical Modeling**
   - Built a **linear regression model** to test the relationship between `Distance`, `Rating`, and `Free Bikes`.
   - Used **Ordinary Least Squares (OLS) regression** from `statsmodels`.
   - **Evaluated model performance** using R² scores and residual analysis.

## **Results**
- **R² Score ≈ 0.000** → The model found **no correlation** between `Distance`, `Rating`, and `Free Bikes`.
- **p-values > 0.05 for all predictors** → Neither `Distance` nor `Rating` had a statistically significant effect.
- **Regression residuals showed no meaningful patterns**, confirming the model's poor fit.
- **Conclusion:** No statistical correlation was found between bike availability and the selected location factors.

## **Challenges & Key Takeaways**
- **Finding Meaningful Features:** The initial assumption that POI distance and rating would impact bike availability turned out to be incorrect.
- **API Limitations:** Station name inconsistencies made data merging difficult.
- **Data Structuring:** SQLite helped manage the data, but the selected features were not useful predictors.

## **Future Directions**
- **Test Other Variables:** Consider time-based patterns (rush hour), weather conditions, or station size.
- **Try Alternative Models:** Clustering or decision trees may uncover non-linear relationships.
- **Focus on Usage Trends:** Instead of prediction, analyze high-usage vs. low-usage stations.

## **Final Thoughts**
Although the model did not find a correlation, this project successfully explored **data acquisition, EDA, database management, and regression analysis**. The biggest takeaway is that **feature selection is critical**, and future work should focus on **better predictors of bike availability**.

