# The Historical NBA Analysis

![NBA Court](/Images/basketballcourt.png)

## Table of content

* [General info](#general-info)
* [Questions](#questions)
* [Parameters](#Parameters)
* [Data Sources](#data_sources)
    * [Preview](#preview)
* [Data Cleaning](#Data_Cleaning)
* [Data Visualization](#Data_Visualization)
* [Reports](#reports)
* [Setup](#setup)
* [Team](#team)

## General info

In this project, we analyzed the NBA history with the parameters of players age, the winning percentage of teams, PER (players efficieny rating), minutes played between 1986-2017 and used Python juyter notebook for creating codes.

## Questions

1. Can the Team Four Factor Rating of Basketball help in accurately determining the team’s win/success?
2. How does age of the player affect PER (Player Efficiency Rating)?
3. How does a player’s move (Top 10 only based on overall points) affect the new team’s winning percentage?
4. How to find top 50 or 100 players and their performance based on minutes played?

## Parameters

| Parameters | Against |
| --------- | -------- |
|Four Factors | Team win/success
|Age | Players Efficiency Ratings (PER)
|Players Move | New Teams winning percenatge
|Players Performance | Time

## Data Sources

### Four factors contribution to NBA Teams success

* (https://www.kaggle.com/drgilermo/nba-players-stats?select=Seasons_Stats.csv)

* (https://data.world/gmoney/nba-team-records-by-year/workspace/file?filename=Historical+NBA+Performance.xlsx)
  
### Additional sources

* (https://www.sportsgamblingpodcast.com/2020/04/20/nba-most-valuable-statistic/)
* (https://pypi.org/project/nba-api/)
Notes: Limiting our project between 1986-2017.

### Preview of the NBA data set

![Preview of our Data](/Images/playerData.png)

## Data Cleaning

* **complete_nba_data**: Merged team_Data and cross_ref csv files to work on first question and related visualizations and arranged the data between 1986 to 2017 and cleaned up player_Data and merged with the combined_team_data. 

* **age_player_data**: Create a dataframe using complete_nba_data  to find age effects PER (Player Efficiency Rating. Gathered the vehicle data from complete_nba_data and use "Year", "Player", "Age", "G", "MP","PER" as column. 

## Data Visualization

* **Impact of Four Factor Ratings on Winning Percentage**: Analyzed the impact of four factor ratings against the winning percentage and plot both parameters. Analyzed 2017 Team performance based on four factors compare with our prediction with actual winning percentage and found Difference in Winning Percentages.Statistical Analysis and table done on the resulting data.

* **Impact of age based on PER**: Analyzed age_player_data and found the quartiles, IQR, upper and lower bound to compare the players who would be on top 10 based on players median. 

* **Impact of players move based on points**: Analyzed players move based on points and winning percentage using player_points_data. Found top 10 players based on points and impact of their move to other team.

## Visualized four factors ratings impacts on winning percentage.

![Winning Percentage](./Images/Impact-Four-Factor-Ratings-on-Winning-Percentage.png)

* There is a positive correlation with Four Factors Ratings Air and Winning Percentage.

## Visualized ages impacts on Player Efficiency Rating (PER)

![Player Efficieny](./Images/ages-impacts-on-player-Efficiency-Rating(PER).png)

* There is a slightly positive correlation with ages and Player Efficiency Rating (PER).

### Setup

Required dependencies:

``` Python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
import scipy.stats as stats
```

### Team

Created by:

* [@jaybdhruv](https://github.com/)

* [@MondragB](https://github.com/MondragB)
* [@sammyschapps87](https://github.com/)
* [@DennisPSmith5676](https://github.com/)
* [@Kate-Yayla](https://github.com/)