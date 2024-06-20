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
