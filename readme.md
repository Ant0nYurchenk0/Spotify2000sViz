# Spotify Data Music Genres Visualization

This project analyzes and visualizes Spotify's top 2000 tracks dataset, categorizing songs into broad genres and displaying them through an interactive visualization.

## Dataset

The dataset contains audio statistics of the top 2000 tracks on Spotify from 1956 to 2019, featuring notable artists like Queen, The Beatles, and Guns N' Roses. The data includes approximately 15 columns describing each track's musical qualities including BPM, energy, danceability, loudness, and valence.

**Source:** [Spotify Top 2000s Mega Dataset](https://www.kaggle.com/datasets/iamsumat/spotify-top-2000s-mega-dataset)

## Features

- **Genre Mapping**: Python script that maps specific genres to broader categories (e.g., "acid jazz" → "Jazz", "alternative rock" → "Rock")
- **Interactive Visualization**: D3.js-powered web interface showing genre distributions
- **Audio Feature Analysis**: Displays 5 key audio features normalized per genre
- **Popularity Metrics**: Shows how often genres appear in top 100 most popular tracks

## Usage

1. **Update the data:**
   ```bash
   python main.py
   ```
   This processes the original CSV file and creates `Spotify-2000-updated.csv` with broad genre categories.

2. **Launch the visualization:**
   ```bash
   python -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser to view the interactive visualization.

## Installation

Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Visualization Details

- **Circle Size**: Proportional to total number of songs in each genre
- **Vertical Position**: Reflects frequency of genre in top 100 most popular tracks  
- **Petal Shapes**: Radar chart showing normalized values of 5 audio features (Valence, Energy, BPM, Danceability, Loudness)
- **Hover Interaction**: Displays detailed statistics for each genre

## Files

- `main.py` - Data processing script that maps genres and creates updated CSV
- `index.html` - Interactive D3.js visualization
- `Spotify-2000.csv` - Original dataset
- `Spotify-2000-updated.csv` - Processed dataset with broad genre categories
- `requirements.txt` - Python dependencies