# Kickstarter Campaign Success Prediction

## Project Overview
This project focuses on developing a machine learning model to predict the likelihood of success for Kickstarter campaigns based on data available at launch. The motivation stems from enabling project creators to understand key success factors early on and optimize their project plans. Additionally, the model can aid backers in identifying promising campaigns to support.

The Kickstarter dataset used contains 20K+ records of historical campaigns across countries and categories. Each record has 68 features covering details like goal amount, duration, number of backers, location, rewards, genre, etc. The target variable is the success status of reaching the funding goal.

The project methodology involves exploratory analysis, feature engineering, model evaluation with algorithms like XGBoost and Random Forest, followed by optimization and ensembling to improve predictive performance. Feature importances are analyzed to understand key success drivers.

The results demonstrate high accuracy in classifying successful campaigns, with the best model achieving 98% test accuracy. The insights can help creators refine project scopes, set realistic goals, offer attractive rewards, and boost promotional efforts. For backers, the model provides data-driven guidance for deciding which campaigns to back.

## Goals and Objectives
The key goals and objectives of this project are:
- Perform exploratory analysis on Kickstarter data to extract insights
- Engineer new features like project duration, reward tiers, text vectors etc.
- Evaluate performance of ML models like SVM, Logistic Regression, Random Forest, XGBoost etc.
- Tune hyperparameters and ensemble models to maximize classification accuracy
- Analyze feature importances to understand predictors of success
- Incorporate economic factors like GDP growth to add context
- Generate actionable insights and recommendations for project creators and backers

## Datasets Used
The main dataset is obtained from Kaggle, containing details on 20,000+ Kickstarter campaigns. Each record has 68 attributes covering:
- Basic info: name, genre, goal amount, launch date, location etc.
- Duration: deadline, campaign duration
- Funding outcomes: pledged amount, number of backers
- Rewards: number of reward levels offered
- Campaign text: name, blurb, campaign URL
- Status: whether goal was met (target variable)

Supplementary GDP data from World Bank is used to understand macroeconomic trends.

## Methodology and Techniques
The systematic methodology followed includes:
- Data Cleaning: Handling missing values, duplicates, formatting errors
- Exploratory Analysis: Univariate distribution, correlations, clustering
- Feature Engineering: Extracting reward tiers, campaign duration, text vectors from raw features
- Feature Selection: Identifying predictive subset of features using decision trees
- Preprocessing: Label encoding, standardization, train-test split
- Modelling: Training Logistic Regression, SVM, Random Forest, XGBoost models
- Tuning and Ensembling: Optimizing hyperparameters through grid search, model stacking
- Evaluation: Comparing model performance using accuracy, precision, recall, F1-score

Key techniques employed:
- Supervised ML models: Regression, SVM, Ensembles (Random Forests, XGBoost, Bagging)
- Oversampling with SMOTE to handle class imbalance
- Dimensionality reduction using PCA
- Visualization for insights: histograms, heatmaps, scatter plots

## Key Findings and Results
The analysis yielded significant insights into Kickstarter success factors:
- Number of backers has very high correlation to success
- Higher funding targets tend to have lower success rates
- Campaigns with shorter durations are more likely to succeed
- Reward tiers and limited editions boost success chances
- Higher GDP results in increased funding, but trends shifted post-2015

The optimized XGBoost model obtained the best performance:
- Accuracy: 98.35%
- Precision: 98.89%
- Recall: 98.32%
- F1-score: 98.32%

## Conclusion and Recommendations
The models demonstrate reliable predictive capabilities for forecasting the success likelihood of proposed campaigns. Creators can leverage these insights to strategize their project planning and increase success odds.

Some actionable recommendations based on findings:
- Set feasible funding goals based on project scope and historical data
- Limit campaign duration to around 1 month
- Structure attractive reward tiers and limited editions
- Promote aggressively in first week to gain early traction
- Consider economic climate when estimating funding potential

There are several avenues for future work, such as incorporating social media data, longitudinal trends, and testing model portability across platforms. Overall, this project provides data-driven guidance for key stakeholders in crowdfunding campaigns.
