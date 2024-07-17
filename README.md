# Winter_Quarter_Baseball_Sports_Analytics_Project_2024

Upload Data Visualizations and R Coding onto Github to display our findings.

This project will analyze MLB player draft data from 2018 to 2020 as tasked by client. The goal is to predict career WAR value by draft characteristics such as round, draft pick number, signing bonus, and by career minor league data. 

We initially analyzed pitcher WAR values by where they were drafted from 2018 to 2020 and their WAR value. With data mining techniques, we determined what factors were significant and which model predicted the highest classifircation accuracy rate.

# Terminologies:
- WAR: Wins Above Replacement
- Signing Bonus: Players' First signing bonus by team they are drafted from

# Predictor Variables (Source baseballr)
Baseball Draft Information
- pick_round
- pick_number
- person_draft_year
- person_pitch_hand_description
- team_name

Player Demographics
- home_city
- home_state
- home_country
- year
- month
- day
- person_birth_city
- person_birth_state_province (Since players may come from outside of US)
- person_birth_country
- person_height
- person_weight

School Information
- school_name
- school_state
- school_country

# Predictor/Response Variables (Personal)
- Q_status: quartile of signing bonus compared to rest of respective draft class
- war_status: define by positive, negative, or no WAR value (indicating that player has yet to debut)

# Process
Our project utilized the baseballr library data and conducted data cleansing to organize the data and then apply these methods below. I utilized these methods below to display which accuracy rates were the highest and which predictors we found to be significant.

- Decision Tree (No Pruning) 
- Decision Tree (Cross Validation) 
- Random Forest (All Predictors)
- Random Forest (15 Predictors) 
- Random Forest (6 Predictors) 

We utilized classification trees as our predictors included categorical variables such as prospect height, draftet team, and state names in the database. After finding the accuracy rates, we were able to rank which model performed the best and its score as well.

Model Accuracy:
- Random Forest (6 Predictors) 86.6% / Random Forest (All Predictors) 86.6%
- Random Forest (15 Predictors) 86.35%
- Decision Tree (Cross Validation) 80.89%
- Decision Tree (No Pruning) 80.65%

We notice that Random Forests with all or 6 predictor variables performed the best compared to other models. All the models performed highly but Random Forest model performed better than Decision Tree models. 

# Significant Predictors
![var_implot_final_model](https://github.com/NathanKim0107/Winter_Quarter_Baseball_Sports_Analytics_Project_2024/assets/128879072/06cac7b5-c90a-45e6-b662-ef6229621d66)

In this plot, we notice that some of the most important predictors were the pick_number, team_name, person_birth_city, person_Weight, home_city, and school_name. Although we are aware of what the significant factors are, it is important to display why these variables are important in determining a players' chance of reaching the MLB stage and ending their career with a positive WAR value.

# Player Round vs WAR Status
![Player Draft Round vs WAR Status Chart](https://github.com/NathanKim0107/Winter_Quarter_Baseball_Sports_Analytics_Project_2024/assets/128879072/51d8ec80-b09b-4d72-824d-905acb916ea3)
In this chart, we notice how there are many players who are unable to move onto the MLB stage and those who attained a negative career WAR value. When analyzing the chart, we notice that there is a right skew behavior for all three statuses. Especially, for Positive Career WAR, we observe that the majority of players were selected in the first 10 rounds of the draft for all draft classes between 2018 to 2020. While there were few players selected in later rounds, there were not many players drafted in later rounds compared to the first few rounds. We can conclude that those who are drafted earliest are given some of the most attention by organizations and are viewed as some of the most talented prospects that the organizations draft. A majority of these talented prospects would then go on to reach the MLB stage and display their skills. 

# Draft Team and WAR Impact
![team_bar_chart](https://github.com/NathanKim0107/Winter_Quarter_Baseball_Sports_Analytics_Project_2024/assets/128879072/99bc41dd-215b-4769-8bde-791595a7d49e)
In this visualization, we observe which teams were successful in bringing players up to the major leauge stages based on Negative and Positive WAR status categories. We can observe how teams like the Arizona Diamondbacks and Seattle Mariners were able to draft players from 2018 to 2020 who have earned their spot and are contributing to their teams' performances. We also notice how many pitchers in 2018 and 2019 have reached the major league stages, with less 2020 draft prospects who are contributing to their teams' performances. Based on the number of prospects and listed organizations, we can determine which organizations have been successful in drafting the right pitchers who are contributing to their organizations. 

# Birth/Home City Map
![Birth City Map Chart](https://github.com/NathanKim0107/Winter_Quarter_Baseball_Sports_Analytics_Project_2024/assets/128879072/659954cf-eb72-44cc-bc19-580103e5b798)
![Home City Map Chart](https://github.com/NathanKim0107/Winter_Quarter_Baseball_Sports_Analytics_Project_2024/assets/128879072/cee4b469-28b3-4aff-a348-ee85c5a41e10)
From this map, we notice that a majority of the prospects were found in California and Texas. There were few prospects found in the Midwest region but there were many prospects found in the Southeast and Southwest regions who were able to debut. From this visualization, we can determine that the birth city of a pitcher can impact a player's chance of reaching the pro stage as the resources available to players may differ and the type of climates players play under impact their performance. [Source](https://www.npr.org/2023/04/12/1169266941/global-warming-could-be-juicing-baseball-home-runs-study-finds#:~:text=Hotter%20temperatures%20may%20take%20a,of%20an%20advantage%20over%20pitchers.%22). However, one topic to further analyze is whether players stay in their birth cities and state or move across different cities or states. Athletes may move to different cities or states for educational or athletic resources. 

When observing home city trends, there were similar trends as there were many prospects whose homne cities were found in California, Texas, and Florida. While there does not appear to be any differences between either charts, we can infer that birth and home cities display states where prospects were able to reach the major league stage. It appears that people do not move far from their birth cities but each predictor is significant towards predicting how well players fare at the professional level as the city prospects live in can determine the types of resources that are available to players.


# School Bar Chart
![Birth City Bar Chart](https://github.com/NathanKim0107/Winter_Quarter_Baseball_Sports_Analytics_Project_2024/assets/128879072/60ed65e5-9c69-4d9d-9783-e1b3710a71a0)
The majority of the schools on the bar chart were from the south like North Carolina and Texas. This bar chart displays schools who have been successful at sending their athletes to the pros. On this chart, we notice that there were only colleges listed with colleges such as Oklahoma, Mississippi State, and Louisville having the highest count of prospects being able to debut. 

# Prospect Weight
![Prospect Wegith Box and Whiskers Plot](https://github.com/user-attachments/assets/77c2f8aa-847d-4b8e-9d6a-d6920414daf2)

