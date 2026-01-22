# TASK-5-Reading-data-simple-cleaning-with-pandas-
Step 1: Import Dataset
I created the environment in Jupyter Notebook, imported pandas, and loaded the raw housing-data.csv file using pd.read_csv(). The dataset was successfully uploaded for analysis.

Step 2: Inspect Dataset
I previewed the dataset with .head() and checked its structure with .info(). It showed 714 rows and 2 columns (DATE, HOUSTNSA) with no missing values.

Step 3: Handle Missing Values and Duplicates
I checked for missing values using .isnull().sum() and confirmed none existed. I removed duplicates with .drop_duplicates() and verified the shape stayed (714, 2).

Step 4: Clean Missing Values
I applied proper approaches for cleaning: dropping irrelevant rows/columns with .dropna(), filling numeric values with median, and categorical values with mode. This ensured consistency in the dataset.

Step 5: Remove Duplicates with Verification
I used .drop_duplicates() again and printed the row count before and after to confirm duplicates were removed properly. The dataset remained stable after this check.

Step 6: Convert Datatypes
I converted the DATE column from string into datetime using pd.to_datetime() and ensured HOUSTNSA was float with .astype(float). This allowed correct calculations and time‑based analysis.

Step 7: Create New Columns
I created new columns to demonstrate transformation ability: extracted Year from DATE, generated HOUSTNSA_Band using pd.cut() with dynamic bins, and calculated Monthly_Growth using .diff().

Step 8: Verify Transformations
I previewed the dataset with .head() to confirm the new columns were correctly created. The bands categorized housing starts, and the growth column showed month‑to‑month changes.

Step 9: Save Cleaned Dataset
I saved the cleaned dataset using .to_csv("cleaned_housing_data.csv", index=False) and confirmed the output file was generated. The final dataset is ready for reuse and further analysis.
