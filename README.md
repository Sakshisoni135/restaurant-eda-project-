# restaurant-eda-project-
EDA on 9500+ restaurants dataset (Zomato-style)



#  Python EDA Project: Restaurant Dataset

###  Project Overview:
Performed Exploratory Data Analysis (EDA) on a dataset of 9,500+ restaurants using **Python** to extract insights on cuisine trends, customer ratings, price range distribution, and delivery preferences.

---

###  Tools & Technologies Used:
- **Language:** Python 3
- **Libraries:** 
  - `pandas` – for data loading and manipulation
  - `numpy` – for numerical operations
  - `matplotlib` & `seaborn` – for visualizations
- **Platform:** Google Colab
- **Output:** Cleaned dataset, correlation matrix, plots, and business insights

---

###  Key Python Steps Included:
1. **Data Loading & Preview**
   - `pd.read_csv()` to load the data
   - `.head()`, `.info()`, `.describe()` for overview

2. **Missing Value Treatment**
   - `.isnull().sum()` to identify missing values
   - `.fillna()` or `.dropna()` used where needed

3. **Univariate Analysis (Single Variable)**
   - `sns.countplot()`, `sns.histplot()`, `sns.barplot()`
   - Top 10 cities, cuisine frequency, price range

4. **Bivariate Analysis (Two Variables)**
   - `sns.scatterplot()`, `sns.boxplot()`
   - Votes vs Ratings, Cost vs Rating, Table Booking vs Rating

5. **Correlation Analysis**
   - `df.corr()` to find relationships between numeric features
   - `sns.heatmap()` to visualize correlations

6. **Outlier Handling & Export**
   - Used `.quantile()` to filter top 1% outliers
   - Saved cleaned data: `df.to_csv('cleaned_eda.csv')`

---

###  Sample Visualization Code Used:

```python
plt.figure(figsize=(10,6))
sns.scatterplot(data=df, x='Average Cost for two', y='Aggregate rating', hue='Price range')
plt.title('Cost vs Rating')
plt.show()
