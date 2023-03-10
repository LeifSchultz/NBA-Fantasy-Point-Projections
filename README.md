# NBA-Fantasy-Point-Projections

## The Goal
In this project My goal is to predict basketball players fanatasy points on any given night and use those predictions to pick players that will make a winning  Draftkings lineup. Draftking fantasy points are calculated by the players stats for the night including their points scored, rebounds, assists, steals, blocks, and turnovers. By predicting each players fantasy point for the slate I could then build a Draftkings linup with the highest project fantasy point score that would then, ideally, win money


## The Data
I used data from Basketabll-reference.com and webscraped the stats of every player from every game int the last 3 years. I also webscraped team statistics like pace of play and defensive rating as well.


## The model
After collecting and cleaning the data, I tested a variety of different machine learning and modeling techniques. Eventually I settled on a gradient Boosting model
that had an r squared of .7 with a low mean absolute value score of 5.01. Now that I had a model capapable of predicting a players fantasy point, the next step was creating the best draftkings lineup that didn't violate any of the lineup conditions; including have exactly nine players, filling all the postional eligibility requirments, and staying below the $50,000 slaary cap. I was able to test 7 of the optimal lineups my model produced by entering them in the Draftkings 50/50 double up contest, where the top fifty percent of lineups will double up on their entry fee and the bottom fifty percent will lose their money. In the end my model was able to win 4/7 weekly contests, maintaining a weekly profit.



### Below are the functionalities of the 5 Jupyter notebooks this project consists of to achieve its goal of projecting player fantasy points and creating an optimal draftkings lineup based on those predictions.


Data Scraping.01.ipynb scrapes games data from Basketball-Reference.com and salary and position information from RotoGuru.

Data Preparation.02.ipynb merges and cleans tge data from to prepare it for modeling

Modeling Historical Data.03.ipynb constructs a baseline model with simple average along with additional model variations and improvements until I reached a final model that is saved to be used for new data.
  lr_model.pkl contains the trained final model to use for predicting new data

Visualizations.04.ipynb creates some visualizations and bar graphs to illustrate the model's performance and feauture differences.

Salary Scrape and Lineup Construction.ipynb scrapes daily salary information. Then uses Genetic Algorithms to select best combinations of players on a given set of games and predictions.
