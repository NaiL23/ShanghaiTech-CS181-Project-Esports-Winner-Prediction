# ShanghaiTech CS181 Project: ML-based Esports Winner Prediction for League of Legends Pro Matches
**Group Members: Lian Yihang, Wu Yiwen, Xiong Xinyang, Yu Shibo, Lv Junting** 

## Introduction

## Dataset
- ../data/2021_LoL_esports_match_data.csv
  - source: https://www.kaggle.com/chuckephron/leagueoflegends
  - pro matches in 2021
  - gold & exp & kill diff at 10min/15min
  - champion lineup & BP
- ../data/LeagueofLegends.csv
  - source: https://oracleselixir.com/tools/downloads
  - pro matches from 2015 to 2018
  - gold diff & dragons & towers & kill at each time step
  - champion lineup & BP
  
## Methods

### Naive Bayesis: Predict based on pure champion lineup

Result: 0.54 on 2021 Esports Dataset 

### Logistic Regression: Predict based on statistics at early game stage (15-min)

Result: 0.75 on 2021 Esports Dataset 



### Recurrent Neural Network: Real-time prediction

Result on 2015-2018 Esports Dataset: 

| Timesteps | RNN Accuracy | LSTM RNN Accuracy |
| --------- | ------------ | ----------------- |
| 0-10min   |              | 0.65              |
| 0-15min   |              | 0.73              |
| 0-20min   |              |                   |

0.73  

## Results & Thoughts
