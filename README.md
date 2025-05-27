## EDA Steps
### Analyzed Feature Distributions:
Plotted histograms with KDE for all numerical features.
Found Calories was heavily right-skewed; Age and Body_Temp had mild skewness; others were near-normal after standardization.

### Checked Relationships:
Used a correlation matrix to find relationships with Calories.
Duration (0.96), Heart_Rate (0.89), and Body_Temp (0.84) were strong predictors.
Height and Weight had high correlation (0.88), indicating multicollinearity.

### Feature Interactions:
Plotted Duration vs Heart_Rate (colored by Calories) and saw that higher values of both led to higher Calories.
Added Exercise_Intensity (Duration * Heart_Rate) as a new feature.

### Analyzed Sex_male:
Used a boxplot to compare Calories by Sex_male. Males burned slightly more calories on average.

### Feature Engineering:
Added BMI (from Height and Weight) and Exercise_Intensity.
Dropped Height and Sex_Weight due to high correlations with Weight (0.88) and Sex_male (0.67).

### Prepared for Modeling:
Standardized Calories to address skewness.
Confirmed all features were standardized and ready for a neural network.

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn
