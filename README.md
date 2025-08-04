# 🎧 Spotify Track Metadata ETL Pipeline

This project demonstrates how to build a simple ETL (Extract, Transform, Load) pipeline to collect music track metadata from the **Spotify Web API**, transform it into structured records, and load it into a **MySQL** database for storage and analysis.

---

## ✨ Features

- Fetches track metadata (track name, artist, album, popularity, duration) from Spotify.
- Stores the metadata in a MySQL database.
- Processes multiple tracks using a list of Spotify track URLs.
- Simple bar chart visualization for a single track.
- SQL queries to analyze popularity and duration.

---

## 🛠️ Tech Stack

- Python
- Spotipy (Spotify Web API)
- MySQL
- mysql-connector-python
- Pandas
- Matplotlib

---
spotify_etl_project/
├── spotify.py # Single track test with visualization
├── spotify_mysql.py # Insert one track into MySQL
├── spotify_mysql_urls.py # Insert multiple tracks from URLs
├── spotify.sql # MySQL schema setup
├── track_urls.txt # List of Spotify track URLs
├── spotify_track_data.csv # Output of single track
## 📁 Project Files


---

## ⚙️ How to Run

1. Install required libraries:


2. Update Spotify API credentials and MySQL login details in each `.py` file.

3. Run the SQL file (`spotify.sql`) in MySQL Workbench to create the database and table.

4. Run the scripts in this order:
- `spotify.py` (optional test + chart)
- `spotify_mysql.py` (insert one track)
- `spotify_mysql_urls.py` (insert multiple tracks)

---

## 📊 Sample SQL Queries

```sql
-- View all tracks
SELECT * FROM spotify_tracks;

-- Top track by popularity
SELECT track_name, artist
FROM spotify_tracks
ORDER BY popularity DESC
LIMIT 1;

-- Average popularity
SELECT AVG(popularity) FROM spotify_tracks;

---

 Acknowledgments
Spotify Web API
Spotipy Python Library


