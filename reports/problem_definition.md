# Song Popularity Prediction Project –  
AI-Driven Song Popularity & Trend Prediction System using Audio Features and User Engagement Data.
This project uses audio features and metadata to predict a song’s popularity score using Machine Learning.

## Business Objective
Predict the popularity of a song before or shortly after release to support playlist curation, marketing spend allocation, and A&R decisions.

## ML Objective
Learn a mapping from audio features and metadata to a continuous popularity score.

## Target Variable
`popularity` (integer, 0–100) as provided by Spotify.

## ML Task Type
Supervised Learning – Regression

## Why Regression?
- Popularity is ordinal & continuous
- Preserves ranking information
- Preferred by industry for downstream thresholding

## Optional Extension
Binary classification:
- Hit: popularity ≥ 70
- Non-Hit: popularity < 70

## Evaluation Metrics (tentative)
- Primary: RMSE
- Secondary: MAE, R²

## Constraints
- No post-release engagement leakage
- Use only pre-release audio features