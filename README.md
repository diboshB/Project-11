# Project-11
Capstone_Project - Regression - Insurance premium prediction

1. Introduction
Health insurance premium prediction is a crucial task in the insurance
industry as it helps both insurance companies and policyholders make
informed decisions. Predicting accurate premiums is essential for risk
assessment and ensuring that policyholders pay premiums that reflect their
health risks. In this project, the goal is to predict health insurance premiums
in the United States based on various personal and health-related factors,
such as age, BMI, smoking status, medical history, and others. A Linear
Regression model was chosen due to its simplicity and interpretability in
regression tasks. The dataset includes 10 variables related to the individual's
demographics and health behaviors, with the target variable being the
insurance premium charges.
2. Data Collection
The dataset used for this project contains various attributes influencing the
cost of health insurance premiums in the U.S. The features include:
• Age: The age of the individual.
• Gender: The gender of the individual (Male/Female).
• BMI (Body Mass Index): A measure of body fat based on height and
weight.
• Children: The number of children/dependents covered by the
insurance.
• Smoker: Whether the individual is a smoker (Yes/No).
• Region: The region in which the individual resides (northeast,
northwest, southeast, southwest).
• Medical History: The individual's medical history (e.g., diabetes,
hypertension, etc.).
• Family Medical History: The family history of medical conditions
(e.g., heart disease, diabetes).
• Exercise Frequency: How often the individual exercises (Never,
Occasionally, Rarely).
• Occupation: The individual's job type (e.g., White collar, Blue collar).
• Coverage Level: The type of insurance coverage (Standard,
Premium).
• Charges: The target variable representing the health insurance
premium amount.
The dataset was loaded into a Pandas DataFrame, and preprocessing steps
were carried out to clean and prepare the data for modeling.
3. Data Preprocessing
Several preprocessing steps were performed to prepare the data for the
Linear Regression model:
3.1 Handling Missing Values
The dataset was checked for missing values. Any rows containing missing
values were filled with 0, and no significant missing values were found in the
columns after preprocessing.
3.2 Data Type Conversion
Columns were converted to appropriate data types:
• Numeric Columns (e.g., age, bmi, children, charges) were converted
to float or int.
• Categorical Columns (e.g., gender, smoker, region, medical history)
were converted to category data type to optimize memory usage and
processing.
3.3 One-Hot Encoding
Categorical variables were transformed into numerical values using one-hot
encoding. This approach helps in converting non-numeric categories into
binary format suitable for machine learning algorithms. The first category of
each feature was dropped to avoid multicollinearity.
3.4 Feature Engineering
• A new feature, BMI Category, was created by categorizing BMI
values into bins (Underweight, Normal, Overweight, Obese). This
transformation was useful for better representing the BMI variable for
prediction.
• One-Hot Encoding was applied to the newly created BMI category to
integrate it with the rest of the features.
3.5 Feature Scaling
No feature scaling was applied as Linear Regression is generally not sensitive
to feature scales. However, it's a good practice to standardize features when
using more complex models.
4. Model Building
The goal was to build a predictive model that estimates health insurance
premiums based on the input features. The steps involved in building the
model are as follows:
4.1 Splitting the Dataset
The dataset was split into features (X) and target variable (y, which is the
charges/insurance premium). The data was then split into training and
testing sets using an 80-20 ratio.
4.2 Training the Model
A Linear Regression model was trained on the training data. Linear
regression was chosen for its simplicity and interpretability, as it provides
insights into how each feature influences the target variable (charges).
4.3 Making Predictions
Once the model was trained, it was used to make predictions on the test set.
The predicted premiums were then compared to the actual premium values
to evaluate the model's performance.
5. Model Evaluation
The model’s performance was evaluated using several key metrics to assess
its predictive accuracy:
• Mean Squared Error (MSE): A measure of the average squared
difference between the predicted and actual values.
• Mean Absolute Error (MAE): The average of the absolute
differences between the predicted and actual values.
• Root Mean Squared Error (RMSE): The square root of the MSE,
providing a more interpretable measure of prediction error.
• R-Squared (R²): A metric indicating the proportion of variance in the
target variable (charges) that is explained by the features.
5.1 Performance Metrics
The evaluation metrics on the test set were as follows:
• Mean Squared Error (MSE): 136,042.26
• R-Squared (R²): 0.9930
• Mean Absolute Error (MAE): 292.86
• Root Mean Squared Error (RMSE): 368.84
These metrics indicate that the model is performing quite well, explaining
over 99% of the variance in the target variable, with a relatively low error
rate.
6. Results & Discussion
6.1 Model Performance
The Linear Regression model performed excellently with an R² value of
0.9930, meaning that 99.3% of the variation in insurance premiums was
explained by the input features. The RMSE of 368.84 suggests that the
model's predictions are reasonably close to the actual charges, with a slight
deviation. However, there's always room for improvement.
6.2 Feature Importance
Linear regression provides insight into the importance of each feature
through its coefficients. The top features contributing to the prediction of
health insurance premiums were:
• Age: Older individuals generally pay higher premiums.
• BMI: Higher BMI values lead to higher premiums due to associated
health risks.
• Smoker Status: Smokers pay higher premiums compared to non-
smokers due to higher health risks.
• Medical History: Having pre-existing medical conditions like diabetes
increases the premium.
• Number of Children: Individuals with more children tend to have
higher premiums due to higher family healthcare costs.
These features significantly influenced the predicted premiums, and
understanding their relationships with the target variable can help optimize
insurance policies.
7. Conclusion
This project successfully demonstrated the use of Linear Regression to
predict health insurance premiums in the U.S. The model performed well
with an R² of 0.9930, indicating that it could explain most of the variance
in insurance premiums. The key features influencing the predictions were
age, BMI, smoking status, and medical history. Further improvements could
be made by exploring more advanced algorithms like Random Forests or
Gradient Boosting, or by tuning hyperparameters for better accuracy.
