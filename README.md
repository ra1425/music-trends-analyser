# Spotify Music Trends Analysis

This project analyzes the Spotify "Top 200" dataset, which includes all global playlists from January 2017 to May 2023. The goal is to identify top artists, track audio feature trends (like Danceability and Energy) over time, and visualize artist popularity.

---

### Analysis Includes:

* **Data Cleaning:** Loading a complex CSV file with a semicolon delimiter, skipping bad lines, parsing dates (from `%d/%m/%Y`), and renaming columns.
* **Time-Series Analysis:** Aggregating data by month to see trends in audio features (`Danceability`, `Acousticness`, etc.) and by week to track artist popularity.
* **Data Normalization:** Using `sklearn.preprocessing.MinMaxScaler` to normalize all audio features, allowing them to be plotted and compared on a single chart.
* **Visualization:** Creating a series of plots with Matplotlib and Seaborn to show:
    * Top 10 artists by total points.
    * Normalized audio feature trends over time.
    * Weekly popularity spikes for the top 10 artists.
* **SQL Analysis:** Loading the clean DataFrame into an in-memory SQLite database and running a `GROUP BY` query to find top artists and their average danceability.

---

### Tools Used:

* Python
* Kaggle (Dataset source)
* Pandas
* Matplotlib & Seaborn
* Scikit-learn
* SQLite
