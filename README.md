# Fantasy_Football_AI
A project to leverage data analysis and machine learning to make informed fantasy football team selections

## PROJECT AIMS and Challenges
**Problem 1 -**: What is the highest scoring team, budget permitting, that could have been set and left on gw1? i.e. given the current points totals for all players, which team, when selected in gw 1 would give you the highest possible return at the current date?

**Problem 2**:  The solution to this problem will inform the final AI selector. What is the best possible manager result when viewing the history of current season gameweeks. i.e. which sequence of teams, when selected within the rules of the game, would provide the maximum possible points haul at the current date?

**Problem 3**: Select the best gw squads as if you were choosing for the first time in each gameweek. So gw you have a budget of £100 and a blank canvas: pick your squad. Gw2 you have a squad of £100M and a blank canvas: pick your squad... etc etc



## Directory of dataframes

1. season_squads.csv: this is the latest full set of gw squads base on the problem two approach
2. players.csv: this set hold all player scoring data from the "elements" endpoint for every gameweek.
3. basic_player_info.csv: this set holds basic info for every player including team, element_type(position) and id
4. cumulative.csv: this set holds cumulative points totals for each player on a rolling gameweek basis. 
5. basic_prepared_players: this set shows all players with the latest points tally, gw1 cost and latest value metric.
6. team_colors.csv: This holds hex colors for all team shirts and shorts.. this is used for the visualisations. 

## Notebook narrative and flow
1. Weekly_calls.ipynb brings in the latest data from FPL endpoints and generates the base csv files for the project
2. gw1_functions.ipynb will generate the best team that could have been drafted at gw1 given latest points scored as set out in problem 1
3. season_funcs2.ipynb will generate the season_squads dataset which shows all the squads selected for every gameweek based on the rules set out in problem 2. 
4. Team_Colours.ipynb is a visualisation notebook to display a team in formation with team colors and player names etc. If you scroll to the end of the notebook there is a standalone function that takes in the season_squads.csv set. If you call the function you will be asked which gameweek squad you want to view. Hit enter to see your squad in team formation. 