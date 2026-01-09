# Decision Trees, Bagging, and Random Trees
CS 7646 — Machine Learning for Trading  
Georgia Institute of Technology

---

## Project Overview

This project explores supervised learning algorithms from the **Classification and Regression Trees (CART)** family and evaluates their behavior under varying hyperparameters.

The focus is on understanding:
- Overfitting vs underfitting
- Bias–variance tradeoff
- The effect of ensemble methods (bagging)
- Structural differences between deterministic and randomized trees

The project consists of multiple controlled experiments using regression tasks and quantitative error metrics.

---

## Algorithms Implemented

The following learners are implemented and evaluated:

- Decision Tree Learner (DT)
- Random Tree Learner (RT)
- Bagged Decision Trees
- Linear Regression (baseline comparison)
- Insane Learner (ensemble stress test)

All learners are evaluated using identical datasets and experimental conditions.

---

## Code Availability and Academic Integrity

The full implementation for this project is maintained in a **separate private repository**.

This separation is intentional and required to comply with **Georgia Tech academic integrity policies**, which prohibit public sharing of full course solutions. Sharing code privately with recruiters and employers is explicitly permitted.

Full implementation is available upon request.

This public repository contains:
- Generated figures
- Experimental results
- High-level methodology
- Analysis and interpretation

---

## Experiment 1 — Decision Tree Overfitting

**Goal:**  
Evaluate how Decision Tree performance changes as `leaf_size` varies.

**Metric:**  
Root Mean Squared Error (RMSE)

**Key Observations:**
- Small leaf sizes result in very low in-sample error
- Out-of-sample error increases sharply at small leaf sizes
- Larger leaf sizes reduce overfitting but increase bias

This experiment clearly demonstrates classic overfitting behavior.

---

## Experiment 2 — Effect of Bagging

**Goal:**  
Compare a single Decision Tree to a Bagged ensemble of trees.

**Metric:**  
RMSE (in-sample and out-of-sample)

**Key Observations:**
- Bagging consistently reduces out-of-sample error
- Variance is significantly reduced relative to a single tree
- In-sample error increases slightly, indicating better generalization

This experiment highlights how ensemble methods improve robustness.

---

## Experiment 3 — Decision Trees vs Random Trees

**Goals:**
- Compare predictive accuracy using MAE
- Compare model complexity via number of tree nodes

**Key Observations:**
- Random Trees reduce variance but increase bias
- Decision Trees achieve lower in-sample error
- Random Trees produce simpler, smaller models
- Model size decreases rapidly as leaf size increases

This experiment illustrates the tradeoff between interpretability, complexity, and generalization.

---

## Summary of Findings

- Decision Trees are highly expressive but prone to overfitting
- Bagging effectively reduces variance and improves generalization
- Random Trees trade accuracy for simplicity and stability
- Leaf size is a critical hyperparameter controlling bias–variance behavior

These results reinforce why ensemble methods are widely used in real-world machine learning systems.

---

## Repository Structure

├── figures/
│   ├── exp1_dt_overfitting_rmse.png
│   ├── exp2_bagging_effect.png
│   ├── exp3_dt_vs_rt_mae.png
│   └── exp3_dt_vs_rt_modelsize.png
└── README.md
