# DataMining-FinalProject
Authors: Ethan Meyer, Ishika Patel

## Project Description
Recently, there has been an explosion of interest in leveraging machine learning models in the context of sports analytics. In this paper, we apply data mining techniques to inform bets on match outcomes of the NCAA March Madness basketball tournament using aggreagated season statistics, tournament information, and team ranking. Specifically, we evaluate four classification models (Four Factor Model, Logistic Regression, K-Nearest Neighbors, and Support Vector Machine) against a series of baseline methods. Using various betting strategies and historical Vegas odds data, we evaluate the performance of our models by computing their accuracy and return on investment (ROI). Our results demonstrate the potential of machine learning for obtaining a positive ROI in sports betting and suggest that similar approaches may be applicable to other sports betting scenarios. We conclude our paper with a discussion of insights gained and propose future work.


## Introduction
Over the last decade, sports betting has experienced a meteoric rise in popularity. In the 2022 tourney alone, March Madness—the annual NCAA Basketball Tournament— was expected to garner approximately  3.1 billion in bets on platforms such as FanDuel, DraftKings, and BetMGM. With this incredible amount of par- ticipation, increasing rates of sports betting legality, and the ample amount of historical data available on NCAA teams, predicting the winner NCAA basketball matches is a prime subject for investiga- tion. 

March Madness matches are renowned for their unpredictability. In fact, it is one of the main reasons the tournament garners so much attention from fans. Factors such as volatile player contribution on the court, streaks in game-play, buzzer beaters, and more all come together to form "Cinderella Stories" - situations in which teams achieve far greater successes than spectators could have reasonably expected. These dynamic aspects of the game engage fans and present a rewarding challenge—that of predicting game winners—for data miners to approach.

## Software Prerequisites

 Python 3
 
 Jupyter Notebook
 

## List of Relevant Python Packages


* Pandas.DataFrame
* numpy
* matplotlib
* sklearn
* Levenshtein



## Data Transformation

#### Data Cleaning
`/preprocessing/Moneyline Data Pre-Processing.ipynb`: Examined and resolved issues within data, filling in missing information

#### Data Exploration
`/models/Ethan's Sandbox.ipynb`: Familiarized  ourselves with structure and information available within data sets 

#### Data Integration
`/preprocessing/Moneyline Data Pre-Processing.ipynb`: Developed methodology for connecting numerous data sources

#### Data Computation 
`/models/ML Model Feature Computation.ipynb`: Aggregated and computed advanced statistics, performed betting unit conversion

## Data Modeling
1. Identified potential classification models
2. Hyperparametrized models
3. Outlined potential betting strategies (bet uniform, bet edge)
4. Calculated performance statistics (Accuracy & ROI)

Models:
- 4-Factor Model (Ishika Patel): `models/FourFactors.ipynb`
- Logistic Regression (Ethan Meyer): `models/Macine Learning Models.ipynb`
- K Nearest Neighbors (Ethan Meyer): `models/Macine Learning Models.ipynb`
- Support Vector Machines (Ethan Meyer): `models/Macine Learning Models.ipynb`

## Evaluation

### Baseline Results: 
`graphics/Data Visualizations.ipynb`

| Model       | Avg. Accuracy | Avg. ROI
| -----------  |------------- | -------
| Bet Favorite      | 70.04%       | -5.49%
| Bet Underdog      | 29.35%       | -4.35%
| Bet Favorite      | 62.85%       | -3.83%

### Four Factor Model Results
`models/FourFactors.ipynb`

| Model       | Avg. Accuracy | Avg. ROI
| -----------  |------------- | -------
|Do Not Bet Within Interquartile Range| 49.9% | -17.9% 
|Must Bet: Median Difference as Split | 62.9% | -5.1%
|Do Not Bet Within Quartile 1 and Median | 66% | -3.2%  
|Must Bet: Quartile 1 Difference as Split | 62.9% | -5.1%  
|Must Bet: Mean Difference as Split | 62.9% | -5.1% 
|Do Not Bet Within Quartile 1 and Mean | 66.1% | -2.9%

| Model       | Avg. Accuracy | Avg. ROI
| -----------  |------------- | -------
|Do Not Bet Within Interquartile Range| 50.1% | -17.8% 
|Must Bet: Median Difference as Split | 62.9% | -5.1%
|Do Not Bet Within Quartile 1 and Median | 71.2% | 2.7%  
|Must Bet: Quartile 1 Difference as Split | 62.9% | -5.1%  
|Must Bet: Mean Difference as Split | 62.9% | -5.1% 
|Do Not Bet Within Quartile 1 and Mean | 70.4% | 1.6%


### Machine Learning Model Results
#### Bet Uniform
`graphics/Data Visualizations.ipynb`

| Model       | Avg. Accuracy | Avg. ROI
| -----------  |------------- | -------
| Logistic Regression     | 71.32%       | +0.44%
| K-Nearest Neighbors      | 66.16%       | -1.28%
| Support Vector Machine      | 71.06%       | -0.43%

#### Bet Edge
`graphics/Data Visualizations.ipynb`

| Model       | Avg. Accuracy | Avg. ROI
| -----------  |------------- | -------
| Logistic Regression     | 51.21%       | +3.13%
| K-Nearest Neighbors      | 36.47%       | -0.45%
| Support Vector Machine      | 44.03%       | -0.80%



## Key Findings
### Four Factor Model
1. **Incorporating Historical Data:** Between models, leveraging years worth of historical data when not updating a model’s attribute weights does drive higher returns.
2. **Betting strategy performance:** Betting based on predetermined weights of a model may not be the best strategy, we need to consider even more enhanced betting strategies.

### Machine Learning Model Results
1. **Accuracy, ROI relationship:** Between models, bet accuracy is not always the best performance measure when optimizing for ROI. 

2. **Betting strategy performance:** Enhanced betting strategies have the potential to drive higher returns.


3. **Positive ROI:** ML models are capable of returning a positive ROI in sports betting applications. 


## Plots: `\graphics`
Make sure you are in Light Mode for best viewing!
### Comparissons
<img src="graphics/Overall ROI Comparisson.png"
     style="float: left; margin-right: 10px;"/>
<img src="graphics/ROI by strategy ML.png"
     style="float: left; margin-right: 10px;" />

### Baseline Models
<img src="graphics/Accuracy baseline boxplot.png"
     style="float: left; margin-right: 10px;"/>
<img src="graphics/ROI baseline boxplot.png"
     style="float: left; margin-right: 10px;" />



### Four Factor Models
<img src="graphics/FF Accuracy Running Data.png"
     style="float: left; margin-right: 10px;"/>
<img src="graphics/FF ROI Running Data.png"
     style="float: left; margin-right: 10px;"/>
<img src="graphics/FF Acuracy Running Season Data.png"
     style="float: left; margin-right: 10px;"/>
<img src="graphics/FF ROI Running Season Data.png"
     style="float: left; margin-right: 10px;"/>



### Machine Learning Models
<img src="graphics/Accuracy Uniform ML boxplot.png"
     style="float: left; margin-right: 10px;"/>
<img src="graphics/ROI Uniform ML boxplot.png"
     style="float: left; margin-right: 10px;" />
<img src="graphics/Accuracy Edge ML boxplot.png"
     style="float: left; margin-right: 10px;" />
<img src="graphics/ROI Edge ML boxplot.png"
     style="float: left; margin-right: 10px;" />
