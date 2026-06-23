# Astrometrics_Statistics_Project
# Space Missions Statistical Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-orange) ![SciPy](https://img.shields.io/badge/SciPy-1.x-green)

## 📌 Overview

A comprehensive **statistical analysis and machine learning study** on a Space Missions dataset, covering probability theory, descriptive statistics, distribution fitting, correlation analysis, regression modeling, and mission success prediction using Gaussian Naive Bayes.

This project was completed as part of the Open Elective Lab (OEL) coursework and demonstrates applied statistics and ML on real-world space exploration data.

---

## 🎯 Objectives

1. Perform complete **descriptive statistical analysis** on space mission parameters
2. Identify and fit **probability distributions** to key variables
3. Analyse **correlation** between mission parameters
4. Build **regression models** to predict launch costs
5. Predict **mission success** using Gaussian Naive Bayes classification

---

## 📊 Dataset

**Space Missions Dataset** containing records of global space missions with the following features:

| Feature | Type | Description |
|---|---|---|
| LaunchYear | Numerical | Year of launch |
| PayloadMass (kg) | Numerical | Mass of payload |
| LaunchCost (Million USD) | Numerical | Cost of launch |
| FuelConsumption (tons) | Numerical | Fuel used |
| FlightTime (minutes) | Numerical | Duration of mission |
| RocketType | Categorical | Type of rocket used |
| OrbitType | Categorical | Target orbit |
| MissionSuccess | Binary | 1 = Success, 0 = Failure |
| Manufacturer | Categorical | Rocket manufacturer |

---

## 🏗️ Project Structure

### Module 1 — Descriptive Statistics

Complete statistical profiling of all numerical features:

| Statistic | Method |
|---|---|
| Mean, Median, Mode | Central Tendency |
| Range, Variance, Std Dev | Dispersion |
| Q1, Q2, Q3, IQR | Quartile Analysis |
| Kurtosis, Skewness | Distribution Shape |

**Visualisations:** Bar charts, pie charts, histograms, and boxplots for all key features and categorical columns (RocketType, OrbitType, MissionSuccess, Manufacturer).

---

### Module 2 — Probability Distributions & Naive Bayes

**Distribution fitting:**

| Distribution | Applied To | Purpose |
|---|---|---|
| Bernoulli | MissionSuccess | Binary success/failure probability |
| Normal | LaunchYear, PayloadMass | Continuous variable fitting |
| Poisson | Mission frequency | Count-based event modeling |

**Gaussian Naive Bayes Classifier:**

```python
Features: PayloadMass (kg), LaunchCost (Million USD),
          FuelConsumption (tons), FlightTime (minutes)
Target:   MissionSuccess (0 / 1)
```

- Train/test split with stratification
- Accuracy score + full classification report
- Bayesian probability applied to space mission success prediction

---

### Module 3 — Correlation & Regression

**Correlation Analysis:**
- Full correlation matrix across all numerical features
- Heatmap visualisation using Seaborn

**Single-Feature Linear Regression:**
- Predicts `LaunchCost (Million USD)` from `PayloadMass (kg)`
- Prints intercept, coefficient, and regression line plot

**Multi-Feature Linear Regression:**
- Iterates over all numerical columns as target variables
- Reports MAE and MSE for each model
- Identifies strongest predictors via coefficient analysis

**Statistical Hypothesis Testing:**
- T-tests: Numerical columns vs. MissionSuccess (binary grouping)
- ANOVA: Categorical columns (RocketType, OrbitType, Manufacturer) vs. numerical features
- Statsmodels OLS for detailed regression summaries

---

## 📈 Key Results

- **Gaussian Naive Bayes** achieved strong accuracy on mission success prediction using only 4 numerical features
- **PayloadMass and LaunchCost** showed the highest positive correlation among numerical features
- **MissionSuccess distribution** followed a Bernoulli distribution with p ≈ 0.85 (high historical success rate)
- **LaunchYear** showed near-normal distribution indicating balanced temporal coverage of the dataset

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.10 | Core language |
| Pandas / NumPy | Data loading and processing |
| Matplotlib / Seaborn | All visualisations |
| SciPy (stats) | Kurtosis, skewness, T-tests, ANOVA, distribution fitting |
| Scikit-learn | Naive Bayes, Linear Regression, train/test split |
| Statsmodels | OLS regression with detailed summary |
| Google Colab | Development environment |

---

## 🚀 How to Run

### 1. Clone the repo
```bash
git clone https://github.com/Galaxy-03/space-missions-analysis.git
cd space-missions-analysis
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy statsmodels
```

### 3. Add dataset
Place `Space_Missions_Dataset.csv` in the project root (or update the filepath in the notebook).

### 4. Run notebook
Open `astrometrics.ipynb` in Google Colab or Jupyter and run all cells sequentially.

---

## 📂 Repository Structure

```
space-missions-analysis/
├── astrometircs.ipynb    ← Main notebook
├── README.md                           ← This file

```

---

## 📚 Statistical Concepts Covered

- Measures of central tendency and dispersion
- Quartile and IQR analysis
- Kurtosis and skewness classification
- Bernoulli, Normal, and Poisson distribution fitting
- Pearson correlation and heatmap analysis
- Simple and multiple linear regression
- Gaussian Naive Bayes classification
- Independent samples T-test and one-way ANOVA
- Applied Gaussian Naive Bayes for mission success classification; evaluated with accuracy score and full classification report across 4 numerical features

---

## 👩‍💻 Author

**Chinmayi Suhas Dighe**
B.Tech CSE, D Y Patil International University, Pune
