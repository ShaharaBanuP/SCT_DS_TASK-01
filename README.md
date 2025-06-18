SCT_DS_TASK-01
⚙️ Data Cleaning Note
While loading the World Bank population data CSV, a parser error occurred due to extra metadata rows at the top of the file:

ParserError: Error tokenizing data. C error: Expected 3 fields in line 5, saw 70

✅ How it was resolved:
The dataset contains 4 lines of metadata before the actual column headers.

In Python, this was fixed using skiprows=4 while reading the CSV:

python
Copy
Edit
pd.read_csv("API_SP.POP.TOTL_DS2_en_csv_v2_71683.csv", skiprows=4)
