# NASA Meteorite Landing Analysis

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![NASA](https://img.shields.io/badge/NASA-Open%20Data-E03C31?style=for-the-badge&logo=nasa&logoColor=white)](https://data.nasa.gov/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

> **End-to-end exploratory data analysis and interactive dashboard** on 45,000+ meteorite landings recorded by NASA & The Meteoritical Society, spanning over 1,000 years of extraterrestrial impacts.

<!-- Add a banner image or dashboard screenshot here -->
<!-- ![Dashboard Preview](assets/dashboard_preview.png) -->

---

##  Overview

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


##  Tech Stack

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

## Dataset

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
| `mass` | Float | Mass in grams |
| `fall` | String | "Fell" (witnessed) or "Found" (discovered) |
| `year` | DateTime | Year of fall/find |
| `reclat` | Float | Latitude |
| `reclong` | Float | Longitude |
| `GeoLocation` | String | Combined lat/long |


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

##  Author

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
