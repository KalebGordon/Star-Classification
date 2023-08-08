# Star Type Prediction

Predicting whether a star is a Dwarf or a Giant based on its features using RandomForest Classifier, K-Nearest Neighbors (KNN), and Logistic Regression.

## Table of Contents

- [Introduction](#introduction)
- [Datasets](#datasets)
- [Features](#features)
- [Label](#label)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Results](#model-training-and-results)
- [Conclusion](#conclusion)

## Introduction

This project focuses on predicting the type of a star as either a Dwarf (0) or a Giant (1) based on various features using different classification algorithms including RandomForest Classifier, K-Nearest Neighbors (KNN), and Logistic Regression. The classifiers are trained on two distinct datasets, `Small Dataset` and `Large Dataset`.

## Datasets

Two datasets were used in this project:

- `Small Dataset`: Star3642_balanced.csv
- `Large Dataset`: Star39552_balanced.csv

## Features

The following features were utilized for classification:

- `Vmag`: Visual Apparent Magnitude of the Star
- `Plx`: Distance Between the Star and the Earth
- `e_Plx`: Standard Error of Plx (Rows with high `e_Plx` values were dropped)
- `B-V`: B-V color index (indicating star temperature)
- `SpType`: Spectral type (encoded)
- `Amag`: Absolute Magnitude of the Star

## Label

The target label for classification:

- `TargetClass`: Star Type (Dwarf - 0, Giant - 1)

## Data Preprocessing

- Removed duplicate index.
- Changed DataTypes.
- Removed missing values.
- Created absolute magnitude `Amag` column using M = m + 5(log10p+1) formula provided.
- The `SpType` column was encoded to ensure consistent values across both datasets.
- Rows with high `e_Plx` values were removed as indicated.

## Model Training and Results

Several classification algorithms were evaluated:

1. RandomForest Classifier:
   - Model trained on `Small Dataset` achieved an accuracy score of 0.91765.
   - Model trained on `Large Dataset` achieved an accuracy score of 0.920529.

2. K-Nearest Neighbors (KNN):
   - Model trained on `Small Dataset` achieved an accuracy score of 0.9423604.
   - Model trained on `Large Dataset` achieved an accuracy score of 0.9700823.

3. Logistic Regression:
   - Model trained on `Small Dataset` achieved an accuracy score of 0.903019.
   - Model trained on `Large Dataset` achieved an accuracy score of 0.874431.

## Conclusion

The classification project successfully predicts the type of stars (Dwarf or Giant) using multiple classification algorithms. The accuracy scores achieved indicate that K-Nearest Neighbors performed the best on both datasets, followed by RandomForest Classifier and Logistic Regression.

These results highlight the importance of experimenting with various algorithms to identify the one that best fits the problem's characteristics. Further exploration, feature engineering, and hyperparameter tuning could lead to even better results.

Feel free to contribute and explore the code in this repository! Your feedback and contributions are highly appreciated.
