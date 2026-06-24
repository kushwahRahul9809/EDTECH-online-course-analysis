

# 🎓 EdTech Online Courses – Power BI Dashboard

An interactive Power BI dashboard analyzing **8,092 online courses** scraped from four major e-learning platforms — **Coursera, Future Learn, Udacity, and Simplilearn** — to uncover patterns in course categories, formats, languages, ratings, and viewer engagement.


---

## 📁 Repository Contents

| File | Description |
|---|---|
| `edtech__.pbix` | Power BI report file (data model + dashboard) |
| `Online_Courses.csv` | Raw dataset used to build the report |
| `README.md` | This file |

---

## 📊 About the Dataset

`Online_Courses.csv` contains **8,092 course records** across **45 columns**, aggregated from multiple course-listing platforms. Because each platform exposes a different schema, the dataset is wide and intentionally sparse — fields like `Program Type`, `Number of Reviews`, and `Price` apply only to certain platforms (e.g., Coursera Specializations) and are blank for others.

**Platform breakdown:**

| Site | Courses |
|---|---|
| Future Learn | 4,843 |
| Coursera | 2,819 |
| Udacity | 282 |
| Simplilearn | 148 |

**Core fields used in the analysis:** `Title`, `Category`, `Sub-Category`, `Course Type`, `Language`, `Skills`, `Rating`, `Number of viewers`, `Duration`, `Site`.

---

## 📈 Dashboard Overview

The report (**"EDTECH ONLINE_COURSE ANALYSIS DASHBOARD"**) is a single-page Power BI dashboard built around four KPI cards, one slicer, and three charts:

| Visual | Type | What it shows |
|---|---|---|
| **Total Courses** | Card | Overall course count in the model |
| **Total number of views** | Card | Sum of `Number of viewers` across all courses |
| **Skills by Rating** | Card | Top skill paired with its rating |
| **Course by Category** | List Slicer | Filters the whole page by `Category` |
| Sub-Category vs. Course Type | Line & Stacked Column Combo Chart | Count of `Course Type` broken down by `Sub-Category` |
| Course Type vs. Skills | Stacked Area Chart | Count of distinct skills taught, by `Course Type` |
| Language distribution | Donut Chart | Count of skills/courses split by `Language` |

---

## 🔍 Key Insights

- **Course catalog:** 8,092 total listings representing **4,908 unique course titles** (many courses are cross-listed or repeated across platforms/languages).
- **Top categories:** Business (895), Computer Science (455), Data Science (448), Health (264), and Information Technology (221) dominate the catalog.
- **Top sub-categories:** Leadership & Management, Data Analysis, Software Development, Business Essentials, and Machine Learning are the five most common.
- **Course format:** Standard "Course" is the most common type (2,307), followed by Specializations (414), Professional Certificates (81), and Projects (17).
- **Language:** The catalog is overwhelmingly English-taught (2,726 of ~2,816 language-tagged courses); Spanish (58) and French (11) are the next most common.
- **Ratings:** Among courses with a published rating (~2,742 records), the average rating is **4.66 / 5**, with most courses rated between 4.6 and 4.8 — indicating generally high learner satisfaction across platforms.
- **Engagement:** Total recorded views across rated/viewed courses exceed **8.4 million**, though viewership is highly skewed — a small number of flagship courses (e.g., Andrew Ng's *Machine Learning Specialization*) drive a disproportionate share of views.

---

## ⚠️ Data Quality Notes

- The dataset merges listings from four platforms with different schemas, so **most columns are sparse by design** (e.g., `Unique Projects`, monthly-access pricing tiers, and `Rank` are >99% empty — they only apply to specific platforms/program types).
- `Rating` and `Number of viewers` are populated for roughly **1 in 3 rows**, mainly Coursera entries.
- `Price` and `Premium course` fields mix raw dollar amounts with free-text promotional descriptions, so they were treated as categorical/text rather than parsed as currency in this analysis.
- Title duplication (~3,184 repeated titles) reflects the same course appearing under multiple languages, sub-categories, or listing pages rather than data entry error.

---

## 🛠️ Tools Used

- **Power BI Desktop** – data modeling and dashboard design
- **CSV / Excel** – source data
- Visual types: Card, List Slicer, Line & Stacked Column Combo Chart, Stacked Area Chart, Donut Chart

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open `edtech__.pbix` in **Power BI Desktop** (free download from Microsoft).
3. Use the **Course by Category** slicer to filter the dashboard by subject area.
4. Explore the charts to compare course types, languages, and skill coverage.

---

## 📌 Possible Next Steps

- Parse `Price` into a clean numeric field for cost-vs-rating analysis.
- Normalize `Duration` (currently free text, e.g. *"Approximately 3 months to complete"*) into a numeric weeks/months field for trend analysis.
- Add a platform-level comparison page (Coursera vs. Future Learn vs. Udacity vs. Simplilearn).

---

## 📄 License

This project is for educational and portfolio purposes. Course data was sourced from publicly listed course catalogs.
