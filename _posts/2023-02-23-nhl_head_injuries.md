---
title: Predicting NHL Head Injuries
date: 2023-02-23
layout: post
category: General
---

**The following will be a walkthrough of a data science project I completed and the methods used.**

# NHL Head Injuries

Head injuries and concussions have been a major concern in professional sports, including the National Hockey League (NHL). The objective of this project was to predict which NHL players are more susceptible to head injuries based on their past performance and other relevant data. This blog post will outline the approach taken for this project, including data understanding, data preparation, modeling, and deployment.


The data for this project was collected from two sources: the Eliteprospect_scraper package and a CSV file of NHL injuries from the past 20 years. The goal was to create a dataset of player performance, including their past injuries, and use this dataset to predict which players are more likely to suffer head injuries. The features used for this analysis were clearly described, and the data was cleaned, changing data types to integers/floats and making new features as required. The final dataset had around 18,000 rows.

The data was stored in a CSV file, and the variables were of string, integer, and float types. Preprocessing steps included cleaning the data, changing the data types to integers/floats, and making new features. The primary challenge in this project was gathering the injury data from the past 20 years. Important aspects of this data were visualized using bar plots and heat maps.

The most appropriate modeling techniques for this project were decision trees, logistic regression, random forest, and gradient boosting. The target variable for this classification problem was head_injuries. The baseline model for this project was a decision tree. Evaluation of this project was based on the F1 score. The minimum viable product (MVP) for this project involved several iterations of modeling, with tweaks to the hyperparameters and a steadily improving F1 score. The level-up stretch goals involved achieving the highest level of F1 score with grid searchcv.

The final results of this project were presented in a non-technical presentation. The Python libraries used for this project included Pandas, NumPy, Matplotlib, SciPy, Seaborn, and scikit-learn. The modeling algorithms used included Gradient Boosting, Decision Trees, Random Forest, and Logistic Regression.


The NHL Head Injuries project can be valuable tool for NHL teams and team managers to take proactive measures to prevent head injuries and minimize the impact of such injuries on the team’s performance. The project used machine learning techniques such as decision trees, logistic regression, random forest, and gradient boost to predict which players are more likely to suffer head injuries based on their past performance and other relevant information. The evaluation of the project was based on the F1 score, and the final results were presented in a non-technical presentation. Overall, this project demonstrated the usefulness of machine learning techniques in identifying and addressing critical issues in the sports industry.
