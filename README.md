
# game of thrones data visualization
![game-of-thrones-92acb30ilmkjbmu9](https://user-images.githubusercontent.com/75095471/218716069-ec64bdf9-5467-4169-8891-3e2716c2bb0c.jpg)


# About Dataset
## Context
Game of Thrones is an American fantasy drama television series created by David Benioff and D. B. Weiss for HBO. It is an adaptation of A Song of Ice and Fire, a series of fantasy novels by George R. R. Martin, the first of which is A Game of Thrones. The show was shot in the United Kingdom, Canada, Croatia, Iceland, Malta, Morocco, and Spain. It premiered on HBO in the United States on April 17, 2011, and concluded on May 19, 2019, with 73 episodes broadcast over eight seasons.

Set on the fictional continents of Westeros and Essos, Game of Thrones has a large ensemble cast and follows several story arcs throughout the course of the show. The first major arc concerns the Iron Throne of the Seven Kingdoms of Westeros through a web of political conflicts among the noble families either vying to claim the throne or fighting for independence from whoever sits on it. A second focuses on the last descendant of the realm's deposed ruling dynasty, who has been exiled to Essos and is plotting to return and reclaim the throne. The third follows the Night's Watch, a military order defending the realm against threats from beyond Westeros's northern border.

Game of Thrones attracted record viewership on HBO and has a broad, active, and international fan base. Critics have praised the series for its acting, complex characters, story, scope, and production values, although its frequent use of nudity and violence (including sexual violence) has been subject to criticism. The final season received significant critical backlash for its reduced length and creative decisions, with many considering it a disappointing conclusion. The series received 59 Primetime Emmy Awards, the most by a drama series, including Outstanding Drama Series in 2015, 2016, 2018, and 2019. Its other awards and nominations include three Hugo Awards for Best Dramatic Presentation, a Peabody Award, and five nominations for the Golden Globe Award for Best Television Series – Drama. Many critics and publications have named the show as one of the best television series of all time.

## Content
In this Dataset, we have various information about each Episode/Season of Game of Thrones. The key features of this Dataset are - Season, No. of Episodes (Season), No. of Episodes (Overall), Title of the Episode, Running Time (Minutes), Directed by, Written by, Original Air Date, U.S. Viewers (Millions), Music by, Cinematography by, Editing by, IMDb Rating, Rotten Tomatoes Rating (Percentage), Metacritic Ratings, Season Ordered, Filming Duration, Novel(s) Adapted, Synopsis of each Episode.

## Dataset Glossary (Column-wise)
Season - No. of Seasons
No. of Episode (Season) - No. of Episode in a particular Season
No. of Episode (Overall) - No. of Episode in the whole Series
Title of the Episode - Name of the Episode
Running Time (Minutes) - Runtime of the Episode in Minutes
Directed by - Name(s) of the Director
Written by - Name(s) of the Writer
Original Air Date - Original Air Date of the Episode
U.S. Viewers (Millions) - No of U.S. Viewers of the Episode in Millions
Music by - Name(s) of the Composer
Cinematography by - Name(s) of the Cinematographer
Editing by - Name(s) of the Editor
IMDb Rating - IMDb Rating of the Episode (10 point scale)
Rotten Tomatoes Rating (Percentage) - Rotten Tomatoes Rating of the Episode in Percentage
Metacritic Ratings - Metacritic Rating of the Episode
Ordered - Date of Series/Season renewal
Filming Duration - Filming Duration of the Season
Novel(s) Adapted - Adapted from which Novel(s)
Synopsis - Synopsis of the Episode

## code
The given code involves various data visualization techniques used to analyze the Game of Thrones dataset. The main objective of the analysis is to understand the factors affecting the popularity of the TV series.
The code starts with importing necessary libraries such as Pandas, Matplotlib, Numpy, Seaborn, and Bokeh. It reads the 'Game_of_Thrones.csv' file and creates a DataFrame named df, which contains various columns such as Season, Episode, Director, Writer, Ratings, and Viewership data of the entire series.
Next, the code creates a pie chart using the Matplotlib library. The pie chart displays the percentage of episodes in each season of the Game of Thrones series. The chart is created by extracting the unique season numbers and then using the value_counts function to find the number of episodes in each season. Finally, the pie chart is plotted with the help of the plt.pie function.

![download (9)](https://user-images.githubusercontent.com/75095471/218714336-f44c43b0-09d4-4199-a340-c057bf867bd6.png)

Further, the code performs some data preprocessing by scaling the 'Rotten Tomatoes Rating (Percentage)' column values between 0 and 10 and creating a new 'total_score' column in the DataFrame by adding the IMDb, Rotten Tomatoes, and Metacritic ratings. Additionally, it renames some column names for better understanding.

![image](https://user-images.githubusercontent.com/75095471/218714502-8e64cfbe-a637-4a58-aed1-ec6d42cc9a15.png)

From this chart, it can be seen that as the episodes of the series go forward, it gains more fans (viewers), but another thing that is clearly evident is the sharp drop of the series from season 7 onwards, despite the fact that the series has more viewers in the seasons 7 and 8, but the downward trend does not stop, which can be the reason for the lack of motivation for the series staff, because the series has found its viewers and the upward trend of viewers has not stopped either.


Next, the code creates a scatter plot with the help of Bokeh library. The scatter plot shows the relationship between the episode number and the number of viewers, along with the total score of each episode. The scatter plot uses the 'No. of Episode (Overall)' and 'U.S. Viewers (Millions)' columns for the x and y-axis respectively. It also plots a line graph that represents the total score of each episode.
The scatter plot also uses a HoverTool function to provide additional information about each episode. The HoverTool displays the 'Directed by', 'Written by', 'Season', and 'Episode' data of each episode when the cursor is moved over the respective point on the scatter plot.
Further, the code creates a heatmap with the help of the Seaborn library. The heatmap displays the correlation between the 'No. of Episode (Overall)', 'U.S. Viewers (Millions)', and 'total_score' columns. The heatmap uses the corr function of the DataFrame to find the correlation coefficient and annotates the values in each cell of the heatmap.

![image](https://user-images.githubusercontent.com/75095471/218714793-c392ee68-911e-4978-8494-77afb66e1d71.png)

A correlation coefficient is a statistical measure of the degree to which changes to the value of one variable predict change to the value of another. In positively correlated variables, the value increases or decreases in tandem.It can be seen that the episode number has a high correlation with the number of viewers and they have a positive correlation, and on the other hand, the total scores have a negative correlation with the viewers and the episode number, which is a confirmation of the analysis of the previous graph.

Finally, the code creates a horizontal bar chart with the help of the Bokeh library. The bar chart displays the average total score of each director who directed the episodes of the Game of Thrones series. The chart uses the 'Director', 'total_score', and 'counts' columns of the DataFrame. It sorts the data based on the 'total_score' column and plots the average score of each director. The HoverTool function displays the number of episodes each director has directed.

![image](https://user-images.githubusercontent.com/75095471/218714939-7d080035-01eb-434b-ac11-42c0d7ad402e.png)

It can be seen that Neil Marshall is the first, but the number of episodes made by him is two, but Alex Graves has made six episodes and the average score is second. It can be said that Alex Graves was the most worthy director of this series (according to scores).

Lastly, the code creates a vertical bar chart with the help of the Bokeh library. The vertical bar chart displays the average total score of each season of the Game of Thrones series. The chart uses the groupby function of the DataFrame to group the data based on the 'Season' column and calculates the average total score for each season. Finally, the chart plots the data with the help of the vbar function of the Bokeh library.

![image](https://user-images.githubusercontent.com/75095471/218715032-49d3f8dc-bf18-4c85-b980-b34517bec517.png)

To show the best season of the series, the average score of all the episodes of one season is the best season


In conclusion, the given code provides a detailed data analysis of the Game of Thrones TV series. It uses various data visualization techniques to identify the factors affecting the popularity of the series. The analysis shows that the number of episodes, viewership, and total score of each episode have a strong correlation with the popularity of the series. The code also identifies the most popular season, director, and episode of the Game of Thrones series.


