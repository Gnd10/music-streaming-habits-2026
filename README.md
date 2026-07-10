# 🎵 Music Streaming Habits Dashboard 2026

![Dashboard Preview](link_to_your_dashboard_screenshot.png) *(Optional: Add a screenshot of your dashboard)*

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

## 🚀 How to Use

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/Gnd10/music-streaming-habits-2026.git
