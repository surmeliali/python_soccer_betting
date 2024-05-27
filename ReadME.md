# Football Score Prediction and Profit Analysis

This repository contains a project for predicting football match scores and calculating potential betting profits using various machine learning models and scalers. The main script is `Score_Prediction_dataset.ipynb`.

## Table of Contents
- [Approach](#approach)
    - [Overview](#overview)
    - [Human Interaction using TOPSIS](#topsis)
    - [Different Strategies](#strategies)
- [Results](#results)
    - [Testing Out of Sample](#testing)
    - [Profit](#profit)
    - [Project Files](#files)
- [Acknowledgements](#acknowledgements)

## APPROACH

### Overview
The project aims to predict football match outcomes and calculate betting profits based on these predictions. Three models are implemented:
1. **Model A:** 1-2 Draw No Bet (DNB) profits by score difference prediction.
2. **Model B:** 1-0-2 winner prediction by *result prediction.
3. **Model C:** 1-0-2 winner prediction by *score prediction.

### TOPSIS:
We emphasized human interaction to enhance the model's performance, integrating the TOPSIS method (Technique for Order Preference by Similarity to Ideal Solution) to incorporate expert knowledge into our decision-making process. This approach ensured our machine learning models were both data-driven and intuitively aligned with strategic insights.

### Strategies:
We tested various betting strategies to identify the most effective ones. The best strategy, "Draw No Bet," utilized a Standard Scaler and Random Forest Classifier (max_depth:10, n_estimators:500).



## RESULTS

### Testing:
To prevent overfitting, we used "out of sample" data as a buffer between the model and the training data. This layer allowed us to identify and mitigate overfitting issues, ensuring robust and reliable predictions on new, unseen matches.

### Profit
By investing $100 per game with a signal to bet, we achieved 10.5% profitability, realizing %10.84 profit ratio over 348 bets. This validated our approach and the effectiveness of combining human interaction, TOPSIS, and rigorous testing.

![Screenshot of Results](/screenshots/results.png)

### Files
- `data_preparation.ipynb`: Dataset cleaning, merging and TOPSIS method implementation.
- `model/Score_Prediction_Dataset.ipynb`: Machine learning model implementation.
- `data/dataset.xlsx`: The main dataset contains various tables.
- `data/football_step10.csv`: The preprocessed dataset used for model training and prediction.

## Acknowledgements
I would like to extend our gratitude to the following sources for their invaluable data contributions:

* [WhoScored](https://www.whoscored.com/Statistics) for providing the comprehensive "Performance data".
* [TransferMarkt](https://www.transfermarkt.com/transfers/) for supplying the detailed "Total Market Cap and Age data."
* [FiveThirtyEight](https://projects.fivethirtyeight.com/soccer-api) for offering "Matches and Betting Odds" information.