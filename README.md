Research Question
Which individual performance metrics most accurately predict the likelihood of an NBA player winning the MVP award in a given season?

Description of Data
The data for this project was sourced from Basketball Reference, focusing on each season’s MVP statistics since the award's inception. We initially scraped seasonal stats for MVP players to capture their performance metrics over time. To build the non-MVP portion, we included the top 50 scorers from each season from 2000 to 2023 to ensure we analyzed only players with a realistic chance of competing for the MVP title, distinguishing between elite and MVP-caliber "hyper-elite" players.
In preprocessing, we encountered missing data in earlier seasons when certain stats weren't tracked, specifically steals and blocks before 1979 and three-point percentages before 1974. We imputed missing values for steals and blocks using the average MVP stats and applied a 40% penalty to field goal percentages for early three-point percentages, reflecting the historical context when three-point shooting was less common.
To address the class imbalance between MVP and non-MVP entries, we removed identifying columns like player names and teams and used SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic MVP entries. This resulted in a balanced dataset with 1178 MVP and 1178 non-MVP rows, including individual player metrics and a target label for MVP status (1 for MVP, 0 for non-MVP).

Features and datatypes
BLK (float64): Average blocks per game.
MP (float64): Average minutes played per game.
3P% (float64): Three-point shot success rate.
PTS (float64): Average points scored per game.
AST (float64): Average assists per game.
FG% (float64): Field goal success rate.
TRB (float64): Average rebounds per game.
G (int64): Total games played.
STL (float64): Average steals per game.
FT% (float64): Free throw success rate.

Group members: Jeremiah Swett, Henry Fischer, Kenny Ikeji, Nazih Baydoun
