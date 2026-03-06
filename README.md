Movie Database Analysis
Exploratory data analysis of mymoviedb.csv using Python

Data Cleaning & Preparation
The dataset was loaded from mymoviedb.csv and prepared for analysis through the following steps:
1.	Removed duplicate rows
2.	Dropped rows with missing values
3.	Converted columns to correct data types: release_date to datetime, vote_count to int, vote_average and popularity to float, and original_language to category
4.	Detected and removed outliers in popularity and vote_count using the IQR method
After cleaning, a brief exploration was done using .info() to verify data types, .describe() for summary statistics, and boxplots to compare distributions before and after outlier removal.

Q1: What is the movie with the highest popularity rate and what kind is it?
The most popular movie is "The Day Naruto Became Hokage", a Comedy, Animation, Action, and Adventure film with the highest popularity score in the dataset.

Q2: What year was the largest number of films produced?
Film counts were grouped by year and the top 10 most productive years were visualized using both a bar chart and a line chart. The data shows a steady increase in production over the years, with a noticeable drop in 2019-2020 due to the COVID-19 pandemic, followed by a recovery and continued growth.

Q3: What is the most common film genre?
Since each film can belong to multiple genres, the genre column was split and counted individually. Drama is the most common genre with 3,112 films, followed by Comedy (2,473) and Action (2,001).
Business Insight: Drama, Comedy, and Action dominate the market, giving studios in these genres a larger potential audience. Niche genres like Western and TV Movie see significantly less production, representing either low demand or an untapped opportunity.


Q4: What kind of movies receive the highest ratings?
The genre column was split and exploded to calculate the average rating per genre. Music films rank highest at 6.52, followed by Horror (6.42) and Crime (6.42), while War and Western have the lowest average ratings.
Business Insight: Despite Drama and Comedy leading in production volume, Music and Horror films rate higher with audiences. Less produced genres can still deliver strong satisfaction, which is worth considering when balancing investment against expected reception.


Q5: Which movie is the most and least popular?
The most popular movie is "The Day Naruto Became Hokage" (score: 63.75), while the least popular is "The United States vs. Billie Holiday" (score: 13.35).
Business Insight: The wide gap highlights how animation and franchise-based content drives significantly higher engagement compared to biographical or historical dramas.


Q6: Which language produces the most movies?
English dominates with 5,869 films, far ahead of Japanese (562), Spanish (295), and French (270), as shown in a bar chart of the top 10 languages.
Business Insight: The global film market is heavily English-centric. However, the presence of Japanese, Korean, and Chinese in the top 10 reflects the growing influence of Asian cinema, which represents a significant and expanding market.


Q8: How has the average movie rating changed over the years?
Average ratings were grouped by year and plotted as a line chart. Early films from the 1900s show high ratings (around 8.0), likely due to the small number of films at the time. Ratings gradually decline and stabilize around 6.5 in recent decades, with a sharp drop in 2022-2024 due to incomplete rating data for recently released films.
Business Insight: The declining trend likely reflects the massive growth in production, with more average-quality films being made alongside standouts. The 2022-2024 drop should be treated as a data quality issue rather than a real trend.


Q9: Which languages produce the highest-rated movies on average?
The analysis was filtered to the top 10 most productive languages for a fair comparison. Japanese films rank highest with an average rating of 6.94, followed by Russian (6.87) and Chinese (6.82), while English ranks last among the top 10 at 6.23.
Business Insight: English produces the most films but rates the lowest among top languages. Japanese and Russian produce fewer films but with consistently higher quality, suggesting these markets prioritize quality over quantity — a valuable benchmark for studios aiming to improve audience reception.
