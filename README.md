Project Overview

This project analyzes internal employee email communication to evaluate overall sentiment, engagement levels, employee ranking, and potential flight risk.

The dataset contains the following columns:

Subject

Body (email content)

Date

From (employee sender)

The goal is to extract insights from raw unlabeled data using NLP techniques and statistical analysis.

-----------------------------------------------------------------------------------------------------------------------------

Project Objectives

The objectives of this project are:

Perform sentiment labeling (Positive, Negative, Neutral)

Conduct exploratory data analysis (EDA)

Calculate monthly sentiment score for each employee

Rank employees based on sentiment score

Identify flight risk employees

Build a linear regression model to analyze sentiment trends

-----------------------------------------------------------------------------------------------------------------------------

Task 1 – Sentiment Labeling

Each email body was analyzed using the VADER Sentiment Analyzer from NLTK.

Based on the compound score:

Score > 0.05 → Positive

Score < -0.05 → Negative

Otherwise → Neutral

A numerical score was assigned:

Positive → +1

Negative → -1

Neutral → 0

Two new columns were added:

Sentiment

Score

-----------------------------------------------------------------------------------------------------------------------------

Task 2 – Exploratory Data Analysis (EDA)

The following analysis was performed:

Dataset structure and data types

Sentiment distribution

Monthly sentiment trend

Message length distribution

Employee-level patterns

All visualizations were saved inside the visualizations folder.

-----------------------------------------------------------------------------------------------------------------------------

Task 3 – Monthly Employee Sentiment Score

For each employee:

Messages were grouped by month.

Scores were summed for each month.

The score resets every new month.

Formula used:

Employee + Month → Sum of sentiment scores

-----------------------------------------------------------------------------------------------------------------------------


Task 4 – Employee Ranking

For each month:

Top 3 employees with highest positive scores

Top 3 employees with lowest negative scores

Sorting was done by:

Sentiment score

Alphabetical order (for tie-breaking)

-----------------------------------------------------------------------------------------------------------------------------


Task 5 – Flight Risk Identification

An employee is considered a flight risk if:

They send 4 or more negative emails within a rolling 30-day period.

A rolling 30-day window was applied per employee to detect sustained negative communication patterns.

The flagged employees are displayed in the notebook output.

-----------------------------------------------------------------------------------------------------------------------------



Task 6 – Predictive Modeling

A Linear Regression model was developed to analyze sentiment trends.

Features used:

Monthly message count

Average message length per month

The model was trained using an 80/20 train-test split.

Evaluation metrics:

Mean Squared Error (MSE)

R² Score

Model performance visualization is saved in the visualizations folder.

-----------------------------------------------------------------------------------------------------------------------------
Project Structure

Employee-Sentiment-Analysis/

main.ipynb

test.xlsx

README.md

requirements.txt

visualizations/

sentiment_distribution.png

message_length_distribution.png

monthly_sentiment_trend.png

ranking_chart.png

model_performance.png

-----------------------------------------------------------------------------------------------------------------------------


Setup Instructions

Install required libraries:

pip install pandas numpy matplotlib seaborn scikit-learn nltk openpyxl

Then run:

jupyter notebook

Open main.ipynb and run all cells sequentially.

Conclusion

This project demonstrates:

Sentiment analysis using NLP

Data exploration and visualization

Monthly employee scoring and ranking

Flight risk detection using rolling window logic

Predictive modeling using linear regression

The workflow is structured, reproducible, and aligned with the project requirements.

-----------------------------------------------------------------------------------------------------------------------------