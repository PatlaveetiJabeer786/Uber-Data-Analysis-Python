# 🚗 Uber Data Analysis — Python EDA

[![Header](https://capsule-render.vercel.app/api?type=waving&color=0:000000,50:1a1a1a,100:276EF1&height=220&section=header&text=Uber%20Data%20Analysis&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Python%20%7C%20Pandas%20%7C%20Matplotlib%20%7C%20EDA%20%7C%20Trip%20Intelligence&descAlignY=58&descSize=17)](https://github.com/PatlaveetiJabeer786/Uber-Data-Analysis-Python)

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Domain](https://img.shields.io/badge/Domain-Ride%20Hailing%20%26%20Mobility-276EF1?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed%20✅-brightgreen?style=for-the-badge)

</div>

---

<div align="center">

```
╔═══════════════════════════════════════════════════════════════════════╗
║                                                                       ║
║   🚗  UBER DATA ANALYSIS  |  PYTHON EDA  |  TRIP INTELLIGENCE  🚗    ║
║                                                                       ║
║   Data Cleaning  •  Peak Hours  •  Trip Purpose  •  Category Split   ║
║                                                                       ║
╚═══════════════════════════════════════════════════════════════════════╝
```

</div>

---

## 🌟 STAR Method — Project Breakdown

---

### 🔴 S — Situation (Business Problem)

> *"Uber generates millions of trip records daily — but raw data is messy, inconsistent, and unreadable. Missing values, broken datetime formats, and unstructured trip purpose fields make it impossible to answer business-critical questions: When are rides requested most? What are people actually using Uber for? Are Business trips longer and more valuable than Personal ones? Without Python EDA, these questions remain unanswered."*

**Pain Points Uber's data team faced:**

```
┌─────────────────────────────────────────────────────────────────────┐
│  ❌ Missing values in START_DATE, END_DATE, PURPOSE columns         │
│  ❌ Inconsistent datetime formats — couldn't extract hours or days  │
│  ❌ No separation between Business vs Personal trip behaviour        │
│  ❌ No visibility into peak demand hours for driver allocation       │
│  ❌ Trip purpose field had 1,000+ NaN values — hiding usage patterns │
└─────────────────────────────────────────────────────────────────────┘
```

---

### 🎯 T — Task (My Role as Data Analyst)

I was given the raw **UberDataset.csv** and tasked with:

| Task | Objective |
|------|-----------|
| 🧹 **Data Cleaning** | Fix nulls, parse datetimes, standardize categories |
| 🔍 **EDA** | Explore distributions, correlations, outliers |
| 📅 **Time Analysis** | Extract hour, day, month from trip timestamps |
| 🗂️ **Category Analysis** | Compare Business vs Personal trip patterns |
| 🎯 **Purpose Analysis** | Identify the most common trip purposes |
| 📊 **Visualization** | Build clear charts for every key insight |

---

### ⚙️ A — Action (What I Did — Step by Step)

#### Step 1 — Data Cleaning

```
╔══════════════════════════════════════════════════════════════════╗
║              DATA QUALITY ISSUES I FIXED                         ║
╠═══════════════════════╦══════════════════════════════════════════╣
║  ❌ PROBLEM           ║  ✅ MY PYTHON SOLUTION                   ║
╠═══════════════════════╬══════════════════════════════════════════╣
║  NaN in PURPOSE col   ║  Filled with "NOT SPECIFIED"            ║
║  Datetime as string   ║  pd.to_datetime() — extracted hr/day    ║
║  Missing MILES values ║  Removed rows — outlier cleaning        ║
║  Duplicate records    ║  df.drop_duplicates() applied           ║
║  Category mismatch    ║  Standardized to Business / Personal    ║
╚═══════════════════════╩══════════════════════════════════════════╝
```

#### Step 2 — Feature Engineering
- Extracted **Hour of Day**, **Day of Week**, **Month** from START_DATE
- Created **Trip Duration** column = END_DATE − START_DATE (in minutes)
- Flagged **long-distance trips** (MILES > 20) for outlier review

#### Step 3 — EDA & Visualizations
- Distribution of trips by **Hour of Day** — peak demand windows
- **Business vs Personal** split — category comparison charts
- **Most common trip purposes** — bar chart (Meetings, Errands, etc.)
- **Miles distribution** — histogram showing short vs long rides
- **Day-of-week heatmap** — busiest days across both categories
- **Monthly trend** — ride volume across all months

---

### 📈 R — Result (Key Insights & Business Outcomes)

#### 🕐 Peak Hours & Demand
- **8–9 AM and 5–6 PM** are the two highest demand windows — classic commute patterns
- **Midnight to 4 AM** has the lowest trip volume — driver cost reduction opportunity
- Uber can use this to **dynamically price surge** and **allocate drivers** more efficiently

#### 🏢 Business vs Personal Trips
- **Business trips** are significantly **longer in miles** than Personal trips — higher revenue per ride
- **Personal trips** are more frequent but shorter — volume drives base revenue
- Business trips spike sharply on **Monday–Wednesday** — corporate travel pattern
- Personal trips peak on **Friday and Saturday** — weekend leisure usage

#### 🎯 Trip Purpose Insights
- **Meetings** is the #1 business trip purpose — followed by Errands and Customer Visits
- **Meal/Entertain** dominates personal category — dining and social outings
- Uber can target **corporate accounts** for Meeting trips — high frequency + high miles = premium revenue

#### 🗺️ Distance & Duration
- Majority of trips are **under 10 miles** — Uber is primarily a short-distance urban tool
- Long-distance trips (20+ miles) correlate with **airport pickups** — opportunity for Uber premium offerings

---

## 📊 EDA Charts Summary

| Chart | What It Shows | Business Use |
|-------|--------------|-------------|
| 📊 **Trip Hour Distribution** | Peak demand by hour of day | Surge pricing & driver scheduling |
| 🍩 **Business vs Personal Donut** | Category split of all trips | Revenue stream segmentation |
| 📊 **Purpose Bar Chart** | Most common trip reasons | Corporate partnership targeting |
| 📉 **Miles Histogram** | Short vs long ride distribution | Fleet type optimization |
| 📅 **Day of Week Bar** | Busiest days per category | Marketing campaign timing |
| 📈 **Monthly Trend Line** | Ride volume across 12 months | Seasonal planning & forecasting |

---

## 📈 Business Value Delivered

| ❌ Before Analysis | ✅ After Analysis |
|-------------------|-----------------|
| No peak hour visibility | 8–9 AM and 5–6 PM confirmed as surge windows |
| Business vs Personal mixed | Clear category split with distinct behaviour |
| 1,000+ NaN PURPOSE rows | Cleaned, labeled, and fully analyzable |
| No trip purpose intelligence | Meetings #1 — corporate strategy enabled |
| No distance patterns | Short-trip urban dominance confirmed |
| Raw unusable CSV | Clean, structured dataset ready for modelling |

---

## 📁 Project Structure

```
Uber-Data-Analysis-Python/
│
├── UberDataset.csv                   # Raw Uber trip dataset
├── Uber_Analsysis_Project.ipynb      # Full Python EDA Notebook
├── Uber_Questions.jpg                # Analysis questions reference
└── README.md
```

---

## 🚀 How to Run

```bash
pip install pandas matplotlib seaborn jupyter
jupyter notebook Uber_Analsysis_Project.ipynb
```

---

## 🧠 Skills Demonstrated

```
✅  Pandas — data cleaning, datetime parsing, feature engineering
✅  Matplotlib & Seaborn — 6 business insight visualizations
✅  EDA methodology — distributions, correlations, outlier detection
✅  Datetime engineering — hour, day, month extraction from raw strings
✅  NaN handling — strategic imputation vs deletion decisions
✅  Business storytelling — every chart tied to a real Uber decision
```

---

## 👨‍💻 About Me

- 🔗 **LinkedIn:** [linkedin.com/in/jabeer-patlaveeti](https://linkedin.com/in/jabeer-patlaveeti)
- 📧 **Email:** jabeerpatlaveeti@gmail.com
- 🌐 **GitHub:** [github.com/PatlaveetiJabeer786](https://github.com/PatlaveetiJabeer786)

---

<div align="center">

⭐ **Found this useful? Please give it a Star!** ⭐

</div>

[![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:000000,50:1a1a1a,100:276EF1&height=100&section=footer)](https://github.com/PatlaveetiJabeer786/Uber-Data-Analysis-Python)
