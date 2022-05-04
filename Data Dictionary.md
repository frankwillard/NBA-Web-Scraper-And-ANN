Data collected from Basketball Reference, many variables are thus described based on [Basketball Reference Glossary](https://www.basketball-reference.com/about/glossary.html)

The initial data was scraped 3/18/22 by me, and was input into Basketball Reference. Basketball Reference is partnered with SportRadar (the official statistics provider of the NBA), in providing the official NBA data for current-season data$^1$. It is well known for being thorough and accurate.

The 2022 data was scraped 5/03/22 (after the regular season ended but before the playoffs ended).

## Data Dictionary

|variable         |description |
|:----------------|:-----------|
|Year        | Year that the season occurred. Since the NBA season is split over two calendar years, the year given is the last year for that season. For example, the year for the 1999-00 season would be 2000. |
|Team        | Name of NBA Basketball Team |
|W        | Wins in a season|
|L        | Losses in a season |
|PW        | Pythagorean Wins; the formula is G * (Tm PTS14 / (Tm PTS14 + Opp PTS14)). The formula was obtained by fitting a logistic regression model with log(Tm PTS / Opp PTS) as the explanatory variable. Using this formula for all BAA, NBA, and ABA seasons, the root mean-square error (rmse) is 3.14 wins. Using an exponent of 16.5 (a common choice), the rmse is 3.48 wins.  |
|PL        | Pythagorean Losses; the formula is G - W Pyth. |
|MOV        | Margin of Victory; the formula is PTS - Opp PTS. |
|SOS        | Strength of Schedule; a rating of strength of schedule. The rating is denominated in points above/below average, where zero is average. A positive number indicates a harder than average schedule. Doug Drinen, creator of Pro-Football-Reference.com, wrote a thorough explanation of this method. |
|SRS        | Simple Rating System; a rating that takes into account average point differential and strength of schedule. The rating is denominated in points above/below average, where zero is average. Doug Drinen, creator of Pro-Football-Reference.com wrote a thorough explanation of this method. |
|ORtg        | Offensive Rating (available since the 1977-78 season in the NBA); for players it is points produced per 100 posessions, while for teams it is points scored per 100 possessions. This rating was developed by Dean Oliver, author of Basketball on Paper. Please see the article Calculating Individual Offensive and Defensive Ratings for more information. |
|DRtg        | Defensive Rating (available since the 1973-74 season in the NBA); for players and teams it is points allowed per 100 posessions. This rating was developed by Dean Oliver, author of Basketball on Paper. Please see the article Calculating Individual Offensive and Defensive Ratings for more information. |
|NRtg        | Net rating: an estimate of point differential per 100 possessions (ORtg - DRtg) |
|Pace        | Pace Factor (available since the 1973-74 season in the NBA); the formula is 48 * ((Tm Poss + Opp Poss) / (2 * (Tm MP / 5))). Pace factor is an estimate of the number of possessions per 48 minutes by a team. (Note: 40 minutes is used in the calculation for the WNBA.) |
|FTr        | Number of FT Attempts per FG Attempt |
|3PAr        | Percentage of FG Attempts from 3 Point Range |
|TS%        | True Shooting Percentage; the formula is PTS / (2 * TSA). True shooting percentage is a measure of shooting efficiency that takes into account field goals, 3-point field goals, and free throws. |
|OeFG%        | When team is on offense (what percentage the team shoots): Effective Field Goal Percentage; the formula is (FG + 0.5 * 3P) / FGA. This statistic adjusts for the fact that a 3-point field goal is worth one more point than a 2-point field goal. For example, suppose Player A goes 4 for 10 with 2 threes, while Player B goes 5 for 10 with 0 threes. Each player would have 10 points from field goals, and thus would have the same effective field goal percentage (50%). |
|OTOV%        | When team is on offense (turnovers committed): Turnover Percentage (available since the 1977-78 season in the NBA); the formula is 100 * TOV / (FGA + 0.44 * FTA + TOV). Turnover percentage is an estimate of turnovers per 100 plays. |
|ORB%        | Offensive Rebound Percentage (available since the 1970-71 season in the NBA); the formula is 100 * (ORB * (Tm MP / 5)) / (MP * (Tm ORB + Opp DRB)). Offensive rebound percentage is an estimate of the percentage of available offensive rebounds a player grabbed while he was on the floor. |
|OFT/FGA        | When team is on offense (team shooting): Free throws per field goal attempt |
|DeFG%       | When team is on defense (what percentage the team allows opponent to shoot): Effective Field Goal Percentage; the formula is (FG + 0.5 * 3P) / FGA. This statistic adjusts for the fact that a 3-point field goal is worth one more point than a 2-point field goal. For example, suppose Player A goes 4 for 10 with 2 threes, while Player B goes 5 for 10 with 0 threes. Each player would have 10 points from field goals, and thus would have the same effective field goal percentage (50%). |
|DTOV%       | When team is on defense (turnovers forced): Turnover Percentage (available since the 1977-78 season in the NBA); the formula is 100 * TOV / (FGA + 0.44 * FTA + TOV). Turnover percentage is an estimate of turnovers per 100 plays.|
|DRB%       | Defensive Rebound Percentage (available since the 1970-71 season in the NBA); the formula is 100 * (DRB * (Tm MP / 5)) / (MP * (Tm DRB + Opp ORB)). Defensive rebound percentage is an estimate of the percentage of available defensive rebounds a player grabbed while he was on the floor. |
|DFT/FGA        | When team is on defense (opponent shooting against team): Free throws per field goal attempt |
|Arena        | Arena in which season's home games were played |
|Attend.        | Total number of people at games during season |
|Playoffs        | Indicator variable representing whether team made playoffs or not in a season |
|W/L%        | Proportion of games won Wins / (Wins + Losses) for season|
|Losing_season        | Indicator variable representing whether team had more losses than wins (or not) in a season |
|Champion        | Target: Indicator variable representing whether team won the championship or not in a season |
|won_last        | Indicator variable representing whether team won the championship in the previous season or not |
|won_last_3        | Indicator variable representing whether team won the championship in any of the previous 3 seasons or not |
