# MAGIC Gamma Telescope Event Classification

Binary classification of high-energy Cherenkov gamma-ray events versus atmospheric hadronic noise using supervised machine learning models.

![Research Poster](SPCMachineLearningPoster.pdf)

## Project Overview
* Goal: Distinguish gamma-ray signals from hadronic noise patterns using geometric and light features.
* Dataset: [UCI MAGIC Gamma Telescope Dataset](https://archive.ics.uci.edu/dataset/159/magic+gamma+telescope) (19,020 samples, 11 features).
* Metric Focus: Optimized for F1-Score to balance precision and recall against disruptive false readings.

## Performance & Results
Evaluated 9 machine learning models using a 70/30 train-test split:

| Model | Test Accuracy | Test Precision | Test Recall | Test F1 Score |
| :--- | :--- | :--- | :--- | :--- |
| **Tuned XGBoost** | **0.879** | **0.878** | **0.947** | **0.911** |
| Random Forest | 0.875 | 0.880 | 0.936 | 0.907 |
| Decision Tree | 0.816 | 0.858 | 0.861 | 0.859 |
| Logistic Regression | 0.787 | 0.800 | 0.899 | 0.849 |

## Key Takeaways
* Top Features: Figure Length (major axis of the ellipse), Figure Alpha (camera angle), and Figure Size were the strongest predictors.
* Best Performer: Tuned XGBoost outperformed all baseline and ensemble models, achieving an 0.911 F1 score.
