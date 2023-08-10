# Spotify_EDA
Spotify Exploratory Data Analysis Project

In the provided project, I have performed various data analysis tasks on a dataset containing information about music tracks.

1. Data Import and Initial Exploration:
 
Imported necessary libraries: numpy, pandas, matplotlib.pyplot, and seaborn.
Loaded a CSV dataset (tracks.csv) using pd.read_csv and stored it in a DataFrame called df_tracks.
Displayed the first few rows of the DataFrame using df_tracks.head().

2. Data Cleaning and Preprocessing:

Checked for missing values using pd.isnull(df_tracks).sum() and printed the count of missing values for each column.
Checked the data types and non-null counts of columns using df_tracks.info() and observed that there are 20 columns with various data types.
Explored statistics of the dataset using df_tracks.describe().transpose().

3. Data Transformation and Manipulation:

Converted the 'release_date' column to a datetime format and set it as the index of the DataFrame.
Created a new column 'duration' by rounding the 'duration_ms' column and dropped the original 'duration_ms' column.
Renamed the columns of the DataFrame to remove underscores and make them more readable.

4. Data Analysis and Visualization:

Calculated the artist with the most followers using df_tracks[['artists']].value_counts().head(1).
Found the track with the highest popularity and its associated artist using df_tracks[['artists', 'popularity']].max().
Sorted tracks by popularity in ascending order and displayed the least popular tracks using sorted_df = df_tracks.sort_values('popularity', ascending=True).head(10).
Plotted a heatmap to visualize correlations between variables using sns.heatmap.
Created scatter plots to explore correlations between variables, such as "Loudness Vs Energy" and "Popularity Vs Acousticness".
Plotted the number of songs released each year using sns.displot and sns.distplot.
Visualized the distribution of song durations across years using a bar plot
