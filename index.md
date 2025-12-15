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

<iframe src="player_performance_kmeans.html" width="100%" height="500" frameborder="0"></iframe>
<iframe src="underperforming_lottery_picks.html" width="100%" height="500" frameborder="0"></iframe>

From the first visual we can see that there is a positive correlation between minutes played and PIR, and that the PIR is centered around 10-15. In order to get clusters, we used kmeans clustering, and each cluster is represented by a different color. There is a solid amount of players averaging PIR above 15, meaning that there were some draft picks that outperformed expectations and became great players, which was our first question.
From the second visual we got the answer to the second question, and the worst draft team is Sacramento Kings, who had 8 top 10 draft picks who underperformed for their career, and average is 2.93 underperformed players for the team.

**Conclusion**
This analysis shows that the performance of top-10 picks varies widely, with a positive correlation between MPG and PIR, showing that players who were given a chance and played more, usually performed better than the players who did not get a proper chance to play. Taking in account that we analyzed only top-10 draft picks, and the overall distribution of their PIR seems to be similar to the distribution of all players, there is no significant difference between the players drafted in the top-10 and other players, excluding stars of the League.
For the second question, which team has had the most “bust” picks, answer is clear, and that is Sacramento Kings. Furthermore, and as a limitation to this question, not every franchise exists the same number of years. For example, Sacramento Kings were founded in 1985, and Denver Nuggets were founded in 1967, giving them more overall draft picks than the others. This makes the case even worse for the Kings, as they had more bad draft picks than some teams that have been in many more drafts, simply because they exist longer.
Also, the limitation to this study and “player success” is that PIR is an accurate measure of statistics of a player, but it does not describe a player's impact on the court directly. Players for whom defense is a specialty, they might have lower PIR numbers, but their impact on the court is simply not measurable by simple statistical numbers.
Some areas of further study would be that we incorporate team’s success where a certain player is playing, so we can have an additional measure of players success. On top of that, an obvious study from this would be to compare draft picks in the first round, for example, picks 1 through 15 and picks 16 through 30, and to see if there is a clear difference between them.

