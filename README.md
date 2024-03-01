# 2024_Draft_Report_SQL
In Fantasy Football, the preseason draft is where each member selects theirt team.  Round by round, players have a minute and a half to select the best player to fit their team.  Without preperation and a great strategy, the one minute and thirty seconds feels like ten seconds. The key to winning fantasy football begins with winning weekly matchups. The 2024 Draft Report creates KPIs, from data in the fantasy football database,   to identify players producing the highest weekly points on the most consistant basis.  A report will be created identifying and ranking the top 150 players by position.  The data will also be imported into Tableau where a Player Draft Card will be created allowing a quick reference guide to each players KPIs. 

## SQL Skills Used:
- Creating tables and inserting data into tables using UPDATE SET
- RANK, DENSE_RANK, ROW_NUMBER function
- Window functions
- CASE statements
- FILTER clause to create Pivot Tables
- UNION clause to combine multiple tables
- Using the Top 6 SQL functions to aggregate and filter data

  ##KPI's used to rank players
  ### Total and Average fantasy points from 2023 season
  - Understanding the total points gives insight into a players top potential\
  - Average points provides a better measure of a players weekly point production
      - Average helps reduce outliers from a week where a player produced uncharacteristic results
   
### Percentile Rank
- Identifies the league average fantasy points per week for each position
- A CASE statement then ranks players average weekly point production and places them in the following categories
      - MAX - produced the highest average points per week for that position group in the 2023 season
      - Top 5% - had average points per week in top 5%
      - Top 10% - had average points per week in top 10%
      - Top 25% - had average points per week in top 25%
      - Above Average - had average points per week above average for that position group
### Percentile Percent
- Sums total amount of weeks in 2023 where a player's point value was above average or higher
- A percentage is then calculated dividing the total weeks a player's points ranked in a category by the total weeks of the season
- A high percentile percent indicates the the probability that a player's score will help win the weekly matchup

### Analyzing KPIs
- Below you will see the top 10 defenses in 2023 based off of the KPIs above.
      -I would prefer to draft Baltimore over Dallas.
          - Their average and total point values are very close.
          - The 18% higher percentile_percent for Baltimore would be the reason why I would choose them.
    - Buffalo and New York Jets are seperated by 5 total fantasy points and 8% percentle_percent
          - I know these two teams play each other twice a year and Buffalo's offense puts up many points, more that the Jets
            
![Screenshot (160)](https://github.com/bhammy27/2024_Draft_Report_SQL/assets/154477061/89e9db3d-b5fa-43fa-84fc-f4dac63b8c9e)
          - I would draft Buffalo based off of avg_fpts

  
      
