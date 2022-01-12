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
| Accuracy | 0.540 | 0.527 |



### Logistic Regression: Prediction based on statistics at early game stage (15min)

#### Result

|                   | lineup only | golddiff at 15min only | golddiff/tower/dragon/kill at 15min |
| ----------------- | ----------- | ---------------------- | ----------------------------------- |
| 2021 Dataset      | 0.541       | 0.760                  | /                                   |
| 2015-2018 Dataset | 0.532       | 0.698                  | 0.723                               |



### Recurrent Neural Network: Real-time prediction by statistics

Capture 7 features per time step:

- `golddiff`: difference in team total gold
- `dragondiff`: difference in number of dragons killed
-  `barondiff`: difference in number of barons killed
-  `heralddiff`: difference in number of heralds killed
-  `towerdiff`: difference in number of enemy towers destroyed
-  `inhibitordiff`: difference in number of enemy inhibitors destroyed
-  `killdiff`: difference in number of enemy champions killed

#### Result on 2015-2018 Esports Dataset

| Timesteps | RNN Accuracy | LSTM RNN Accuracy |
| --------- | ------------ | ----------------- |
| 0-5min    | 0.580        | 0.589             |
| 0-10min   | 0.665        | 0.667             |
| 0-15min   | 0.731        | 0.739             |
| 0-20min   | 0.773        | 0.774             |
| 0-25min   | 0.827        | 0.829             |
| 0-30min   | 0.844        | 0.850             |

