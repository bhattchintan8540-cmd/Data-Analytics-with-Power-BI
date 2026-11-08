# 🎬 OTT Streaming Platforms Analytics Dashboard — Netflix, Amazon Prime & Disney+ Hotstar

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Netflix](https://img.shields.io/badge/Netflix-E50914?style=for-the-badge&logo=netflix&logoColor=white)](https://www.netflix.com)
[![Amazon Prime](https://img.shields.io/badge/Amazon_Prime_Video-00A8E1?style=for-the-badge&logo=prime&logoColor=white)](https://www.primevideo.com)
[![Disney+ Hotstar](https://img.shields.io/badge/Disney+_Hotstar-00147e?style=for-the-badge&logo=disneyplus&logoColor=white)](https://www.hotstar.com)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-orange?style=for-the-badge)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

An end-to-end Business Intelligence (BI) and comparative entertainment analytics project developed in **Microsoft Power BI Desktop**, benchmarking content catalogs, release trajectories, genre distribution, age ratings, and geographical reach across the world's leading Over-The-Top (OTT) streaming giants: **Netflix**, **Amazon Prime Video**, and **Disney+ Hotstar**.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Architecture](#-dataset-architecture)
- [Dashboard & Visualizations Breakdown](#-dashboard--visualizations-breakdown)
  - [1. Netflix Analytics View](#1--netflix-analytics-view)
  - [2. Amazon Prime Video Analytics View](#2--amazon-prime-video-analytics-view)
  - [3. Disney+ Hotstar Analytics View](#3--disney-hotstar-analytics-view)
- [Cross-Platform Comparative Insights](#-cross-platform-comparative-insights)
- [Prerequisites & Getting Started](#-prerequisites--getting-started)
- [Tech Stack & Tools](#-tech-stack--tools)
- [Future Enhancements](#-future-enhancements)

---

## 🔍 Project Overview

The global video-on-demand ecosystem is characterized by distinct content acquisition and original production strategies. This project aggregates and models **19,940+ streaming titles** across Netflix, Amazon Prime Video, and Disney+ Hotstar to deliver an executive-level comparative performance view:

- **Catalog Volume & Composition**: Total titles, Movies vs. TV Shows ratio, and catalog expansion rates.
- **Audience Targeting & Maturity Ratings**: Distribution of content classification (TV-MA, TV-14, PG-13, TV-G, TV-Y7) indicating target demographics.
- **Genre Specialization**: Funnel ranking of leading genre categories (Dramas, Comedies, Documentaries, Kids & Family, Action).
- **Historical Release Trends**: Tracking archival content volume and the post-2015 surge in direct-to-digital releases.
- **Global Footprint**: Filled map visualizations tracking country-of-origin distribution for international content localization.

---

## 🗄️ Dataset Architecture

The project ingests three distinct platform datasets stored in `Dataset/`:

| Dataset File | Platform | Total Titles | Primary Focus |
|:---|:---|:---:|:---|
| **`netflix_titles.csv`** | Netflix | **8,809** | Broad international diversity, high TV-MA originals, documentary footprint |
| **`amazon_prime_titles.csv`** | Amazon Prime Video | **9,687** | Extensive movie archive, diverse independent productions, deep catalog depth |
| **`disney_plus_titles.csv`** | Disney+ Hotstar | **1,450** | High-density family, animation, franchise universes (Marvel, Star Wars, Pixar) |

### Unified Data Schema:
Every dataset contains normalized attributes facilitating cross-platform benchmarking:

- **`show_id`**: Unique identifier for each movie or TV show.
- **`type`**: Primary classification (`Movie` vs. `TV Show`).
- **`title`**: Commercial title of the media asset.
- **`director`**: Primary and contributing directors.
- **`cast`**: Key actors and leading cast members.
- **`country`**: Country or co-production nations of origin.
- **`date_added`**: Timestamp when the title was indexed on the platform.
- **`release_year`**: Original commercial debut / theatrical release year.
- **`rating`**: Maturity content rating code (TV-MA, TV-14, R, PG-13, TV-PG, TV-G, TV-Y, etc.).
- **`duration`**: Runtime formatted in minutes (for Movies) or number of seasons (for TV Shows).
- **`listed_in`**: Genre categories and sub-genres.
- **`description`**: Synopsis and plot overview.

---

## 📈 Dashboard & Visualizations Breakdown

The Power BI model (`Working File/OTT Dashboard.pbix`) features three dedicated analytical views:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        OTT ANALYTICS DASHBOARD                         │
├─────────────────────┬───────────────────────────┬──────────────────────┤
│ 🔴 NETFLIX VIEW     │ 🔵 AMAZON PRIME VIEW      │ 🟢 HOTSTAR VIEW      │
│ • Total Titles Card │ • Total Titles Card       │ • Total Titles Card  │
│ • Global Map        │ • Global Map              │ • Global Map         │
│ • Rating Dist. (Col)│ • Rating Dist. (Cluster)  │ • Rating Dist. (Col) │
│ • Top Genres Funnel │ • Top Genres Funnel       │ • Top Genres Funnel  │
│ • Trend by Year     │ • Releases per Year Area  │ • Release Additions  │
│ • Watch Duration    │ • Watch Duration Donut    │ • Watch Duration     │
└─────────────────────┴───────────────────────────┴──────────────────────┘
```

### 1. 🔴 Netflix Analytics View
- **Executive Metric Cards**: Dynamic KPI callouts tracking total catalog size, total standalone movies, and episodic series.
- **Global Production Footprint (Filled Map)**: Visual mapping of international productions highlighting dominant content hubs (United States, India, United Kingdom, South Korea, Japan).
- **Top 5 Show Rating Types (Column Chart)**: Breakdown of content ratings demonstrating Netflix's strong weighting toward mature adult audiences (`TV-MA` and `TV-14`).
- **Top 3 Genres (Funnel Chart)**: Volume hierarchy revealing the platform's anchor genres (`Dramas`, `Comedies`, `Documentaries`).
- **Show Trend by Year (Stacked Area Chart)**: Trajectory of content additions showing exponential growth between 2016 and 2021.
- **Watch Duration Composition (Donut Chart)**: Proportional split between feature films (~70%) and multi-season episodic television (~30%).
- **Interactive Navigation**: Direct deep link to `netflix.com` and release year filter slicer.

### 2. 🔵 Amazon Prime Video Analytics View
- **Executive Metric Cards**: Catalog counters measuring Prime Video's vast repository (~9,687 assets).
- **Top Countries by Show (Filled Map)**: Geographic distribution analysis displaying high domestic density alongside international expansion.
- **Top 5 Show Rating Types (Clustered Column Chart)**: Dual-series comparative breakdown of ratings cross-tabulated by Movies vs. TV Shows.
- **Top 3 Genres (Funnel Chart)**: Analysis of Amazon's catalog anchors, demonstrating leadership in `Drama`, `Comedy`, and `Action`.
- **Releases per Year (Stacked Area Chart)**: Visualizing extensive back-catalog titles spanning 1920 to 2021.
- **Watch Duration (Donut Chart)**: Movie-heavy distribution reflecting Amazon's digital rental and purchase library heritage.
- **Interactive Navigation**: Direct deep link to `primevideo.com` and release year filter slicer.

### 3. 🟢 Disney+ Hotstar Analytics View
- **Executive Metric Cards**: Focused inventory metrics reflecting Disney's curated high-value intellectual property (~1,450 titles).
- **Top Countries by Show (Filled Map)**: Content origin visualization showing concentrated production primarily from the United States with Indian regional content integration.
- **Top 5 Show Rating Types (Column Chart)**: Prominence of family-safe classifications (`TV-G`, `TV-PG`, `G`, `PG`) aligning with brand guidelines.
- **Top 3 Genres (Funnel Chart)**: Genre rankings dominated by `Animation`, `Kids & Family`, and `Action-Adventure`.
- **Annual Additions Trend (Clustered Column Chart)**: Release timeline tracking post-launch library buildout.
- **Watch Duration (Donut Chart)**: Balanced franchise movie catalog alongside episodic Disney+ Original releases.
- **Interactive Navigation**: Direct deep link to `hotstar.com` and release year filter slicer.

---

## 💡 Cross-Platform Comparative Insights

| Metric / Dimension | 🔴 Netflix | 🔵 Amazon Prime Video | 🟢 Disney+ Hotstar |
|:---|:---|:---|:---|
| **Catalog Depth** | High (~8.8K) | Largest (~9.7K) | Curated / Focused (~1.4K) |
| **Dominant Format** | Movies (~70%) | Movies (~80%+) | Movies (~72%) |
| **Primary Audience Rating** | TV-MA / TV-14 (Mature) | 13+ / 16+ / All Ages | TV-G / TV-PG / PG (Family) |
| **Core Genre Pillars** | Dramas, International, Comedies | Action, Suspense, Comedy | Animation, Family, Marvel/Star Wars |
| **Release Strategy** | High-velocity streaming originals | Deep archival cinema + originals | Franchise IP + Tentpole releases |

---

## 🚀 Prerequisites & Getting Started

### Prerequisites
- [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Free download for Windows)
- Microsoft Excel or any CSV viewer (optional, for inspecting raw datasets)

### How to Run Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/bhattchintan8540-cmd/Data-Analytics-with-Power-BI.git
   ```

2. **Navigate to the Project 2 directory**:
   ```bash
   cd "Data-Analytics-with-Power-BI/Project 2"
   ```

3. **Open the Power BI file**:
   - Navigate to `Working File/`
   - Double-click **`OTT Dashboard.pbix`** to launch the interactive report in Power BI Desktop.

4. **Refresh Data (if required)**:
   - In Power BI Desktop, click **Refresh** on the Home tab to update data tables from the `Dataset/` folder.
   - Use the interactive year slicers and country maps on each tab to cross-filter the report dynamically.

---

## 🛠️ Tech Stack & Tools

- **Business Intelligence**: Microsoft Power BI Desktop
- **Data Modeling & Queries**: Power Query (M Language), DAX
- **Data Formats**: Structured Comma-Separated Values (`.csv`)
- **Visual Paradigms**: Filled Maps, Funnel Charts, Stacked Area Charts, Clustered Columns, Donut Charts, KPI Cards, Interactive Slicers

---

## 🔮 Future Enhancements

- [ ] Build a unified multi-platform comparison page synthesizing all 3 services into a single benchmarking matrix.
- [ ] Incorporate IMDb ratings and Rotten Tomatoes score metrics to benchmark library quality vs. quantity.
- [ ] Add sentiment analysis on title descriptions using natural language processing (NLP).
- [ ] Implement director and actor co-occurrence network analysis to identify prolific platform creators.

---
*⭐ If you find this project informative, consider giving the repository a star!*
