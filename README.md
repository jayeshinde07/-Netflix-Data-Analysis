# Movie Data Analysis (EDA)

Exploratory Data Analysis on a dataset of ~9,800 movies to uncover trends in
genre popularity, audience ratings, and release patterns — built with Python,
Pandas, and Seaborn.

#  Overview

This project cleans and analyzes a movie metadata dataset (title, release date,
popularity, vote average, vote count, genre) to answer questions like:

- What genre appears most frequently across movies?
- How are audience vote averages distributed?
- Which movie had the highest and lowest popularity score?
- Which year had the most movie releases?

# Dataset

- File: `mymoviedb.csv`
- Rows: 9,800 movies
- Columns: Release Date, Title, Overview, Popularity, Vote Count,
  Vote Average, Original Language, Genre, Poster URL

# Data Cleaning & Preparation

- Converted `Release_Date` to datetime and extracted release year
- Dropped irrelevant columns (`Overview`, `Original_Language`, `Poster_Url`)
- Removed duplicate and null records
- Binned `Vote_Average` into 4 categories (`not_popular`, `below_avg`,
  `average`, `popular`) using quartile-based cutoffs
- Split multi-genre strings (e.g. `"Action, Adventure"`) into individual rows
  using `explode()`, so each movie-genre pair is analyzed separately
- Cast `Genre` to a categorical data type for memory efficiency

# Key Analysis & Visualizations

- Genre distribution — bar chart of most frequent genres in the dataset
- Vote average distribution — count plot across the 4 rating categories
- Highest/lowest popularity movies — identified via filtering on the
  `Popularity` column
- Release year trends — histogram showing which years had the most
  movie releases

# 🛠 Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

# 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook movie_data_analysis.ipynb
```

# 📈 Key Insight

[Fill in once you re-check your output — e.g., "Drama and Comedy were the
most frequently occurring genres, and movie releases peaked in [year]."]

# 📄 Files

- `movie_data_analysis.ipynb` — main analysis notebook
- `mymoviedb.csv` — dataset
