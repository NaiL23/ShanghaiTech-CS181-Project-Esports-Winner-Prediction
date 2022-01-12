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

### Naive Bayesis: Prediction based on pure champion lineup

#### Result

|       | 2021 Dataset | 2015-2018 Dataset |
| ----- | ------------ | ----------------- |
| Accuracy | 0.54 | 0.52 |



### Logistic Regression: Prediction based on statistics at early game stage (15min)

#### Result

|       | 2021 Dataset | 2015-2018 Dataset |
| ----- | ------------ | ----------------- |
| 10min |              |                   |
| 15min | 0.75         |                   |



### Recurrent Neural Network: Real-time prediction by statistics

#### Result on 2015-2018 Esports Dataset

| Timesteps | RNN Accuracy | LSTM RNN Accuracy |
| --------- | ------------ | ----------------- |
| 0-5min    | 0.56         | 0.58              |
| 0-10min   | 0.66         | 0.65              |
| 0-15min   | 0.72         | 0.73              |
| 0-20min   | 0.76         | 0.77              |
| 0-25min   | 0.78         | 0.80              |
| 0-30min   |              |                   |



## Results & Thoughts
