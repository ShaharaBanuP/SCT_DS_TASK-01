# 📊 Population Data Visualization

As part of exploratory data analysis, I visualized population trends using a dataset containing population figures for various countries from 1960 to 2024.

## ✅ Key Tasks:
Data Cleaning: Removed unnecessary columns, stripped whitespaces, and ensured population columns were in numeric format.

Categorical Variable Visualization:
Created a bar chart to display the top 5 most populous countries in a selected year (e.g., 2020).

Continuous Variable Visualization:
Generated a histogram to show the distribution of population values across countries for a selected year.

## 📌 Tools Used:

Python

Pandas for data wrangling

Seaborn and Matplotlib for visualization

These visualizations help identify population distribution patterns and compare population sizes across countries in a given year.


### ⚙️ Data Cleaning Note

While loading the World Bank population data CSV, a parser error occurred due to extra metadata rows at the top of the file:

ParserError: Error tokenizing data. C error: Expected 3 fields in line 5, saw 70

✅ How it was resolved:
The dataset contains 4 lines of metadata before the actual column headers.

In Python, this was fixed using skiprows=4 while reading the CSV:


pd.read_csv("API_SP.POP.TOTL_DS2_en_csv_v2_71683.csv", skiprows=4)
