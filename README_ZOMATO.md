# 🍽️ Zomato Cuisine Analytics

This project analyzes Zomato restaurant data to uncover insights about cuisines, ratings, votes, and pricing using pandas and Plotly.

---

## 📌 Objective

- Clean messy CSV data from Zomato
- Analyze and rank cuisines by rating, popularity, and cost
- Visualize top trends using bar plots and scatter plots

---

## 📁 Input File

- `data.xlsx - zomato.csv` (rename your CSV file if needed)

---

## 🚦 Pipeline Overview

### 1. **Data Cleaning**
- Remove duplicates
- Fill missing ratings, votes, and cost with zeros
- Convert `approx_cost(for two people)` to float
- Format location and cuisine fields
- Extract `main_cuisine`

### 2. **Cuisines Exploded**
- Break comma-separated cuisines into individual rows for deeper aggregation

### 3. **Cuisine Summary Metrics**
- `avg_rating`: Average rating per cuisine
- `total_votes`: Total votes received
- `avg_cost`: Average cost for two people
- `restaurant_count`: Number of restaurants per cuisine

---

## 📊 Visualizations

- **Top 15 cuisines by average rating** → `top_rating_cuisines.html`
- **Top 15 cuisines by total votes** → `top_voted_cuisines.html`
- **Cost vs Rating scatter plot** → `price_vs_rating.png`

---

## 🔍 Key Insights (Printed in Terminal)
- Best rated cuisines (min 5 restaurants)
- Most popular cuisines (by vote count)
- Most expensive cuisines (by average cost)
- Top 5 best-rated restaurants overall

---

## 📤 Output Files

Saved to the `output/` directory:
- `cleaned_data.csv`
- `cuisine_summary.csv`
- `cuisine_summary.xlsx`
- `cuisine_summary.json`
- Plot files (`.html`, `.png`)

---

## ▶️ How to Run

```bash
python zomato_analysis.py
```

Make sure the script and CSV file are in the same folder.

---

## 🛠️ Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- plotly
- logging
- os

---

## 👨‍💻 Author

Made with ❤️ for food + data enthusiasts!
