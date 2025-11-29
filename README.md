# Zomato-Data-Analysis(EDA)

## Project Overview
This project performs an end-to-end Exploratory Data Analysis (EDA) on a dataset containing over **36,000 restaurant listings** from Zomato in Bangalore, India. The primary goal is to derive actionable business insights that explain consumer behavior, rating distributions, and the success factors of different restaurant types and locations.

The analysis covers data cleaning challenges (handling messy rating/cost columns) and uses powerful visualization techniques to tell a data story.

## 🔑 Key Findings & Business Insights

* **Premium Service Correlates with Quality:** Restaurants that offer **Table Booking** have an average rating of **4.14/5**, significantly higher than those that do not (3.63/5). This suggests that restaurants investing in the full dining experience attract higher customer satisfaction.
* **Online Dominance:** Approximately **60%** of all restaurants listed offer the **Online Ordering** service, reflecting the massive shift in consumer preference toward delivery.
* **Cuisine Demand:** The three most popular and available cuisines are **North Indian, Chinese, and South Indian**, indicating high market saturation and demand in these categories.
* **Geographic Focus:** The **BTM** locality has the highest concentration of restaurants, followed by **Whitefield** and **HSR Layout**, highlighting primary target markets for new establishments.
* **Cost vs. Rating:** The relationship between cost and rating is weak, suggesting that while price is a factor, high ratings are achievable across various price ranges, primarily driven by quality of service and food.

## 🛠️ Technical Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook (Google Colab)

## 📊 Visualizations

Here are some of the key insights visualized from the dataset:

### Top 10 Locations by Restaurant Volume
This bar chart reveals the most competitive areas in the city based on the sheer number of listed restaurants.
<img width="989" height="590" alt="1" src="https://github.com/user-attachments/assets/123d24f8-2a70-4c81-adbc-67b955bf5b9f" />

***

### Top 10 Most Popular Cuisines
**Insight:** North Indian and Chinese cuisines dominate the market, appearing in the majority of restaurant menus.
<img width="989" height="590" alt="2" src="https://github.com/user-attachments/assets/3540c62a-c5fd-4059-9f20-28d1536558b6" />

***

### Online Ordering Penetration
**Insight:** Approximately 60% of restaurants offer online ordering, highlighting the necessity of a digital presence for survival in this market.
<img width="558" height="581" alt="3" src="https://github.com/user-attachments/assets/f8ad663c-ee2e-4fad-a5fc-c4990336ac4b" />

***

### Rating Distribution by Table Booking Availability
This box plot clearly shows the difference in the median and spread of ratings between restaurants that offer table booking and those that do not.
<img width="691" height="470" alt="4" src="https://github.com/user-attachments/assets/a1f2a912-b44d-40c8-95fd-08f6ff8525e1" />

***

### Cost for Two vs. Rating
This scatter plot explores the correlation between the approximate cost for two people and the restaurant's final rating, using the "Online Order" status as a distinguishing factor.
<img width="863" height="547" alt="5" src="https://github.com/user-attachments/assets/3107cece-02d9-4f27-b3ec-9d7b347d8c04" />

***

## Data Preparation & Cleaning Highlights
The analysis required significant cleaning, including:
* Standardizing the `rate` column (converting string format 'X/5' to float X, and handling 'NEW' or '-' values as missing data).
* Cleaning the `approx_cost(for two people)` column by removing comma separators and converting the values to a numeric format.
* Exploding the comma-separated `cuisines` column for accurate popularity counts.
* Removing duplicate entries and records with incomplete critical data (`rate`, `cost`, `location`).
