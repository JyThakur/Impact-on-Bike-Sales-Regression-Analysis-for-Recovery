## **Introduction**  
This project analyzes a dataset from a US-based bike-sharing company containing **730 days of rental records** (2018-2019). The data includes features like weather conditions (`temp`, `hum`, `windspeed`), temporal variables (`season`, `month`, `weekday`), and usage metrics (`casual`, `registered`, `cnt`). The goal is to understand patterns in bike rental demand and build a predictive model to help the company optimize operations and recover from pandemic-related losses.  

---

## **Objective**  
1. **Identify key factors** influencing bike rental demand.  
2. **Develop a predictive model** to forecast daily bike rentals (`cnt`).  
3. **Provide actionable insights** to improve business strategies and mitigate future losses.  

---

## **Steps Conducted**  
1. **Data Cleaning & Preprocessing**  
   - Removed irrelevant columns (`instant`, `dteday`).  
   - Handled multicollinearity by dropping correlated features (`atemp`, `casual`, `registered`).  
   - Encoded categorical variables (`season`, `month`, `weathersit`).  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized relationships between features and target variable (`cnt`).  
   - Identified higher demand in **summer/fall** and lower demand during **bad weather**.  

3. **Feature Engineering**  
   - Scaled numerical features (`temp`, `hum`, `windspeed`) using Min-Max scaling.  
   - Created dummy variables for categorical features.  

4. **Model Building (Linear Regression)**  
   - Used **Recursive Feature Elimination (RFE)** to select significant predictors.  
   - Optimized the model by removing features with **high VIF** and **insignificant p-values**.  
   - Final model included **10 key features** (e.g., `yr`, `windspeed`, `spring`).  

5. **Model Evaluation**  
   - Achieved **R² scores**: **0.79 (train)** and **0.76 (test)**.  
   - Residual analysis confirmed **normally distributed errors**.  

---

## **Results**  
- **Key Findings**:  
  - **Higher demand in 2019** vs. 2018 (post-pandemic recovery potential).  
  - **Summer/Fall months** (March–September) had peak rentals.  
  - **Bad weather** (snow/rain) significantly reduced demand.  
- **Business Recommendations**:  
  - **Increase promotions during peak seasons**.  
  - **Offer weather-based discounts** to maintain rentals in adverse conditions.  

---

## **Conclusion**  
The Linear Regression model successfully identified **weather, seasonality, and year** as major drivers of bike rentals. By leveraging these insights, the company can **optimize pricing, marketing, and inventory** to recover from pandemic losses. Future improvements could explore **advanced models** (e.g., Random Forest) for better accuracy.  

**Tools Used:** Python, Pandas, Scikit-learn, Statsmodels, Matplotlib, Seaborn  
**Author:** Jay Thakur
