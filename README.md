# Phase_3_Project
# **HORIZON CONSULTANCY AND MARKETING GROUP:** *PREDICTING HIGH-GROWTH YOUTUBE CHANNELS USING CLASSIFICATION MODEL*
## **Business Understanding**
## Overview
Horizon Consultancy and Marketing Group is looking forward to patnering with influential YouTubers to help promote several brands that the company will be working with in the next few months.
The company's Business Development Manager needs information to identify YouTube channels that are likely to experience high subscriber growth in the next month so they can target them for early brand partnerships. Therefore they require to make data-driven decisions based on the predictions from the classification model.
## **Data Understanding**
The dataset used in this project is Global YouTube Statistics. It offers a perfect avenue to analyze and gain valuable insights from the experts on the platform. It contains 28 columns including:
Channel metrics: subscribers, video views, uploads, rank
Categorical features: category, channel_type, Country
Growth indicators: subscribers_for_last_30_days
Country-level context: population, unemployment rate, education enrollment 
Therefore, this makes it suitable for classification. Our target variable derived from this dataset is High growth channel which makes 'subscribers_last_30_days' the binary classification target.
## **Modeling**
The models use channel-level performance metrics, content characteristics, and country-level socioeconomic indicators as features. These variables were selected because they are available prior to subscriber growth and are likely to influence a channel’s ability to attract new subscribers.
Several columns were dropped. Those that were completely insignificant to modeling and those that served as identifiers, outcome-derived metrics, or post-growth indicators were removed to prevent data leakage and ensure the model relied only on information available prior to subscriber growth.
Categorical variables were transformed using one-hot encoding to convert them into a numerical format suitable for classification models. A logistic regression model was used as the baseline model due to its interpretability and effectiveness for binary classification problems. Model performance was evaluated using accuracy, precision, recall, and F1-score to assess how well the model identifies high-growth channels. After tuning the regularization parameters, the logistic regression model showed improved generalization on the test set, indicating that controlling model complexity helped reduce overfitting.
Secondly,a decision tree was our nonparametric model in order to capture nonlinear relationships and interactions between features without requiring feature scaling.
## **Evaluation**
After evaluating multiple classification models, the tuned decision tree classifier was selected as the final model due to its superior predictive performance on unseen data. The tuned decision tree achieved the highest test accuracy (0.8876), outperforming both the baseline and tuned logistic regression models.

The strong performance of the decision tree suggests that nonlinear relationships and feature interactions play an important role in predicting high-growth YouTube channels. By tuning model hyperparameters such as tree depth and minimum sample sizes, the model was able to generalize effectively while reducing overfitting.

In addition to its predictive strength, the decision tree model provides interpretable insights through feature importance rankings, allowing Horizon Consultancy and Marketing Group to better understand which factors most strongly influence channel growth and to translate these insights into actionable marketing strategies.
## **Conclusion**
This project demonstrated the application of predictive modeling techniques to address a real-world digital marketing problem: identifying high-growth YouTube channels. By framing the problem as a binary classification task, multiple models were built and evaluated using an iterative approach, including logistic regression and decision tree classifiers.

Among the models tested, the tuned decision tree achieved the strongest predictive performance on unseen data, indicating that nonlinear relationships and feature interactions play a significant role in channel growth. Through careful preprocessing, prevention of data leakage, and appropriate metric selection, the final model provides reliable and interpretable predictions.

These findings equip Horizon Consultancy and Marketing Group with a data-driven tool to better target high-growth creators, optimize marketing investments, and make informed strategic decisions while acknowledging the importance of model limitations and contextual use.