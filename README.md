# Tuana İnci DSA210 Term Project
Volleyball Positional Impact Analysis

## Introduction
This project analyzes how different **player positions** contribute to **team success** in professional **women’s volleyball**.  
The focus is on the **top four national teams** that reached the **semifinals of the 2025 FIVB Volleyball Nations League (VNL)** — **Italy**, **Brazil**, **Poland**, and **Japan**.  
By studying detailed **player-level statistics** such as spikes, blocks, aces, and errors across positions (**outside hitter**, **opposite**, **setter**, **middle blocker**, and **libero**), the project aims to understand which positions have the greatest impact on team performance and how positional balance affects international success.

## Motivation
In competitive volleyball, each position plays a unique and vital role in determining team outcomes.  
This project is motivated by the following goals:
- **Identify which positions contribute most** to overall team success.  
- **Compare player performance** across elite national teams.  
- **Analyze positional balance** between offensive and defensive roles.  
- **Understand how performance metrics** (such as spikes and blocks) influence rankings and match results.  
- **Highlight the efficiency patterns** that separate championship-level teams from others.  

## Data Source
The primary dataset will be collected from the **official statistics** of the **2025 Volleyball Nations League (Women’s Tournament)**, available on the **Volleyball World** website.  
Additional sources include:
- **Volleybox.net** – For player positions, nationality, and background details.  
  


## Hypothesis Testing
- **Positional Contribution Test:**  
  - **H₀:** All positions contribute equally to team success.  
  - **H₁:** Certain positions contribute more significantly to team performance.  
  - **Method:** ANOVA and correlation analysis.  
  - **Interpretation:** If *p-value < 0.05*, position-based differences are statistically significant.

- **Team Performance Comparison Test:**  
  - **H₀:** There is no difference in performance between the top national teams.  
  - **H₁:** At least one team performs significantly better in key metrics.  
  - **Method:** Independent t-tests and descriptive comparison.  
  - **Interpretation:** If *p-value < 0.05*, performance differences are significant.

- **Efficiency–Ranking Relation Test:**  
  - **H₀:** Spike efficiency and team ranking are not correlated.  
  - **H₁:** Higher spike efficiency is positively correlated with better rankings.  
  - **Method:** Correlation and regression analysis.  
  - **Interpretation:** If *p-value < 0.05*, efficiency is a significant predictor of success.

## Tools & Technologies
- **Python**
  - `pandas` – Data cleaning and organization  
  - `numpy` – Statistical calculations and averages  
- **Jupyter Notebook** – For analysis and visualization  
- **Excel** – For initial data collection and manual preprocessing  

## Data Processing
- **Data Cleaning:** Remove missing or inconsistent records from the dataset.  
- **Standardizing Positions:** Unify position names (e.g., *OH*, *MB*, *OP*, *S*, *L*).  
- **Data Integration:** Combine data from multiple sources (VNL website, Volleybox).  
- **Feature Selection:** Focus on relevant variables such as spikes, blocks, aces, and efficiency.  
- **Grouping and Aggregation:** Summarize player statistics by position and national team for analysis.  

## Data Analysis & Visualizations
- **Positional Comparison:** Use **bar and box plots** to compare positional performance metrics across teams.  
- **Team-Level Analysis:** Create **radar charts** to visualize overall team strengths and weaknesses.  
- **Correlation Study:** Generate **heatmaps** to show relationships between efficiency, scoring, and errors.  
- **Performance Distribution:** Use **violin and scatter plots** to analyze player contributions within positions.  
- **Predictive Modeling (Future Work):** Build a **regression model** to estimate team ranking based on positional averages.  


## Limitations & Future Work
- **Limited Dataset:** Only covers the 2025 VNL Women’s Tournament.  
- **Data Availability:** Some player-level metrics may be incomplete.  
- **Sample Size:** Analysis is limited to four national teams.  
- **Future Work:**  
  - Include more tournaments (e.g., Olympic Games, World Championships).  
  - Automate data collection from official APIs.  
  - Implement advanced machine learning models for ranking prediction.  
  - Build an interactive visualization dashboard for real-time insights.  
