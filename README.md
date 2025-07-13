# Shell.ai Hackathon: Fuel Blend Properties Prediction Challenge

This repository contains our solution for the **Fuel Blend Properties Prediction Challenge**, part of the **Shell.ai Hackathon 2025**. The objective of this challenge was to develop a machine learning model capable of predicting the physical and chemical properties of fuel blends, based on the composition and known properties of their individual components.

## 🛠 Problem Statement

Participants were provided with:
- A dataset of fuel blends with fractional composition of up to 5 components per blend
- 10 associated component properties that were unknown.

The goal was to predict **10 target blend properties**, which are critical for evaluating fuel performance, using these inputs.

## 📁 Dataset Overview

Each blend record included:
- `Component1_fraction` to `Component5_fraction`
- `Component1_Property1` to `Component5_Property10`

The target columns were:
- `Blend_Property1` to `Blend_Property10`

## 🧠 Approach

- Gradient Boosting (XGBoost):
Used XGBoost on to predict all targets at once in attempt 1, but then predicted each target column individually in attempt 2. Used feature engineering to try to find more complex relationships between fuel properties and fractions, and parameter tuning to get the lowest validation MAPE.


Final submission used a with feature engineering steps such as:
- Weighted averaging of component properties by their fractions
- Handling missing values and imputation
- Scaling and normalization

## 📊 Evaluation Metric

Performance was evaluated using **MAPE* across all 10 blend properties.

