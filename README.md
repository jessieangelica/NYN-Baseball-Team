### Data Analysis of New York Mets (2004–2012)
Data analysis on the New York Mets (teamID = 'NYN') baseball team from 2004 to 2012 using sabermetrics concepts like the Pythagorean Expectation to evaluate team performance.

### Load and Filter Team Data
- These libraries support data manipulation (pandas, numpy), statistical analysis (scipy, statsmodels), and visualization (matplotlib, seaborn, plotnine).
- Loads team statistics from Teams.csv.
- Returns the shape (rows, columns) of the dataset.

### Filter New York Mets (teamID = 'NYN') from 2004 to 2012
- Filters the Mets' seasons from 2004 to 2012.
- Selects columns for year, teamID, Wins (W), and Losses (L).
- Displays the selected columns.

### Add Runs Data: RS and RA
- Perform the same task without creating temporary data frames mets and my_mets:
- Adds Runs Scored (R) and Runs Allowed (RA).
- filter and extract specific data from the full Teams dataset, focusing only on the New York Mets team (teamID == 'NYN') between the years 2004 and 2012
Note :
- R: Runs Scored
- RA: Runs Allowed.

### Calculate Actual Winning Percentage
###  Calculate Pythagorean Expected Winning Percentage
- This predicts a team's expected win % based on run differential. 
- In other words, it measures how many more (or fewer) runs a team scores than it allows.
- Run differential gives a strong indication of team strength.

### Expected Wins (W_hat)
Converts expected win % to total expected wins. It is taking the predicted winning percentage (how often a team is expected to win), and turning it into an actual number of wins over a full season.

### Compare Actual vs Expected Performance
- Lists seasons where Mets overperformed or underperformed relative to expectation.
- Sorts seasons by actual win percentage from best to worst.

### Compute Residual (Difference between Actual and Expected Wins)
- Positive Diff: Team won more games than expected.
- Negative Diff: Team won fewer than expected.

### Summary Statistics
- This tells you how the team performed overall:
- Their average win count was about 81 wins per year.
- Their best season had 97 wins, and the worst had 70.
- The data has moderate variation (std ≈ 9.1).

Assess whether the team overperformed or underperformed expectations.
- num_years: Number of seasons.
- total_W, total_L: Total wins and losses.
- total_WPct: Overall winning percentage.
- sum_resid: Sum of residuals (actual wins - predicted wins) over those years.

Adds a gm column indicating who the General Manager (GM) was for each season:
- Duquette for 2004
- Minaya for 2005–2010
- Alderson for 2011–2012

### Creates performance summaries by GM:
- Total wins/losses.
- Overall winning percentage.
- Sum of residuals (how far off the actual win count was from expected).
Sorting by sum_resid shows which GM oversaw more "lucky" or "unlucky" seasons.

Interpretation :
- All three GMs had teams that underperformed expectations based on run differential.
- Alderson's teams were closest to expectation (only -1.3 wins off).
- Minaya's teams played the most seasons and had the most total wins, but also underperformed most compared to their expected win total.

### Compare All MLB Franchises (2004–2012)
Repeats the same logic for all MLB teams, calculating:
- Predicted win % and win total using Pythagorean expectation.
- Difference between actual and expected wins (Diff).

### Group by Franchise and Summarize
Shows the 6 most underperforming franchises (negative residuals) — i.e., teams that lost more games than their run statistics predicted.

- How many seasons each franchise had.
- Their total wins, losses, and win percentage.
- How much they over/under-performed expectations (sum_resid).

### Summary
- mets_summary : Summary stats for Mets from 2004–2012
- gm assignment	: Label each season with the GM in charge
- grouped by GM :	Evaluate GM performance based on wins and residuals
- mets_ben2 creation :	Prepare similar metrics for all MLB teams
- grouped2 analysis	: Rank franchises by performance versus Pythagorean expectations

###  Conclusion :
- num_years: All the teams have data from 2004 to 2012, so the value is 9 for each tea
- total_W:This is the total number of wins for each team during the 9 years.
- total_L:This represents the total number of losses for each team during the same period.
- total_WPct:It tells you how successful each team was overall. The win percentage is a value between 0 and 1, with a value closer to 1 indicating a better performance.
- sum_resid: the difference between the actual wins (W) and the expected wins (W_hat). A negative value means the team underperformed, while a positive or smaller negative value means they were closer to or exceeded expectations.
  - Toronto Blue Jays (TOR): They underperformed by a significant margin, winning 29 fewer games than expected based on their run differential.
  - Atlanta Braves (ATL): They underperformed by 24 fewer games than expected.
  - Colorado Rockies (COL): They underperformed by about 22 games.
  - Chicago Cubs (CHC): They underperformed by about 14 games.
  - Cleveland Indians (CLE): indicating a relatively smaller underperformance compared to the others.
  - New York Mets (NYM): They underperformed the least in this group, but still below expectations.
  

