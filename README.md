# Data-Generation-using-Modelling-and-Simulation-for-ML
# Assignment: Data Generation using Modelling and Simulation for Machine Learning

## Step 1: Selection of Simulation Tool

Simulation Technique Selected: **Monte Carlo Simulation (Wireless Network Model)**  
Platform Used: **Google Colab (Python)**  

Monte Carlo simulation was used to generate synthetic data by randomly sampling input parameters and computing output using mathematical modelling equations.

---

## Step 2: Installation and Exploration

The following Python libraries were used:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

The simulation model is based on wireless communication theory using:

- Path Loss Model
- Signal-to-Noise Ratio (SNR)
- Shannon Capacity Formula

---

## Step 3: Identification of Important Parameters and Bounds

The following parameters were selected along with their lower and upper bounds:

| Parameter | Lower Bound | Upper Bound |
|------------|------------|------------|
| Distance (meters) | 10 | 500 |
| Transmission Power (dBm) | 10 | 30 |
| Bandwidth (MHz) | 1 | 20 |
| Interference Factor | 0.1 | 2.0 |
| Noise Power | Constant | 1e-9 |

Output Variable:
- Throughput (calculated using Shannon Capacity formula)

---

## Step 4: Random Parameter Generation

For each simulation:

- Parameters were randomly generated within defined bounds using uniform distribution.
- These parameters were passed into the mathematical simulation model.
- Throughput was calculated and recorded.

---

## Step 5: Generation of 1000 Simulations

A total of **1000 Monte Carlo simulations** were performed.

Each simulation generated one data record consisting of:

- Distance
- Transmission Power
- Bandwidth
- Interference
- Throughput

The resulting dataset was stored as a structured dataframe and exported as CSV.

---

## Step 6: Comparison of 5–10 Machine Learning Models

The generated dataset was split into training and testing sets (80:20 split).

The following regression models were trained and evaluated:

1. Linear Regression  
2. Ridge Regression  
3. Lasso Regression  
4. Decision Tree Regressor  
5. Random Forest Regressor  
6. Gradient Boosting Regressor  
7. Support Vector Regressor (SVR)  
8. K-Nearest Neighbors (KNN)  

### Evaluation Metrics Used:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### Best Performing Model:
Gradient Boosting Regressor achieved the highest R² score and was selected as the best model.

---

## Conclusion

Using Monte Carlo simulation, synthetic data was successfully generated based on wireless network modelling. A total of 1000 simulations were performed, and multiple machine learning models were evaluated. Based on performance comparison, Gradient Boosting Regressor provided the best predictive accuracy for the simulated dataset.
