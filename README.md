![](video_game.jpg)

# Description: 

Video games are big business: the global gaming market is projected to be worth more than $300 billion by 2027 according to Mordor Intelligence. With so much money at stake, the major game publishers are hugely incentivized to create the next big hit. But are games getting better, or has the golden age of video games already passed?

# Analysis: 

In this project, SQL is utilitzed for following analysis: 
- video game critic and user scores as well as sales data for the top 400 video games released since 1977. 
- search for a golden age of video games by identifying release years that users and critics liked best 
- explore the business side of gaming by looking at game sales data.

# Methodology:

The search will involve joining datasets and comparing results with set theory. As well as using SQL features filter, group, join, limit, aggregate and order data. 

# Data:

- The database contains two tables. Each table has been limited to 400 rows for this project
- You can find the complete dataset with over 13,000 games on Kaggle or in my repo

# Result:

- This [notebook](notebook.ipynb) contains the SQL code for the following findings:
  1. Top 10 best selling video games since 1977
  2. 10 years with the highest average critic score
  3. Golden Years; years where critics and users broadly agreed that games released were highly rated

# Schema of the tables used for this analysis

### `game_sales` table

| Column | Definition | Data Type |
|-|-|-|  
|name|Name of the video game|`varchar`|
|platform|Gaming platform|`varchar`|
|publisher|Game publisher|`varchar`|
|developer|Game developer|`varchar`|
|games_sold|Number of copies sold (millions)|`float`|
|year|Release year|`int`|

### `reviews` table

| Column | Definition | Data Type |
|-|-|-|
|name|Name of the video game|`varchar`|  
|critic_score|Critic score according to Metacritic|`float`|
|user_score|User score according to Metacritic|`float`|


### `users_avg_year_rating` table

| Column | Definition | Data Type |
|-|-|-|
|year| Release year of the games reviewed |`int`|  
|num_games| Number of games released that year |`int`|
|avg_user_score| Average score of all the games ratings for the year |`float`|

### `critics_avg_year_rating` table

| Column | Definition | Data Type |
|-|-|-|
|year| Release year of the games reviewed |`int`|  
|num_games| Number of games released that year |`int`|
|avg_critic_score| Average score of all the games ratings for the year |`float`|

