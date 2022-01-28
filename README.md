# SyPy Bowl Analysis

Team 2: Austin Rodriguez, John Leelike, Michael Cordes, and Troy Prata


# Summary

This repository contains an analysis of NFL preseason favorites and corresponding Super Bowl Outcomes and our journey to the results.

## What is the best pre-season betting strategy?
The first question we considered is which of three betters would yield the best results if all three picked a certain strategy and bet across a certain period.  The three strategies are as follows:

 1. Strategy 1 bets $100 on the top preseason Super Bowl favorite
 2. Strategy 2 bets $50 on each of the top two preseason Super Bowl favorites
 3. Strategy 3 bets $20 on each of the top five preseason Super Bowl favorites

The team individually voted and the results are as follows:

 1. Strategy 1 - 50%
 2. Strategy 2 - 25%
 3. Strategy 3 - 25%

Winning strategy is Strategy 1

## How do we obtain the data needed?

After our first question, we needed to ask, how would we obtain this data.  We discovered a website called pro-football-reference.com that housed all the data in a format that allowed for export to a .csv.  The only problem was the website did not have page that presented an aggregate view.  We were able to create an empty data frame and run a for loop that called out to the website and pulled each year between 1990 and 2022.

We had the preseason favorites but needed a list of Super Bowl winners. We located a list of Super Bowls by year with the necessary information.  

We also wanted to explore the number of Super Bowl games played at each location.  We located a csv with a listing of every Super Bowl locations. 

## How would we prepare the data obtained?

We created multiple data frames that housed our preseason Super Bowl odds, the Super Bowl outcomes, and Super Bowl locations.

Using the large Super Bowl odds data frame, we created a data frame for each strategy that only contained the team(s) the strategy bet on for each year.  Once we had each strategy data frame created, we needed to calculate if the strategy won any of the bets each year.  This was solved by defining functions that ran loops against the strategies teams and if the team was the winner what were the odds of the bet plus return the original bet. 

## Are there any trends or correlations within the strategies 

We found that the Strategy 1 out performs Strategy 2 and 3.  Strategy 2 outperforms Strategy 3 but not Strategy 1. Strategy 3 does not outperform Strategy 1 or Strategy 2.

We also developed scatter plots for each Strategy and compared the winning teams to the strategy's results.  The 2002 Bucs Super Bowl presented the highest return for Strategy 1.  The Pittsburg Steelers 2008 returned the most for Strategy 2 and Strategy 3

## Where were the most Super Bowls Played?

Using a mapbox API, we were able to visualize the density of Super Bowls played in each location.   New Orleans played host to the most Super Bowls during our review period (1990 - 2022).
