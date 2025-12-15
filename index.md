# Evaluating NBA Lottery Picks Using Career Performance

**Group Members:**  
Ali Efe Isik, Djordje Lazarevic  
   
[Google Colab](https://colab.research.google.com/github/aliefe9/Evaluating_NBA_Lottery_Picks_Using_Career_Performance/blob/main/nba_final.ipynb)
**Introduction**  
This project looks into the career success of NBA players who were selected in the first 10 places in the NBA draft. We used a dataset from kaggle that contains detailed statistics from multiple NBA seasons, and our research question is: “How successful have first 10 draft picks been, and which teams made the most draft mistakes?”
We evaluated player performance using the Performance Index Rating(PIR), a generally used efficiency metric in the basketball world outside the NBA, that incorporates all positive statistical contributions and subtracts negative contributions. As it summarizes on-court impact in a single number, it is a good comparison number between players.
The goal of the analysis is to compare PIR between players and identify which players underperformed or outperformed in their careers. Our approach involved data cleaning, calculating PIR from the box score data, and generating summary tables and visualizations to compare performance.
Issues that we encountered with the data is that we had to filter the data so we only have one row for each player, as there were some duplicates. Also, the dataset had some data outside the NBA, so we had to filter it to be based only on the NBA players.

**Methods and Results**  
The dataset was imported from kaggle and contains NBA data since 1999 including biographical information about players, draft position and box-score data. We filtered data so it only includes players drafted between picks 1-10, and we removed players born before 1965, as our dataset is since the 1999 season, those players are out of their prime level of play, so it is unfair to count them in this process.
PIR was calculated using the standard formula:
PIR=(points+rebounds+assists+steals+blocks)−[(FGA−FGM)+(FTA−FTM)+turnovers].
The final dataset we used for analysis contained the player, average PIR, team that drafted a player and average minutes(MPG). We used this in order to create visualizations and to separate players into clusters of efficiency. The visualizations look like this:

<iframe src="fig1.html" width="100%" height="500" frameborder="0"></iframe>
<iframe src="fig2.html" width="100%" height="500" frameborder="0"></iframe>
