# NHL-Undervalued-Forwards-Equation
This code is built to sift through 3 years of NHL regular-season data to find a correlation in advanced analytics among forwards who saw a positive change in points from the previous season to the next by 0.2 points per game (PPG). In order to qualify for this data field, the filters below have been applied to clean the data.
1. Forward in the NHL
2. Previous season: the forward must have played> 30 regular-season games
3. Previous season: the forward must have played > 250 minutes of 5v5 ice time

The goal of this project is to find a correlation in analytics to build a weighted predictive formula that helps General Managers find undervalued players who, given "proper opportunity," can produce 0.20 PPG more the following season, equating to approximately 16 more points in an 82-game season. 

"Proper Opportunity" is defined in this project as a player receiving an adequate amount of opportunity in playing time and role, whilst fitting into the team's specific systems and developing chemistry with his linemates. Below is a list of variables that equate to creating a "proper opportunity" scenario for the player.
1. Forward plays within the team's Top 9 for the given season
2. Forward's season average of Time on Ice (TOI) is around 16 minutes per 60 minutes (Full NHL game length)
2b. If a forward's average TOI equates to 16 minutes or more, then the player must receive 1:30 to 3 minutes more TOI  for more opportunity
3. Forward must see a positive change in Power Play TOI by 25 seconds from the previous season's average
4. Forward fits into the team's play style
5. Forward develops chemistry with linemates
6. Forward sustains health
7. Forward sustains previous season's averages in analytical fields present in the formula

The filtered data found 71 occurrences of a positive change in PPG of 0.20 from the previous season
70 players total saw the increase
1 player saw a change twice over the years evaluated: Martin Necas

Upon review of the data, strong correlations were found among 6 previous-season advanced analytics and the 70 players that saw the positive change in PPG by at least 0.20. Listed below are the 6 analytics found and also used in the equation.
1. 5v5 expected goals - actual goals per 60 minutes
2. 5v5 primary points per 60 minutes
3. 5v4 minutes per game
4. Overall points per game
5. 5v5 high danger shots per 60 minutes
6. 5v5 on-ice expected goals percentage
- These six statistics are each individually weighted within the equation.
- These are weighted as regression coefficients.
  
The equation is 100/1+e^-s
e = a fixed number for conversion found through the data
-s = sum of player statistics and predetermined weights for the given 6 statistics

For evaluation purposes, to give a prediction for a given season, the equation uses the previous season's statistics because this is a predictive model. 
- 2026-27 Season Prediction is based on 2025-26 Season Data
- 2025-26 Season Prediction is based on 2024-25 Season Data
- 2024-25 Season Prediction is based on 2023-24 Season Data
Note that a good equation score, ranking in the 25th percentile of the data field, does not result in a guaranteed positive change in PPG the following season, as proper opportunity must come to fruition as well. 
Strongest candidates exhibit scoring in the 90th percentile of the field equation score average while having room to grow their average TOI from the previous season 
