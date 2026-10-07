# 🌠 NASA Meteorite Landing Analysis

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![NASA](https://img.shields.io/badge/NASA-Open%20Data-E03C31?style=for-the-badge&logo=nasa&logoColor=white)](https://data.nasa.gov/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

> **End-to-end exploratory data analysis and interactive dashboard** on 45,000+ meteorite landings recorded by NASA & The Meteoritical Society — spanning over 1,000 years of extraterrestrial impacts.

<!-- Add a banner image or dashboard screenshot here -->
<!-- ![Dashboard Preview](assets/dashboard_preview.png) -->

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Findings](#-key-findings)
- [Tech Stack](#-tech-stack)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Analysis Highlights](#-analysis-highlights)
- [Power BI Dashboard](#-power-bi-dashboard)
- [Getting Started](#-getting-started)
- [Future Work](#-future-work)
- [Author](#-author)

---

## 🔭 Overview

This project performs a comprehensive analysis of NASA's Meteorite Landings dataset, combining **Python-based statistical analysis** with an **interactive Power BI dashboard** to uncover patterns in meteorite discoveries across time, geography, and physical properties.

### What This Project Demonstrates

| Skill | Application |
|-------|-------------|
| **Data Cleaning** | Handling missing values, date parsing, outlier detection |
| **Feature Engineering** | Mass categorization, continent estimation, classification grouping |
| **Statistical Analysis** | Hypothesis testing (Mann-Whitney U, Chi-Square), distribution fitting |
| **Geospatial Analysis** | Global mapping, hemisphere analysis, continent-level aggregation |
| **Data Visualization** | 20+ publication-quality charts with Matplotlib, Seaborn, and Plotly |
| **Business Intelligence** | 3-page interactive Power BI dashboard with DAX measures |

---

## 🔑 Key Findings

1. **97% of cataloged meteorites were "Found"** (discovered after landing), only ~3% were witnessed falling — highlighting massive observational bias.

2. **Antarctica is the #1 meteorite discovery site** — not because more land there, but because dark rocks stand out on white ice and are well-preserved.

3. **Meteorite discoveries exploded after 1970** — driven by systematic Antarctic search programs (ANSMET) and Saharan expeditions.

4. **Mass follows a log-normal distribution** — most meteorites are small (median ~30g), but outliers like Hoba (60,000 kg) skew the data enormously.

5. **L-chondrites dominate** — ordinary chondrites (L, H, LL groups) make up ~80% of all classified meteorites.

6. **Found meteorites are significantly heavier** than fallen ones (Mann-Whitney U test, p < 0.001) — larger fragments survive longer on the surface.

7. **Northern Hemisphere records more sightings** (Fell) due to higher population density, but Southern Hemisphere dominates finds (Found) due to Antarctic programs.

8. **Classification diversity has increased 5x** since 1950 — reflecting advances in meteoritics and analytical techniques.

9. **Mass correlates weakly with latitude** — suggesting no strong geographic mass-selection bias beyond collection methodology.

10. **The heaviest meteorites cluster in Africa** — the Hoba meteorite in Namibia (60 tonnes) remains the largest known meteorite on Earth.

---

## 🛠 Tech Stack

| Category | Tools |
|----------|-------|
| **Languages** | Python 3.10+ |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Statistical Analysis** | SciPy (Mann-Whitney U, Chi-Square, Kolmogorov-Smirnov) |
| **Dashboard** | Microsoft Power BI |
| **Platform** | Kaggle Notebooks |
| **Data Source** | [NASA Open Data Portal](https://data.nasa.gov/) |

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| **Source** | [NASA Meteorite Landings](https://data.nasa.gov/Space-Science/Meteorite-Landings/gh4g-9sfh) via The Meteoritical Society |
| **Records** | ~45,716 meteorite entries |
| **Time Span** | 860 AD – 2013 |
| **Key Features** | Name, Mass, Classification, Coordinates, Fall/Found status, Year |
| **Format** | CSV |

### Data Dictionary

| Column | Type | Description |
|--------|------|-------------|
| `name` | String | Official meteorite name |
| `id` | Integer | Unique identifier |
| `nametype` | String | "Valid" or "Relict" |
| `recclass` | String | Meteorite classification (e.g., L5, H6, Iron) |
| `mass (g)` | Float | Mass in grams |
| `fall` | String | "Fell" (witnessed) or "Found" (discovered) |
| `year` | DateTime | Year of fall/find |
| `reclat` | Float | Latitude |
| `reclong` | Float | Longitude |
| `GeoLocation` | String | Combined lat/long |

---

## 📂 Project Structure

```
nasa-meteorite-analysis/
│
├── 📓 notebooks/
│   └── nasa_meteorite_analysis.ipynb    # Main Kaggle notebook (full EDA)
│
├── 📊 powerbi/
│   ├── meteorite_dashboard.pbix         # Power BI dashboard file
│   ├── meteorite_theme.json             # Custom dark theme
│   └── dashboard_guide.md              # Step-by-step build instructions
│
├── 📁 data/
│   ├── raw/
│   │   └── Meteorite_Landings.csv       # Original NASA dataset
│   └── processed/
│       └── meteorite_landings_cleaned.csv  # Cleaned & feature-engineered
│
├── 🖼 assets/
│   ├── dashboard_page1.png              # Dashboard screenshots
│   ├── dashboard_page2.png
│   ├── dashboard_page3.png
│   ├── geospatial_map.png               # Key visualization exports
│   ├── temporal_analysis.png
│   └── mass_distribution.png
│
├── 📄 README.md                         # This file
├── 📄 LICENSE                           # MIT License
└── 📄 requirements.txt                  # Python dependencies
```

---

## 📈 Analysis Highlights

### 🗺 Geospatial Distribution
Meteorite landings span all seven continents, with a striking concentration in **Antarctica** (systematic search programs), the **Sahara Desert** (dark rocks on sand), and **populated areas of Europe/Asia** (higher witness rates).

<!-- ![Geospatial Map](assets/geospatial_map.png) -->

### ⏰ Temporal Trends
Discovery rates remained low until the 1970s, then surged exponentially — driven by the **Antarctic Search for Meteorites (ANSMET)** program and increased scientific interest.

<!-- ![Temporal Analysis](assets/temporal_analysis.png) -->

### ⚖️ Mass Distribution
Mass follows a **log-normal distribution** spanning 8 orders of magnitude — from dust particles (<1g) to the 60-tonne Hoba meteorite.

<!-- ![Mass Distribution](assets/mass_distribution.png) -->

---

## 📊 Power BI Dashboard

The interactive dashboard consists of **3 pages**:

| Page | Focus | Key Visuals |
|------|-------|-------------|
| **Executive Overview** | High-level KPIs & global picture | KPI cards, world map, timeline, donut chart |
| **Classification & Mass** | Deep dive into meteorite types | Treemap, bar charts, box plots |
| **Geospatial Deep Dive** | Geographic patterns | Interactive map, continent comparison, scatter plots |

### DAX Measures Created
- Total Meteorites, Total Mass (MT), Average Mass (kg)
- Fell/Found percentages
- Year-over-Year growth rates
- Conditional formatting rules

> 📖 See [`powerbi/dashboard_guide.md`](powerbi/dashboard_guide.md) for step-by-step build instructions.

<!-- ![Dashboard](assets/dashboard_preview.png) -->

---

## 🚀 Getting Started

### Option 1: Kaggle (Recommended)
1. Go to the [Kaggle Notebook](YOUR_KAGGLE_LINK_HERE)
2. Click **Copy & Edit** to run it yourself
3. The dataset loads automatically from Kaggle

### Option 2: Local Setup
```bash
# Clone the repo
git clone https://github.com/laraibzafarlaraib/nasa-meteorite-analysis.git
cd nasa-meteorite-analysis

# Create virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook notebooks/nasa_meteorite_analysis.ipynb
```

### Requirements
```txt
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
plotly>=5.14.0
scipy>=1.10.0
scikit-learn>=1.2.0
jupyter>=1.0.0
```

---

## 🔮 Future Work

- [ ] **Predictive modeling**: Classify meteorite type from mass and location features
- [ ] **Clustering analysis**: K-Means/DBSCAN on geographic coordinates to find landing hotspots
- [ ] **Time series forecasting**: Predict future discovery rates
- [ ] **NLP on meteorite names**: Extract naming patterns and conventions
- [ ] **Integration with asteroid tracking data**: Correlate landings with known asteroid orbits
- [ ] **Streamlit web app**: Deploy an interactive version online

---

## 👩‍💻 Author

**Laraib Zafar**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/laraib-zafar-5465a5267)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github)](https://github.com/laraibzafarlaraib)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail)](mailto:laraibzafarlaraib@gmail.com)

---

## 📜 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **NASA Open Data Portal** for making this dataset publicly available
- **The Meteoritical Society** for maintaining the comprehensive meteorite catalog
- **ANSMET** (Antarctic Search for Meteorites) for decades of systematic collection

---

<p align="center">
  <i>⭐ If you found this project useful, give it a star!</i>
</p>
