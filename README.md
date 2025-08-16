# 🎶 Streaming Platforms Dataset Analysis (Spotify 2024)

## 📌 Project Overview
This project analyzes the **Most Streamed Songs on Spotify in 2024** dataset, enriched with performance metrics from multiple streaming platforms.  
The goal is to uncover **patterns, correlations, and key drivers of streaming success** across Spotify, YouTube, TikTok, Apple Music, Deezer, Amazon Music, Pandora, and SoundCloud.  

We combined **data cleaning, web scraping, exploratory data analysis (EDA), and visualization techniques** to answer research questions around **streaming performance, cross-platform relationships, and engagement metrics**.

---

## 📂 Dataset
**Source:** [Kaggle – Most Streamed Spotify Songs 2024](https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024)  

The dataset contains information on the **most streamed songs on Spotify in 2024**, with **29 columns** covering metadata and platform-specific popularity metrics.  

### Key Features:
- **Track Information** → Name, Album, Artist, Release Date, ISRC code  
- **Streaming Metrics** → Spotify streams, playlist counts, reach  
- **Cross-Platform Performance** → YouTube views & likes, TikTok posts & engagement, Apple Music, Deezer, Amazon Music, Pandora, SoundCloud  
- **Other Popularity Indicators** → Airplay spins, SiriusXM spins, Shazam counts, TIDAL & Spotify popularity  
- **Additional Attributes** → Explicit content flag, collaborations  

---

## 🔍 Research Questions
We structured our analysis around **10 key questions**:

1. What factors contribute the most to a song’s all-time rank?  
2. How do Spotify streams compare to YouTube views for the top-ranked songs?  
3. Do explicit songs tend to perform better across streaming platforms than clean songs?  
4. How does TikTok virality influence Spotify streaming numbers?  
5. Do songs with a higher number of playlist features have more streams?  
6. Is there a correlation between radio spins and streaming numbers across platforms?  
7. Do explicit tracks have higher TikTok engagement but lower radio spins?  
8. How does a song’s release year influence its cumulative streaming performance?  
9. Do collaborations achieve higher streams or playlist reach than solo tracks?  
10. Do Shazam counts indicate a song’s future streaming success?  

---

## 🧹 Data Cleaning Process
To ensure a **reliable and consistent dataset**, the following steps were applied:

1. **Data Import & Inspection** → Used `pandas` to explore structure, column types, and missing values.  
2. **Data Type Conversion** → Converted string-based numbers (e.g., `1,234,567`) to numeric, `Release Date` to datetime.  
3. **Handling Missing Values** →  
   - Dropped rows with missing **critical fields** (e.g., Artist, Spotify Streams).  
   - Filled missing values with **0** where absence implied non-appearance (e.g., TikTok posts, playlist counts).  
   - For popularity metrics, used **median values** or logical imputations based on performance indicators.  
4. **Standardizing Formats** → Unified text formatting, removed commas, corrected data types.  
5. **Dropping Irrelevant Columns** → Removed `TIDAL Popularity` due to excessive null values and low analytical value.  
6. **Final Integrity Check** → Ensured no nulls remained, with all missing entries handled logically.  

---

## 🌐 Web Scraping
To **enrich the dataset**, additional information was gathered from **two external websites**:  
**Source 1:** [kworb – Spotify Most Streamed Songs of All Time](https://kworb.net/spotify/songs.html)  
**Source 2:** [AllMusic](https://www.allmusic.com)  
- Scraped extra metadata and streaming-related statistics (such as recent tracks, engagement signals, or missing attributes).  
- Cleaned and standardized the scraped data using the same process (handling nulls, converting types, formatting).  
- **Merged the scraped datasets** with the original Kaggle dataset to provide a more comprehensive analysis.  

### Extended Analysis
After integrating the scraped data, we addressed **4 additional questions**, focusing on:  
- How recent releases compare to older hits across multiple platforms.  
- The effect of added engagement metrics on Spotify rank predictions.  
- Cross-validation of platform popularity scores.  
- Whether scraped data revealed new patterns not present in the original dataset.  

---

## 📊 Analysis Approach
We applied **Exploratory Data Analysis (EDA)** and **visualizations** to answer the research questions:  

- Distribution plots and bar charts for **release year, explicit vs clean songs**.  
- Correlation heatmaps for **cross-platform relationships** (Spotify vs YouTube, TikTok vs Spotify, Shazam vs Streams).  
- Trend analysis of **release years vs cumulative streams**.  
- Comparative analysis of **collaborations vs solo tracks**.  
- Engagement insights from **TikTok, Shazam, and Airplay data**.  

---

## 🛠 Tools & Libraries
- **Python**  
- **Pandas** → Data cleaning & manipulation  
- **Matplotlib / Seaborn** → Data visualization  
- **NumPy** → Statistical operations  
- **BeautifulSoup / Requests** → Web scraping  
- **Jupyter Notebook** → Analysis & exploration  

---
