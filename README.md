# 🎵 Spotify Social Media Analytics — Excel Project

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?logo=microsoftexcel&logoColor=white) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen) ![Domain](https://img.shields.io/badge/Domain-Social%20Media%20Analytics-blue)

## 📌 Project Overview

This project performs a comprehensive social media performance analysis for **Spotify** across three platforms — **Instagram, Twitter, and YouTube** — using Microsoft Excel. It covers data cleaning, engagement analysis, hashtag performance, campaign ROI, and follower growth trends across 4 marketing campaigns and 300+ posts spanning June 2024 to September 2025.

---

## 🗄️ Dataset Structure

The workbook contains the following key data tables:

| Sheet | Description |
|---|---|
| `Posts` | 300 posts with platform, date, content type, likes, shares, comments, impressions, reach, clicks, hashtags, and campaign name |
| `Engagement Summary` | Weekly follower data per platform — new followers, unfollows, total followers, engagement rate, ad spend |
| `Campaign Metadata` | 4 campaigns with budget, objective, target platforms, date range, and hashtags |

### Campaigns Covered

| Campaign | Objective | Budget | Platforms |
|---|---|---|---|
| SummerBeats | Brand Awareness | ₹1,75,000 | Instagram, YouTube |
| Wrapped2024 | Engagement | ₹2,25,000 | Twitter, YouTube |
| ChillVibes | Product Launch | ₹2,00,000 | Instagram, Twitter |
| IndieWave | Traffic | ₹1,60,000 | Facebook, Instagram |

---

## 🧹 Task 1 — Data Cleaning & Preprocessing

- **Removed duplicate post entries** to ensure campaign metrics reflect real performance
- **Standardized date and platform formats** using Power Query Editor
- **Fixed numeric columns** (likes, impressions, ad spend) for correct formatting
- **Split multi-hashtag columns** using Text to Columns, then unpivoted all hashtag columns into a single clean column using Power Query

---

## 📊 Task 2 — Engagement & Hashtag Analysis

**Engagement Rate per Platform (using SUMIF formulas):**

| Platform | Engagement Rate |
|---|---|
| Twitter | 0.073 (Highest) |
| Instagram | 0.071 |
| YouTube | 0.070 |

**Top 10 Posts by Engagement Rate** identified using Pivot Tables — the highest-performing post reached an engagement rate of **0.26**.

**Total Likes, Shares & Comments by Content Type & Platform** via Pivot Table:
- Instagram: Text posts significantly outperform Stories
- Twitter: Stories outperform text posts
- YouTube: Both Reels and Text perform similarly

**Average Clicks per Hashtag:**

| Hashtag | Avg. Clicks |
|---|---|
| #SpotifyWrapped | 208.47 (Highest) |
| #DiscoverWeekly | 197.17 |
| #SoundtrackOfLife | 192.46 |
| #NowPlaying | 186.72 |
| #MusicForEveryone | 183.48 |
| #SpotifyHits | 176.75 (Lowest) |

**Hashtag ranking by total clicks** using `SUMIF` + `RANK` formulas — `#NowPlaying` ranked #1 in total clicks.

---

## 🌐 Task 3 — Platform Performance & Strategy

- **YouTube** led with the highest engagement rate (9.99), narrowly ahead of Instagram (9.98) and Twitter (9.93)
- Compared **weekly follower growth rates** across platforms over 65+ weeks using Pivot Tables
- **Peak growth week:** 28 July–3 August 2025 with a growth rate of 0.017
- **Ad Spend vs. Engagement analysis:**
  - Instagram: 5,728 engagements on ₹27,753 spend — **most efficient**
  - Twitter: 5,639 engagements on ₹27,829 spend
  - YouTube: 5,599 engagements on ₹27,809 spend
- **Content type recommendation:**
  - Twitter Stories lead with engagement rate of 0.26
  - Instagram Stories underperform (0.18) — text posts recommended
  - YouTube should mix Reels and Text for optimal reach

---

## #️⃣ Task 4 — Hashtag & Content Deep Dive

**Average Engagement per Hashtag:**

| Hashtag | Avg. Engagement | Avg. Engagement Rate |
|---|---|---|
| #MusicForEveryone | 3,637 (Highest) | 8.91% |
| #SpotifyWrapped | 3,615 | 8.64% |
| #DiscoverWeekly | 3,580 | 8.76% |
| #NowPlaying | 3,536 | 9.86% |

**Content Type Performance across Platforms** (Max Likes, Shares, Comments, Clicks, Reach):
- Twitter Stories topped engagement with 0.26 rate and 4,984 likes
- Instagram Text drove 4,931 likes but Stories lagged at 0.18 rate
- YouTube Reels slightly outperformed Text content

**Optimal Content-Platform Recommendations:**
- **Instagram** → Stories (347 avg shares, 245 avg comments)
- **Twitter** → Stories (3,127 avg likes, top clicks)
- **YouTube** → Reels (3,099 avg likes, 235 avg comments)

---

## 📈 Task 5 — Campaign Performance & ROI

**Total Impressions, Likes & Clicks per Campaign:**

| Campaign | Total Impressions | Total Likes | Total Clicks |
|---|---|---|---|
| ChillVibes | 6,331,868 | 471,034 | 28,708 |
| IndieWave | 4,039,305 | 274,455 | 18,717 |
| SummerBeats | 1,233,853 | 89,871 | 5,557 |
| Wrapped2024 | 865,406 | 61,815 | 4,614 |

**Engagement Uplift (During vs. Before Campaign)** calculated using `SUMIFS` formulas with date range filtering:
- **IndieWave** had the strongest uplift at **+0.91**
- **Wrapped2024** showed strong uplift at **+0.75**
- ChillVibes and SummerBeats saw negative uplift (-0.36 and -0.95)

**Campaign ROI** (Engagement / Budget):
- **ChillVibes** achieved the highest ROI of **₹2.12 per rupee spent**

**Follower Growth per Campaign** using `SUMIFS` with date range:
- SummerBeats: 16,066 new followers (strongest)
- IndieWave: 15,065
- Wrapped2024: 13,891
- ChillVibes: 12,594

---

## 📉 Task 6 — Follower Trend & Correlation Analysis

- **Identified best week for net follower gain** per platform using Pivot Tables — YouTube peaked at 391,621 total followers during June 9–15, 2024
- **Moving average chart** built to analyze follower growth trends over time
- **Correlation between Ad Spend and Follower Growth** calculated using `CORREL()` formula: **-0.017**, indicating virtually **no relationship** between ad spend and follower growth

---

## ❓ Business Questions Answered

| Question | Answer |
|---|---|
| Which content types drive the most engagement? | Instagram Stories and ChillVibes campaign lead in engagement |
| Where to allocate advertising budget? | IndieWave — strongest engagement uplift (0.91) |
| What influences follower growth? | Hashtags like #DiscoverWeekly and #MusicForEveryone |
| How do campaigns correlate with subscriptions? | Positive relationship between social campaigns and premium subscriptions |

---

## 🛠️ Excel Features & Techniques Used

| Feature | Usage |
|---|---|
| Power Query | Date standardization, deduplication, hashtag unpivoting |
| Pivot Tables | Engagement summaries, follower trends, content type comparison |
| SUMIF / SUMIFS | Platform engagement rates, campaign-period filtering |
| RANK | Hashtag performance ranking |
| CORREL | Ad Spend vs. Follower Growth correlation |
| Date Range Logic | Campaign duration and pre/during period comparison |
| Structured Table References | Dynamic formulas using `Table[Column]` syntax |
| Charts | Ad Spend vs. Engagement visualization, Moving Average trend chart |

---

## 📁 Project Files

```
📦 Excel Project
 ┗ 📊 Spotify social media.xlsx   # Complete analysis workbook with all 6 tasks,
                                    raw data tables, Pivot Tables, charts & Q&A
```

---

## 🚀 How to Open

1. Open `Spotify social media.xlsx` in **Microsoft Excel** (2016 or later recommended)
2. Enable editing and allow content if prompted
3. Navigate through sheets: start with `Posts` and `Engagement Summary` for raw data, then explore `TASK 1` through `TASK 6` for the full analysis
4. Check the `Question & Answers` sheet for a summary of key business insights

---

## 💡 Key Insights

- **Twitter Stories** deliver the highest engagement rate (0.26) — best platform-content combination
- **ChillVibes** had the highest ROI at ₹2.12 and the most total impressions (6.3M)
- **Ad spend has no meaningful correlation** with follower growth (-0.017) — organic strategy matters more
- **IndieWave** showed the strongest real-world impact with 91% engagement uplift during its campaign period
- **#SpotifyWrapped** drives the most clicks per post (208 avg) making it the most valuable hashtag

---

## 👤 Author

### Tridev Pal
📍 Calcutta, West Bengal, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin)](https://www.linkedin.com/in/tridev-pal-74575a379/)

> Feel free to connect or raise issues via GitHub if you have suggestions or improvements!
