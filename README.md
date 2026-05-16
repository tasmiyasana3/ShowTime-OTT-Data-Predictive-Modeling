# Predictive Modelling, OTT Content Viewership Analysis

## Project Overview
This project analyzes the main factors that affect first-day content viewership on the ShowTime OTT platform using Linear Regression.

The study looks at how variables like trailer engagement, ad impressions, release timing, genres, seasons, platform traffic, and major sports events impact content performance on the first day.

The project includes:
- Exploratory Data Analysis (EDA)
- Data preprocessing
- Outlier treatment
- Feature engineering
- Linear regression modeling
- Assumption testing
- Model performance evaluation
- Business insights and recommendations

---

## Business Problem
OTT platforms rely on audience engagement and successful content launches. Knowing what drives first-day viewership helps improve:
- Release schedules
- Marketing strategies
- Trailer campaigns
- Genre targeting
- Seasonal release planning

This project's goal is to find the most important factors affecting first-day content views and create a predictive model to estimate content performance.

---

## Dataset Information
The dataset includes 1,000 observations with 8 features related to OTT content performance.

### Features Used
- `visitors` — Weekly platform visitors (millions)
- `ad_impressions` — Advertisement impressions (millions)
- `major_sports_event` — Major sports event presence (0/1)
- `genre` — Content genre
- `dayofweek` — Release day
- `season` — Release season
- `views_trailer` — Trailer views (millions)
- `views_content` — First-day content views (target variable)

---

## Technologies & Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Scikit-learn
- Jupyter Notebook

---

## Exploratory Data Analysis (EDA)

### Key Findings
- Trailer views had a strong positive correlation with first-day content views (r ≈ 0.75).
- Major sports events negatively affected content performance.
- Saturday and Wednesday releases did better on average.
- Summer and Winter seasons generated higher engagement.
- Sci-Fi, Horror, and Thriller genres had stronger first-day performance.
- Ad impressions alone provided very weak predictive power.

---

## Data Preprocessing
We performed several preprocessing steps:

### Data Cleaning
- No missing values were found.
- No duplicate records were detected.

### Outlier Treatment
- Winsorization was applied to:
  - `visitors`
  - `ad_impressions`
- Log transformation was applied to:
  - `views_trailer`
- We retained outliers in the target variable to keep real-world business scenarios intact.

### Feature Engineering
- We created additional features from genre-related information.
- We applied dummy encoding for categorical variables.

---

## Model Building

### Baseline Model
We developed a Linear Regression model to predict:
- `views_content`

### Regression Assumption Testing
We tested several assumptions:
- Multicollinearity (VIF)
- Linearity
- Normality of residuals
- Homoscedasticity
- Residual independence

### Model Refinement
We removed features with high p-values and multicollinearity to improve clarity and statistical significance.

---

## Model Performance
The final regression model showed strong predictive performance with:
- A high R² score
- Stable residual behavior
- Reduced multicollinearity
- Improved clarity

The model identified trailer engagement as the strongest predictor of first-day content performance.

---

## Business Insights

### Trailer Engagement Drives Success
- Trailer views were the most important predictor of content performance.
- Strong trailer campaigns greatly improved launch-day engagement.

### Release Timing Matters
- Saturday and Wednesday releases achieved higher average views.
- Friday had the highest number of releases but lower average performance.

### Sports Events Reduce Engagement
- Major sports events negatively affected first-day viewership.
- Avoiding large sports-event days could boost launch success.

### Seasonal Trends Exist
- Summer and Winter seasons showed the highest audience engagement.
- Fall releases performed worse by comparison.

### Genre Performance
- Sci-Fi, Horror, and Thriller genres had better first-day conversion rates.
- Romance and Comedy genres showed lower engagement.

---

## Business Recommendations
- Increase investment in trailer marketing campaigns.
- Schedule flagship releases during Summer and Winter.
- Prefer Saturday and Wednesday for launches.
- Avoid release dates that coincide with major sports events.
- Focus on genres that perform well for premium content launches.

---

## Project Structure
- `PM_BusinessReport_TS compressed.pdf` — Detailed business report
- `PredictiveModeling_Project_TS.ipynb` — Full Python implementation
- `ottdata.csv` — Dataset csv file
- `README.md` — Project documentation

---

## Author
Tasmiya Sana

---

## Conclusion
This project shows how predictive modeling and statistical analysis can help OTT platforms improve content release strategies and boost audience engagement. By identifying key performance drivers, the analysis supports data-driven decision-making for digital streaming platforms.
