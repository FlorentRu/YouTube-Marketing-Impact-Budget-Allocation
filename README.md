# YouTube Marketing Impact Budget Allocation

This repository demonstrates an **end-to-end** workflow for marketing analytics with an emphasis on **YouTube Marketing**. It includes synthetic data generation, data exploration, incremental impact measurement, and marketing budget optimization using Python.

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Key Features](#key-features)  
3. [Project Structure](#project-structure)  
4. [Detailed Workflow](#detailed-workflow)  
5. [Next Steps?](#next-steps)  


---

## Project Overview

In this demo project, we simulate a year’s worth of daily marketing spend across three channels:
1. **Search Ads**  
2. **Display Ads**  
3. **YouTube Ads**

We also generate a daily “outcome” metric. Then we:

- Explore the data and measure how each channel contributes to the outcome.  
- Build a **multiple linear regression** model to estimate each channel’s incremental impact.  
- Use optimization techniques from **SciPy** to allocate a fixed budget across channels in a way that maximizes the predicted outcome.

**Why?**  
Companies like Google and YouTube rely on data scientists to understand how marketing spend translates into business results. This project illustrates those core analytics and modeling steps.

---

## Key Features

1. **Synthetic Data Generation**  
   - Creates a realistic dataset with daily marketing spend, seasonal patterns, and random noise.

2. **Data Exploration**  
   - Statistical summaries  
   - Correlation heatmaps

3. **Modeling & Impact Analysis**  
   - Multiple linear regression to estimate channel effects  
   - Interpret coefficients as incremental outcome per $1 spent

4. **Budget Optimization**  
   - Given a fixed budget, uses constraint-based optimization to find the best distribution of spend among channels.

5. **Visualization**  
   - Plots of actual vs. predicted outcomes  
   - Residual distribution

---

## Project Structure

marketing-mix-yt/ 

├── YouTube Marketing Impact Budget Allocation.ipynb # Main Python script with all steps 

├── README.md # This README file 

└── ... (I created a ipynb to thouroughly explain every steps along the process)

- **YouTube Marketing Impact Budget Allocation.ipynb**  
  Contains the full workflow: data generation, EDA, modeling, optimization, and plotting.

- **README.md**  
  This document explaining how to use and navigate the project.

---
## Detailed Workflow

1. **Data Generation**  
   - Creates a daily dataset (365 days) of random marketing spend for each channel.  
   - Injects seasonality and random noise into the outcome metric.

2. **Exploratory Analysis**  
   - Produces summary statistics.  
   - Generates correlation matrices and heatmaps to visualize relationships.

3. **Modeling**  
   - Splits data into training (80%) and testing (20%).  
   - Trains a multiple linear regression model to identify channel coefficients.  
   - Evaluates performance using RMSE (Root Mean Squared Error) and R² (coefficient of determination).

4. **Incremental Impact**  
   - Interprets regression coefficients as incremental outcomes per $1 of channel spend.

5. **Optimization**  
   - Uses [SciPy’s `minimize`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.minimize.html) to maximize predicted outcomes under a fixed budget.  
   - Returns the optimal spend distribution for each channel.

6. **Visualization**  
   - Plots actual vs. predicted values to compare model performance.  
   - Shows residual distributions to detect any potential model biases.

---

## Next Steps?

- **Non-Linear Modeling**  
  Incorporate non-linear or diminishing returns (log-spend, polynomial features) to better capture real-world spending behavior.

- **Time-Series Effects**  
  Introduce time-series techniques (e.g., Prophet, ARIMAX) to account for trends and seasonality more precisely.

- **Dashboard Integration**  
  Build interactive dashboards using libraries such as [Streamlit](https://streamlit.io/) or [Dash](https://dash.plotly.com/).

- **Real-World Data**  
  Replace the synthetic dataset with actual marketing datasets, ensuring data privacy and compliance.

---
