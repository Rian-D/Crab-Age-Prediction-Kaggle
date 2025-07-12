# Crab Age Prediction
My machine learning solution for the Kaggle Crab Age Prediction competition, earning me a leaderboard position of **#XXX** and a score of X.XXXXX (**top X%** of all submissions).

<!-- Add your leaderboard screenshot here -->

## Competition Overview
This project tackles the [Crab Age Prediction Kaggle Competition](https://www.kaggle.com/competitions/playground-series-s3e16/overview). The goal is to predict the age of crabs based on physical measurements including dimensions and weight components.

**Evaluation Metric:** Mean Absolute Error (MAE)


## Dataset Summary
- **Training Data:** 74,051 crabs with age measurements
- **Test Data:** 49,368 crabs (predictions needed for submission) 
- **Features:** 8 variables including length, diameter, height, and various weight measurements
- **Target:** Age (continuous variable)


## Methodology

### 1. Data Quality Assessment & Cleaning
- **Weight Inconsistency Fix:** Identified 7,110 rows where component weights (shucked + viscera + shell) exceeded total weight
- Applied proportional scaling to maintain physical constraints while preserving data
- Validation ensured all weight ratios became logically consistent

### 2. Feature Engineering Pipeline
- **Comprehensive Feature Creation:** XX new engineered features from 8 original measurements
- **Weight Proportion Analysis:** Calculated meat, shell, and viscera ratios (key biological indicators)
- **Morphological Ratios:** Length-to-diameter, height ratios for body shape characterization (I learnt about these through domain research)
- **Advanced Metrics:** Crab BMI, shell thickness, growth efficiency indicators

### 3. Feature Selection & Impact Testing
- **Individual Feature Analysis:** Tested each engineered feature's isolated contribution to MAE reduction
- **Cumulative Feature Addition:** Greedy forward selection to find optimal feature combinations
- **Feature Group Testing:** Evaluated features by biological relevance (shape ratios, weight proportions, etc.)
- **Performance Validation:** Cross-validation to ensure robust feature selection

### 4. Model Training & Validation
- Chose to use XGBoost as it is often the best for regression problems using tabular data
- Cross-validation for robust performance estimation


## Feature Engineering Details

**Created Features:**

**Body Shape Ratios:**
- Length_Diameter_Ratio: Overall body elongation
- Height_Length_Ratio: Body profile indicator
- Height_Diameter_Ratio: Cross-sectional shape

**Weight Proportions (Biological Indicators):**
- Meat_Ratio: Edible meat percentage (key maturity indicator)
- Shell_Ratio: Shell development percentage
- Viscera_Ratio: Internal organ proportion

**Advanced Morphological Metrics:**
- Body_Volume: Length × Diameter × Height (size proxy)
- Surface_Area: Calculated surface area for biological scaling
- Crab_BMI: Weight per unit length squared (condition indicator)
- Shell_Thickness: Shell weight relative to surface area

**Growth & Maturity Indicators:**
- Soft_Weight: Combined meat and viscera weight
- Meat_Shell_Ratio: Meat development relative to shell
- Weight_per_Length: Linear growth efficiency
- Shell_Development: Shell weight relative to body volume

**Why These Features Matter:**
- **Weight ratios** capture biological development patterns that correlate with age
- **Morphological ratios** reflect growth allometry in marine organisms
- **Volume and surface area** provide size-independent shape descriptors
- **Growth efficiency metrics** capture metabolic and developmental patterns


## Potential Improvements
- **Ensemble Methods:** Combine multiple regression algorithms optimised for biological data
- **Outlier Detection:** Identify and handle anomalies in training data
- **Domain-Specific Features:** Incorporate more advanced marine biology knowledge for additional feature engineering


## Key Insights
- **Weight ratios** proved more predictive than absolute measurements
- **Shell development metrics** showed strong correlation with crab age
- **Feature engineering** provided significant improvement over raw measurements
- **Data quality** correction was crucial for biological constraint satisfaction


## License
This project is licensed under the MIT License.

*This project was developed as part of the Regression with a Crab Age Dataset Kaggle competition to demonstrate machine learning techniques for biological regression problems.*
