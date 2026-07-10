# 🎵 Music Streaming Habits Dashboard 2026 - Power BI

([Overview Dashboard.png](https://github.com/Gnd10/music-streaming-habits-2026/blob/a35e4d19faef24064855bab7682875d37d2ac652/Overview%20Dashboard.png)) 

## 📊 About This Project

This project provides an in-depth analysis of music streaming habits from **4,000 users** on a music platform in 2026. The goal is to understand user behavior, content preferences, and identify key business opportunities—especially in converting Free users to Premium subscribers.

The analysis is structured around three main pillars:
1.  **User Demographics:** Who are our users? (Age, Location, Subscription Type).
2.  **Listening Behavior:** How do they use the platform? (Duration, Mood, Genres, Favorite Artists).
3.  **Business Insights:** What does this mean for product strategy and marketing?

## 🔍 Key Insights Summary

| Category | Insight | Key Figures |
| :--- | :--- | :--- |
| **Users & Engagement** | The platform has a highly engaged user base, with the average user listening for **2.3 hours** per day. | **Total Users:** 4,000<br>**Active Users:** 82.68% |
| **Upsell Opportunity** | While **Free users** make up the majority (45.5%), **Premium users** are significantly more active (82.9%). This indicates a massive conversion potential. | **Premium Active:** 82.9%<br>**Free Users:** 45.5% |
| **Target Demographics** | The average user age is **27.85 years**, dominated by the Adult (25-34) age group. The largest markets are **Japan (439 users)** and **Canada (429 users)**. | **Dominant Age:** 25-34 (42.3%)<br>**Top Country:** Japan (439) |
| **Listening Behavior** | **Pop** and **Afrobeats** are the dominant genres, with **SZA** and **Bad Bunny** as top artists. The *Workout* mood has the highest skip rate. | **Avg. Listening:** 138.7 min<br>**Top Mood (Workout):** 28.62% skip rate |

## 📁 Dataset Structure

The main CSV file (`music_streaming_habits_2026.csv`) contains the following columns:

| Column | Description |
| :--- | :--- |
| `listener_id` | Unique identifier for each user. |
| `age` | User's age. |
| `country` | User's country of origin. |
| `subscription` | Type of subscription (Free, Premium, Student, Family). |
| `top_genre` | Most frequently listened genre. |
| `top_artist` | Most frequently listened artist. |
| `daily_listening_minutes` | Total listening minutes per day. |
| `songs_per_day` | Number of songs played per day. |
| `skip_rate_pct` | Percentage of songs skipped. |
| `top_mood` | Most frequently selected mood. |

*(And many more columns like `platform`, `playlists_count`, `uses_offline_mode`, etc.)*

## 🚀 How to Use This Dashboard

### Option 1: Open the Power BI File
1. **Download** the `.pbix` file from this repository
2. **Open** with Power BI Desktop (free download from Microsoft)
3. **Explore** the interactive dashboards

### Option 2: View Online
- **Publish** to Power BI Service for web access
- **Share** with stakeholders via Power BI Service

### Option 3: Connect Your Own Data
1. **Download** the `music_streaming_habits_2026.csv` file
2. **Open** Power BI Desktop
3. **Click** "Get Data" → "Text/CSV"
4. **Select** the CSV file
5. **Load** the data
6. **Rebuild** or **Modify** the visualizations

## 📊 Dashboard Features

### Page 1: Overview
- **Key Metrics Cards:** Total Users, Premium Active %, Avg. Songs/Day, Avg. Listening (min)
- **Top Mood vs Total Users:** Bar chart showing top 5 moods
- **Country vs Total Users:** Geographic distribution
- **Subscription Distribution:** Pie chart (Free 45.5%, Premium 29.83%, Student 14.65%, Family 10.03%)
- **Top 10 Favorite Artists:** Horizontal bar chart

### Page 2: User Demographics
- **Age Distribution:** Age vs Total Users
- **Subscription by Age Group:** Stacked bar chart
- **Country Distribution:** Map visualization
- **Top 5 Countries by Subscription:** Stacked bar chart
- **Listening Minutes by Age Group:** Bar chart
- **Songs/Day by Country:** Combined chart

### Page 3: Listening Behavior
- **Top Mood vs Avg Skip Rate:** Bar chart
- **Songs/Day vs Listening Minutes by Subscription:** Scatter plot
- **Top Genre vs Avg Listening:** Bar chart
- **Top Genre vs Avg Playlists:** Bar chart
- **Average Songs by Age Group:** Bar chart
- **Platform Distribution:** Additional metrics

## 📈 DAX Measures Used

```dax
// Total Users
Total Users = COUNTROWS('music_streaming_habits_2026')

// Premium Active %
Premium Active % = 
DIVIDE(
    CALCULATE(COUNTROWS('music_streaming_habits_2026'), 
              'music_streaming_habits_2026'[subscription] = "Premium"),
    [Total Users]
)

// Average Listening Minutes
Avg Listening Minutes = 
AVERAGE('music_streaming_habits_2026'[daily_listening_minutes])

// Average Songs Per Day
Avg Songs Per Day = 
AVERAGE('music_streaming_habits_2026'[songs_per_day])

// Active Users %
Active Users % = 
DIVIDE(
    CALCULATE(COUNTROWS('music_streaming_habits_2026'), 
              'music_streaming_habits_2026'[songs_per_day] > 0),
    [Total Users]
)

// Offline Users %
Offline Users % = 
DIVIDE(
    CALCULATE(COUNTROWS('music_streaming_habits_2026'), 
              'music_streaming_habits_2026'[uses_offline_mode] = TRUE()),
    [Total Users]
)
💡 Actionable Recommendations
Recommendation	Rationale	Priority
Premium Conversion Campaign	45.5% Free users, 82.9% Premium active	🔴 High
Promote Offline Mode	Only 42.75% usage rate	🟡 Medium
Focus on Top Markets	Japan, Canada, USA, Brazil, Nigeria	🔴 High
Improve Workout Playlists	Highest skip rate (28.62%)	🟡 Medium
Engage Teen Users	Underrepresented age group	🟢 Low
Podcast Cross-Selling	Many users also listen to podcasts	🟢 Low
🛠️ Tools & Technologies
Data Visualization: Power BI Desktop

Data Source: CSV file (4,000 records)

Documentation: GitHub Markdown

🤝 Contributing
Contributions to improve the dashboard or add new analyses are welcome!

Ways to Contribute
1. 📊 Add new visualizations
2. 🔍 Create additional DAX measures
3. 📝 Improve documentation
4. 🐛 Report issues


📈 Future Enhancements
1. Add forecasting for user growth
2. Create drill-through pages for deeper analysis
3. Implement row-level security for data protection
4. Build custom visualizations using R/Python visuals
5. Automate data refresh with Power BI Service
