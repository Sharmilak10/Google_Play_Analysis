# Google Play Store Analysis

## 📌 Project Overview
This project analyzes data from the Google Play Store to gain insights about app categories, ratings, installs, and more.  
The analysis is divided into three tasks, each focusing on different aspects of the dataset.

## 📂 Files in This Project
- **googleplaystore.csv** → Dataset containing app details.
- **Task1.ipynb** → First analysis task.
- **Task2.ipynb** → Second analysis task.
- **Task3.ipynb** → Third analysis task.
- **requirements.txt** → List of required Python packages.

## 🛠️ Requirements
Before running the notebooks, install the required packages:

```bash
pip install -r requirements.txt
```

---

## 📊 Task Explanations

### **Task 1 – Revenue vs Installs for Paid Apps**
- Filters the dataset to include only **Paid apps**.
- Cleans and converts `Installs` and `Price` columns to numeric values.
- Calculates **Revenue** for each app as `Installs × Price`.
- Creates a **scatter plot** of Revenue vs. Installs, color-coded by app category.
- Adds a **trendline** to visualize the correlation.

---

### **Task 2 – Avg Installs & Revenue for Free vs Paid Apps (Top 3 Categories)**
- Cleans and filters the dataset based on:
  - Installs ≥ 10,000
  - Revenue ≥ $10,000
  - Android version > 4.0
  - App size > 15 MB
  - Content Rating = "Everyone"
  - App name length ≤ 30 characters
- Identifies the **top 3 categories** based on average installs.
- Compares **Free vs Paid apps** in these categories using a **dual-axis chart**:
  - Bar plot for average installs
  - Point plot for average revenue
- Graph is **time-restricted** to run only between **1 PM and 2 PM IST**.

---

### **Task 3 – Bubble Chart with Sentiment & Category Translation**
- Cleans data and converts sizes to MB.
- Performs **sentiment analysis** (subjectivity) on app names.
- Filters apps with:
  - Rating > 3.5
  - Reviews > 500
  - No “S” in app name
  - Sentiment subjectivity > 0.5
  - Installs > 50,000
- Restricts to specific categories (Game, Beauty, Business, etc.).
- Translates some category names into **Hindi**, **Tamil**, and **German**.
- Creates a **bubble chart**:
  - X-axis → App Size (MB)
  - Y-axis → Rating
  - Bubble size → Installs
  - Special color for "Game" category
- Graph is **time-restricted** to run only between **5 PM and 7 PM IST**.

---
