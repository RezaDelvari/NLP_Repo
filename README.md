# Hotel Review Analysis

## Overview
This project aims to analyze hotel reviews dataset to predict reviewer scores based on various factors such as reviewer nationality, review content, and hotel characteristics. The dataset contains information like average score, reviewer nationality, review word counts, nights stayed, etc. Additionally, the project involves Exploratory Data Analysis (EDA) to understand the distribution of data and identify patterns, followed by model development using Logistic Regression and Decision Tree algorithms.

## Dataset Description
The dataset consists of the following fields:

- Additional_Number_of_Scoring
- Average_Score
- Reviewer_Nationality
- Negative_Review
- Review_Total_Negative_Word_Counts
- Positive_Review
- Review_Total_Positive_Word_Counts
- Reviewer_Score
- Total_Number_of_Reviews_Reviewer_Has_Given
- Total_Number_of_Reviews
- Hotel_Address
- Leisure_Trip
- Nights_Stayed

## Data Preprocessing
Initially, duplicate rows in the dataset were identified and removed. The binary columns and non-numerical review columns were dropped for further analysis. A total of 13 numerical features were retained for the analysis.

## Exploratory Data Analysis (EDA)
EDA revealed several insights about the dataset:

- Majority of columns are heavily skewed to the right.
- Most reviewers have less than 8 total reviews given.
- Review word counts are mostly under 23.
- Most reviewers stay at the hotel for less than 3 days.
- The dataset spans over 3 years, from 2015 to 2017.

## Distribution of Target Column
The target column, which is Reviewer_Score, was found to be slightly imbalanced, with 57% good reviews and 43% bad reviews. This split also implies a base accuracy of 57% for blind guessing all reviews to be good.

## Model Development
Two models were developed:

1. **Logistic Regression**: Achieved a train accuracy of 71.1% and a test accuracy of 70.9%.
2. **Decision Tree**: Initially overfitted with a train accuracy of 100% and a test accuracy of 69.9%. The model was optimized using Grid Search, resulting in improved performance with a test accuracy of 75.8%.

## Conclusion
The project involved preprocessing the data, conducting EDA, and creating models to predict reviewer scores. The Decision Tree model with optimized parameters performed the best, achieving a test accuracy of 75.8%. Further optimization and model evaluation can be explored using techniques like PCA and Grid Search CV or Randomized Search CV. These approaches can improve model performance and interpretability.
