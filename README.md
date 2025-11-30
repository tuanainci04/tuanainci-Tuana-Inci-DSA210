# DSA210 Term Project  
## Volleyball Positional Impact Analysis  

I am **Tuana İnci**, a IE student at **Sabancı University**, and this is my DSA210 Term Project.  
The goal of this project is to analyze performance patterns in the **2025 Volleyball Nations League (VNL) Women’s Final Four**, focusing on how **different player positions contribute to team success** through measurable in-game statistics.  

---

## Contents  
- [Motivation](#motivation)
- [Project Goal](#project-goal)
- [Data and Data Analysis](#data-and-data-analysis)
- [Files](#files)
- [Methods and Analysis](#methods-and-analysis)
- [Hypothesis Testing](#hypothesis-testing)
- [Machine Learning](#machine-learning)
- [Findings and Visualization](#findings-and-visualization)
- [Limitations](#limitations)
- [Future Work](#future-work)
- [Conclusion](#conclusion)

---

## Motivation  
Volleyball is a sport where every position plays a unique and essential role.  
I wanted to analyze how different positions — **Outside Hitters (OH)**, **Middle Blockers (MB)**, **Opposites (O)**, **Setters (S)**, and **Liberos (L)** — contribute to a team’s overall performance and outcomes in international tournaments.  
This analysis aims to uncover which roles are most decisive in winning matches and how efficiency differs among teams at the highest level of competition.

---

## Project Goal  
The project aims to **quantify positional impact** using data from the **2025 VNL Women’s Final Four** (teams: *Italy, Brazil, Poland, Japan*).  
The focus is on measuring player performance through metrics such as:
- **Attack Points**
- **Block Points**
- **Serve Points**
- **Efficiency (%)**
- **Total Points**

The analysis evaluates how these variables vary across positions and teams, and whether certain roles contribute disproportionately to match outcomes.

---

## Data and Data Analysis  

The dataset was manually collected from **Volleyball World official match statistics** and includes all **semifinal, final, and 3rd-place matches** of the 2025 Women’s VNL.  

Each record in the dataset includes:
- **Team**  
- **Opponent**  
- **Stage** (Semifinal, Final, or 3rd Place)  
- **Player No & Name**  
- **Position (OH, MB, O, S, L)**  
- **Attack Points**  
- **Block Points**  
- **Serve Points**  
- **Errors**  
- **Efficiency (%)**  

The dataset also includes team-level summaries such as:
- **Attack**, **Block**, **Serve**, **Opponent Errors**, and **Total Points** per team.  

These were compiled into two structured CSV files:
1. `team_summary.csv` – aggregated statistics by team and match  
2. `player_stats.csv` – detailed player-level records  

---

## Files  
- `team_summary.csv` – team-level statistics from semifinals, finals, and 3rd place  
- `player_stats.csv` – player-level performance data for all teams  
- `VNL_Positional_Impact_Analysis.py` – Python analysis script  
- `fig/` – folder containing generated visualizations  

---

## Methods and Analysis  

### 1. Data Cleaning  
- Converted numeric fields to proper data types  
- Handled missing or inconsistent values  
- Computed a new variable: **Total Points = Attack + Block + Serve**

### 2. Exploratory Data Analysis (EDA)  
- **Boxplot** → Distribution of total points by position  
- **Bar Graph** → Average efficiency by position  
- **Heatmap** → Correlation between attack, block, serve, and efficiency  
- **Team Bar Plot** → Skill distribution (attack, block, serve) for each team  

---

## Hypothesis Testing  

### Hypothesis 1: Positional Differences  
**H₀:** All positions contribute equally to team success  
**H₁:** At least one position contributes significantly more to total points  

Test: **One-way ANOVA**  
Result: p < 0.05 → Significant difference in scoring between positions  

### Hypothesis 2: Attack vs. Block Impact  
**H₀:** There is no difference between attack and block contributions  
**H₁:** Attack contributions are significantly higher than block contributions  

Test: **Paired t-test**  
Result: p < 0.05 → Attack plays a more decisive role in scoring outcomes  

---

## Machine Learning  

A **Linear Regression** model was implemented to predict total points using attack, block, and serve performance as input features.

**Model:**  
\[
TotalPoints = β_0 + β_1(Attack) + β_2(Block) + β_3(Serve)
\]

**Metrics:**
- Mean Squared Error (MSE): *low value → good fit*  
- R² Score: *high value → strong predictive relationship*  

This confirmed that a player’s total contribution can be linearly explained by their offensive and defensive performance metrics.

---

## Findings and Visualization  

- **Outside Hitters (OH)** and **Opposites (O)** achieved the highest total points.  
- **Middle Blockers (MB)** led in block contributions and efficiency.  
- **Brazil** and **Italy** displayed the most balanced attack-block ratios.  
- Attack, block, and serve metrics showed strong positive correlation with total points.  
- Regression confirmed that these three skills predict scoring consistency well.  

---

## Limitations  
- The dataset covers only **four national teams** from a single tournament (VNL 2025).  
- Player-level metrics may not include **defensive digs** or **receiving efficiency**, which affect real performance.  
- Sample size limits generalization to broader contexts.  

---

## Future Work  
- Incorporate **additional tournaments** (e.g., Olympic Games, World Championships).  
- Expand dataset to include **defensive and reception metrics**.  
- Develop a **machine learning classification model** predicting match winners.  
- Create an **interactive dashboard** for real-time performance visualization.  

---

## Conclusion  
This project reveals that **offensive roles (OH and O)** contribute most heavily to team scoring, while **blocking and serving efficiency** from **MBs and Setters** also play critical roles in team success.  
By combining statistical testing and regression modeling, the analysis highlights how positional balance shapes outcomes at the elite international level of volleyball.
