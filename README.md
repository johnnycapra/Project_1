# Project_1

Project Proposal: Major League Baseball (MLB) Analysis
Team Members: Ian Morrison, Jacob Pos, Johnny Capra, Laura Dudley
Since baseball's beginning as a professional sport nearly 150 years ago, people 
have been recording meticulous details about each game in order to rank teams 
and quantify the performance of individual players. We are exploring a dataset of 
over 100 Major League Baseball (MLB) seasons to discover what broader trends 
and relationships can be found with such a long period of game records.
 
We are analyzing the following questions:
1) Is there really a "home team advantage"? In other words, is a team more likely 
to win if playing at their home stadium? Is there any difference between how likely
a team will win in the regular season vs. the playoffs in their home stadium? 
2) Are there patterns visible in the data that show the differences in how teams 
with the most playoff games score vs. the teams with the fewest playoff games?
3) Do global or economic events affect the number of games played in a season, 
and in what way?
Data Sources:
https://sportsdata.io/developers/api-documentation/mlb#/sports-data-feeds/
league-feeds
https://projects.fivethirtyeight.com/mlb-api/mlb_elo.csv
https://projects.fivethirtyeight.com/mlb-api/mlb_elo_latest.csv

----

Question 1:  
Is there really a "home team advantage"? In other words, is a team more likely to 
win if playing at their home stadium? Is there any difference between how likely a 
team will win in the regular season vs. the playoffs in their home stadium? 
The first question we examined is whether a team really has an advantage when 
playing in their home stadium: the “home team advantage.” The phrase is pretty 
common in our language, but is it just observation bias by excited fans watching 
their home team play? We examined this question in two ways, using the scores 
for every game played each season from 1910 through 2019 recorded in a dataset
from fivethirtyeight.com (https://projects.fivethirtyeight.com/mlb-api/mlb_elo.csv).
By calculating the percentage of games won by home teams in each season 
plotting it as a line graph (overall_fig2.png), we were able to see that the 
percentage of home team wins was over 50% for every year except 1917. We 
then created a histogram to display the frequency of each home win percentage 
in our dataset (overall_fig1.png). As you can see from this visualization, the 
majority of home team win percentages for all years is between just over 52% and
just over 55%. 
This indicates a slight but noticeable advantage to the home team. Looking back 
at the line graph, we can see that the past 40 years of games has consistently 
stayed within these values, while earlier seasons account for some of outlying, 
less frequent values (49%-50% and 56%-57%).
The next 4 visualizations were created the same way, but specifically for regular 
season home team wins (reg_fig1.png and reg_fig2.png) and playoff home team 
wins (playoff_fig1.png and playoff_fig2.png). As you can see, the regular season 
very closely follows the previous visualizations of the overall home team wins, 
which is to be expected because the majority of games are played during the 
regular season. 
There is greater variability in the home team wins for the playoffs, with the most 
frequent total home team win percentages hovering around 50%, plus or minus a 
few tenths of a percent. This greater variability is most likely due to the smaller 
dataset, as relatively few playoff games are played in a season. 
Based on these visualizations, we can conclude that the idea of a “home team 
advantage” holds true as an observation for most games played, but not during 
the playoffs.

------

Question 2:
Are there patterns visible in the data that show the differences in how teams with 
the most playoff games score vs. the teams with the fewest playoff games?
Our next question compares the scores from teams that have been played many 
playoff games against the scores from teams that have played in only a few 
playoff games, to see if there is a pattern or a visible difference in these two 
groups. Again, using the dataset from fivethirtyeight.com 
(https://projects.fivethirtyeight.com/mlb-api/mlb_elo.csv), we first determined the 
top 5 and bottom 5 playoff teams by counting the number of playoff games 
played from 1910 through 2019 and selecting the highest and lowest counts, 
respectively.
Next, we created a box plot of each team’s score, grouped into the top 5 teams 
and the bottom 5 teams (box_top_5 and box_bottom_5). These box plots display 
the following statistical information about each team’s playoff scores:
-The mean (average) score, represented by the “x” in the box.
-The median score, shown as a horizontal bar inside the box.
-The upper and lower quartiles (75th percentile & 25th percentile) of their scores, 
displayed as the top and bottom of the box. The distance between the box’s top &
bottom reflects the statistical dispersion (interquartile range) of the scores. 
-The minimum and maximum values within 1.5 times the statistical dispersion, 
shown as vertical lines (whiskers) coming out of the box.
-Any outlier scores, which are scores outside the minimum and maximum values 
calculated above. These are represented by red dots on our visualizations.
The notable differences between the top 5 teams’ box plot and the bottom 5 
teams’ box plot are the box sizes and the number of outlier scores. The top 5 
teams have very similar sized boxes in the box plot, which would indicate a similar
degree of variability between these teams in their playoff game scores. The top 5 
teams also each have at least one outlier score above the maximum value, which 
don’t fit the typical pattern of scores. Together these seem to indicate a common 
trait of these teams is both a consistent and competitive ability to score high in 
their playoff games.
The bottom 5 teams have less consistent boxes, and only have a single outlier 
score above the maximum value, and have a single outlier low score as well. The 
maximum values indicated by the top whiskers are also lower in general than the 
maximum values of the top 5 teams. Together, this seems to indicate a lower 
scoring ability for these teams.

------

Question 3:
Do global or economic events affect the number of games played in a season, and
in what way?
Our final question was inspired while exploring a second data source 
(https://sportsdata.io/developers/api-documentation/mlb#/sports-data-feeds/
league-feeds). 
Major League Baseball comprises two leagues – the National League (NL) and the 
American League (AL). This line graph (wins_per_league_covid.png) compares the 
number of total wins for each league for the 2017 to 2023 seasons. As you can 
see, the leagues are very closely matched, however the dip in the number of wins 
for both leagues in 2020 is quite dramatic. Due to the COVID-19 pandemic, the 
2020 season had fewer than half of the total games originally scheduled for the 
season, which lead us to wonder what other events may have affected baseball 
throughout its long history as a professional sport. 
Returning to our primary dataset 
(https://projects.fivethirtyeight.com/mlb-api/mlb_elo.csv), we created a line graph 
showing the total number of games played each season, starting with the earliest 
(1871) through the latest (2021) in this dataset. The resulting visualization 
(history_matches.png) reveals several other seasons in which significantly fewer 
games were played. 
There’s quite a bit of variability in the number of games played during the first 
three decades, which can be attributed to the infancy of the sport’s organization, 
however the trend is an increase in the number of games per season over time. 
Then we get to the first dramatic dip in our graph, 1900. This marks the end of the
early history of baseball in America, in which there were multiple leagues, to the 
two-league system (NL & AL) we have now, established in 1901. 
The number of games played in a season during the period of 1904 to 1960 is 
incredibly stable, with just one dip during 1918. Initially, we believed this to be an 
effect of the 1918 Influenza pandemic (so-called “Spanish Flu”), but it was actually
World War I. The “Work or Fight” rule, issued in 1918, required men to either work 
in jobs supporting the war effort, or be drafted. As the deadline for compliance 
was mid-season (July), the MLB requested and was granted an extension, with the 
agreement that the season would be shortened.
Following this stable period, the number of games trends upward again until 1972,
when we see another dip, which was caused by a player strike. The strike 
continued past the season’s start date, causing the first 1 ½ weeks’ games to be 
cancelled. 
Another player strike in 1981 caused an even more dramatic dip in the number of 
games played during that season. Unlike the 1972 player strike, which lasted a 
little under 2 weeks at the beginning of the season, the 1981 player strike 
continued for 2 months in the middle of the season. This led to approximately 38%
of the season’s games being cancelled.
Yet another player strike occurred in 1994, which was the longest strike in MLB 
history and caused the 1994 regular season to be ended early and the cancelation
of the World Series for that year.
The final and most dramatic dip was, of course, in 2020, and the height of the 
COVID-19 pandemic. Indefinite postponements, positive test results in players, 
and restrictions on travel and gathering all contributed to the drop in 2020’s total 
games by approximately 2/3rds the normal count.
Despite the effects of a war, multiple player strikes, and global pandemic reflected
in this visualization, it’s notable that many other national and global crises 
happened during this period of over 150 years which didn’t affect the baseball 
season at all, at least in terms of the number of games played.

References:
1900:
https://en.wikipedia.org/wiki/Major_League_Baseball#Founding 
https://en.wikipedia.org/wiki/
History_of_baseball_in_the_United_States#Rise_of_the_major_leagues
1918:
https://time.com/5903122/pandemic-world-series/
https://www.axios.com/2020/04/06/coronavirus-spanish-flu-baseball-1918
https://en.wikipedia.org/wiki/1918_Major_League_Baseball_season
1972:
https://en.wikipedia.org/wiki/1972_Major_League_Baseball_season
https://en.wikipedia.org/wiki/1972_Major_League_Baseball_strike
1981:
https://en.wikipedia.org/wiki/1981_Major_League_Baseball_season
https://en.wikipedia.org/wiki/1981_Major_League_Baseball_strike
1994:
https://en.wikipedia.org/wiki/1994_Major_League_Baseball_season
https://en.wikipedia.org/wiki/1994%E2%80%9395_Major_League_Baseball_strike
2020:
https://en.wikipedia.org/wiki/2020_Major_League_Baseball_season