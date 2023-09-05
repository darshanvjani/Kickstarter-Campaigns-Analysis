# Kickstarter Campaign Success Prediction
<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/wordcloud_auto_x2.jpg?raw=true"/></p>

- [Presentation Desk](https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/CMPE257_Project_Presentation.pdf)

## Project Overview
This project focuses on developing a machine learning model to predict the likelihood of success for Kickstarter campaigns based on data available at launch. The motivation stems from enabling project creators to understand key success factors early on and optimize their project plans. Additionally, the model can aid backers in identifying promising campaigns to support.

The Kickstarter dataset used contains 20K+ records of historical campaigns across countries and categories. Each record has 68 features covering details like goal amount, duration, number of backers, location, rewards, genre, etc. The target variable is the success status of reaching the funding goal.

The project methodology involves exploratory analysis, feature engineering, model evaluation with algorithms like XGBoost and Random Forest, followed by optimization and ensembling to improve predictive performance. Feature importances are analyzed to understand key success drivers.

The results demonstrate high accuracy in classifying successful campaigns, with the best model achieving 98% test accuracy. The insights can help creators refine project scopes, set realistic goals, offer attractive rewards, and boost promotional efforts. For backers, the model provides data-driven guidance for deciding which campaigns to back.

## Goals and Objectives
The key goals and objectives of this project are:
- Perform exploratory analysis on Kickstarter data to extract insights
- Engineer new features like project duration, reward tiers, text vectors etc.
- Evaluate performance of ML models like SVM, Logistic Regression, Random Forest, XGBoost, Catboost etc.
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

Supplementary GDP data from World Bank is used to understand **macroeconomic trends**.

## Methodology and Techniques
The systematic methodology followed includes:
- Data Cleaning: Handling missing values, duplicates, formatting errors
- Exploratory Analysis: Univariate distribution, correlations, clustering
- Feature Engineering: Extracting reward tiers, campaign duration, text vectors from raw features
- Feature Selection: Identifying predictive subset of features using decision trees
  
<p align="center">
  <img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/selected_features.PNG?raw=true"/>
</p>
- Preprocessing: Label encoding, standardization, train-test split

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/data_preprocess_flowchart.png?raw=true"/></p>
- Modelling: Training Logistic Regression, SVM, Random Forest, XGBoost models
- Tuning and Ensembling: Optimizing hyperparameters through grid search, model stacking (voter classifier)
- Evaluation: Comparing model performance using evaluation metrics with models trained on different data sample stratifies (SMOTE, ADASYN)

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/main_flowchart.png?raw=true"/></p>

Key techniques employed:
- Supervised ML models: Regression, SVM, Ensembles (Random Forests, XGBoost, Bagging)
- Oversampling with SMOTE to handle class imbalance
- Dimensionality reduction using PCA for feature importance

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/pca.png?raw=true"/></p>

- Visualization for insights: histograms, heatmaps, scatter plots, word cloud

## Key Findings and Results
The analysis yielded significant insights into Kickstarter's success factors:
- The Success Rate depends highly on the founding team.

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/num_proj_vs_successful_proj.png?raw=true"/></p>

- Certain category has a high success rate then others

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/success_rate_by_category.png?raw=true"/></p>
  
- Increase in funding doesn't always mean higher success rate for early-stage startups

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/temporal_trends_funding_successrate.png?raw=true"/></p>
  
- Top 3 categories having 80% pledge money allocation

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/top_4_category_80pr_pledge.png?raw=true"/></p>
  
- Funds Received by each founder and team

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/top_funding_each_creator.png?raw=true"/></p>
  
- Country GDP has a high correlation with capital allocation in early-stage startup

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/total_fund_and_GDP_for_2015.png?raw=true"/></p>
  
- GDP growth of a country given a boost in funding for an early-stage startup (Higher GDP results in increased funding, but trends shifted post-2015)

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/total_fund_and_GDP_in_USA.png?raw=true"/></p>
  
- The most favorite categories for investors

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/total_usd_pledged_per_category.png?raw=true"/></p>
  
- Increase in **App-Related** projects, beginning in 2013. This aligns with **the growing popularity of smartphones and mobile technology** story.

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/trend_app_project.png?raw=true"/></p>

## Result Comparision
Base Classifier vs Hyper parameter tuned model (no oversampling)

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/base_ft.PNG?raw=true"/></p>

Voting Classifier (Base & Fine Tuned models) (no oversampling)

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/voter_class.PNG?raw=true"/></p>

Synthetic Minority Oversampling Technique (Base & Fine Tuned models)

<p align="center"><img src="https://github.com/darshanvjani/Kickstarter-Campaigns-Analysis/blob/main/Data%20Visualization%20Images/smote.PNG?raw=true"/></p>


## The optimized XGBoost model obtained the best performance:
- Accuracy: **98.35%**
- Precision: **98.89%**
- Recall: **98.32%**
- F1-score: **98.53%**

## Conclusion and Recommendations
The models demonstrate reliable predictive capabilities for forecasting the success likelihood of proposed campaigns. Creators can leverage these insights to strategize their project planning and increase success odds.

Some actionable recommendations based on findings:
- Set feasible funding goals based on project scope and historical data
- Limit campaign duration to around 1 month
- Structure attractive reward tiers and limited editions
- Promote aggressively in first week to gain early traction
- Consider economic climate when estimating funding potential

There are several avenues for future work, such as incorporating social media data, longitudinal trends, and incorporation of policy changes over the years. Overall, this project provides data-driven guidance for key stakeholders in crowdfunding campaigns.
