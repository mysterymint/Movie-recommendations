DSA 4060 Week 1 Popularity Recommender
Student Name: Emmanuel Muondo
Student number: 669926

Project Overview
This project explores MovieLens user-item ratings and builds two non-personalized movie recommendation baselines: a minimum-rating popularity baseline and a Bayesian weighted-rating baseline. The recommender serves as a transparent baseline and an introductory model before moving into personalized algorithms.

Dataset
Dataset: MovieLens latest-small from GroupLens.
Source Link: GroupLens MovieLens Datasets
Files Used: movies.csv and ratings.csv
Date Accessed: September 2026

Methods
Rating-Count and Average-Rating Exploration: Loading data, validating integrity (checking for missing values and duplicates), and summarizing user interaction statistics and sparsity.
Minimum-Rating Popularity Baseline: Filtering movies by a minimum engagement threshold () and sorting by average rating.
Weighted-Rating Baseline: Applying a Bayesian weighted score formula to balance rating volume and average quality, pulling low-volume movies toward the global mean.

How to Run
Clone the repository:
git clone https://github.com/YOUR-USERNAME/dsa4060-week1-recommender.git
cd dsa4060-week1-recommender


Install the required packages:
pip install -r requirements.txt


Place the required CSV files (movies.csv and ratings.csv) inside the data/ folder if they are omitted.
Open the Jupyter Notebook:
jupyter notebook notebooks/week1_popularity_recommender.ipynb


Run all cells from top to bottom.

Key Findings
Exploratory analysis revealed a high interaction matrix sparsity exceeding , demonstrating that individual users rate only a tiny fraction of available films.
Relying solely on raw average ratings causes distortion, as obscure films with single five-star reviews outrank universally acclaimed masterpieces.
Implementing the 90th-percentile weighted score effectively stabilizes rankings, balancing high user appreciation with statistical confidence.

Limitations
Popularity Bias: Mainstream blockbusters dominate the lists, sidelining independent or niche content.
Lack of Personalization: Every visitor receives the identical Top 10 list regardless of individual tastes or viewing histories.
Cold-Start Problem: New movies with zero interactions cannot appear in popularity or weighted lists because they lack engagement data.
Repository Structure

dsa4060-week1-recommender/
├── data/
│   ├── movies.csv
│   └── ratings.csv
├── images/
│   └── top10_recommendations.png
├── notebooks/
│   └── week1_popularity_recommender.ipynb
├── .gitignore
├── README.md
└── requirements.txt


Screenshot
<img width="587" height="271" alt="image" src="https://github.com/user-attachments/assets/16e3e8af-3f79-426e-ab33-72743953b02d" />

