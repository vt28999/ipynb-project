# 🎬 IMDb Movies Data Analysis & Visualization

> A comprehensive Exploratory Data Analysis (EDA) project on IMDb movie data using Python, Pandas, NumPy, Seaborn, Matplotlib, and YData Profiling.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blue?style=for-the-badge&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-green?style=for-the-badge)

---

## 📖 Overview

This project performs an end-to-end analysis of an IMDb movies dataset to uncover meaningful insights about movie ratings, genres, directors, revenues, certificates, and audience engagement.

The notebook covers the complete data analytics workflow:

- Data Cleaning
- Data Transformation
- Missing Value Analysis
- Exploratory Data Analysis (EDA)
- Statistical Insights
- Data Visualization
- Automated Data Profiling
- Business-Oriented Findings

---

## 🚀 Key Objectives

- Identify **Hidden Gem Movies**
- Detect **Overhyped Movies**
- Analyze movie ratings across years
- Discover the most successful genres
- Explore top-performing directors
- Study revenue patterns and audience voting behavior
- Generate visual insights using professional charts

---

## 🛠️ Tech Stack

| Tool | Purpose |
|--------|---------|
| Python | Programming Language |
| Pandas | Data Manipulation |
| NumPy | Numerical Computing |
| Matplotlib | Visualization |
| Seaborn | Statistical Visualization |
| YData Profiling | Automated EDA Report |
| Jupyter Notebook | Development Environment |

---

## 📂 Project Structure

```text
IMDb-Movie-Analysis/
│
├── project.ipynb
├── movies.csv
├── profiling_report.html
└── README.md
```

---

## 📊 Dataset Features

| Feature | Description |
|----------|-------------|
| title | Movie Name |
| year | Release Year |
| duration | Runtime (minutes) |
| rating | IMDb Rating |
| votes | Number of User Votes |
| gross_income | Gross Revenue |
| genre | Movie Genres |
| certificate | Movie Certification |
| directors_name | Director Name |
| stars_name | Lead Actors |

---

## 🧹 Data Cleaning & Preprocessing

### Duration Conversion

```python
df['duration'] = df['duration'].str.replace(' min','')
```

### Gross Income Cleaning

```python
df['gross_income'] = (
    df['gross_income']
    .str.replace(',', '')
    .astype(float)
)
```

### Votes Cleaning

```python
df['votes'] = (
    df['votes']
    .str.replace(',', '')
    .astype(int)
)
```

### Missing Value Analysis

```python
df.isnull().sum()
```

---

## 🔍 Exploratory Data Analysis

### ⭐ Hidden Gems

Movies with:

- High IMDb Ratings
- Low Vote Counts

Used to identify underrated films that deserve more recognition.

---

### 💰 Overhyped Movies

Movies with:

- High Revenue
- Low Ratings

Helpful for understanding commercially successful but critically weak films.

---

### 🎭 Genre Analysis

Analysis includes:

- Most Common Genres
- Highest Rated Genres
- Highest Grossing Genres

```python
df['genre'].str.split(',').explode()
```

---

### 🎬 Director Analysis

Discover:

- Most Active Directors
- Highest Revenue Generating Directors
- Average Ratings by Director

```python
df.groupby('directors_name')
```

---

### 🏆 Certificate Analysis

Evaluate:

- Most Common Certifications
- Revenue by Certification
- Average Runtime by Certification

Examples:

- U
- UA
- PG-13
- R

---

## 📈 Visualizations

The project includes multiple visualizations:

### Rating Distribution

- Histogram
- Density Analysis

### Movie Production Trend

- Movies Released Per Year

### Rating Trends

- Average Rating by Year

### Correlation Heatmap

Relationships between:

- Rating
- Votes
- Duration
- Revenue
- Year

### Top Actors Analysis

- Most Frequently Appearing Actors

### Revenue Analysis

- Highest Grossing Movies
- Revenue Distribution

---

## 📋 Automated Profiling Report

Generate a complete EDA report with:

```python
from ydata_profiling import ProfileReport

profile = ProfileReport(df)
profile.to_file("profiling_report.html")
```

The report includes:

- Missing Values
- Correlations
- Variable Statistics
- Data Quality Checks
- Interactive Visualizations

---

## 🎯 Business Questions Answered

✔ Which movies are hidden gems?

✔ Which movies are overhyped?

✔ Which genres dominate the industry?

✔ Which genres generate the highest revenue?

✔ Which directors consistently perform well?

✔ Does movie duration affect ratings?

✔ How have ratings evolved over time?

✔ What factors influence audience engagement?

---

## 📸 Sample Insights

- Drama and Action genres dominate the dataset.
- High revenue does not always imply high ratings.
- Several highly rated movies receive relatively few votes.
- Director reputation often correlates with audience engagement.
- Revenue distribution is heavily skewed toward a small number of blockbuster films.

---

## ⚡ Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/imdb-movie-analysis.git
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn ydata-profiling
```

### Launch Notebook

```bash
jupyter notebook
```

Open:

```text
project.ipynb
```

---

## 🎓 Learning Outcomes

This project demonstrates practical experience with:

- Data Cleaning
- Data Wrangling
- Exploratory Data Analysis
- Statistical Thinking
- Data Visualization
- Business Analytics
- Python Data Science Ecosystem

---

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

---

## ⭐ Support

If you found this project helpful, please consider giving it a **Star ⭐** on GitHub.

It helps others discover the project and motivates future improvements.

---

## 👨‍💻 Author

**Your Name**

Data Analyst | Data Science Enthusiast | Python Developer

---

> Transforming raw movie data into actionable insights through analytics and visualization.
