This project focuses on data cleaning and exploratory analysis of AQI data. The dataset includes pollutants like PM2.5, PM10, NO2, CO, and their impact on air quality.

Objectives
1.Load and explore the dataset to understand its structure.
2. Identify and handle missing values and duplicate records.
3. Perform exploratory data analysis (EDA) to gain insights.
4. Visualise AQI distribution using histograms.

 Steps Performed
1. Data Loading & Exploration
Used Pandas to read the dataset (air quality data.csv) and inspect the first few rows (df.head()).
Checked dataset shape (df.shape), column names, and data types (df.info()).
Analysed missing values and duplicate entries (df.isnull().sum(), df.duplicated().sum()).
2. Data Cleaning & Preprocessing
Handled missing values: Dropped rows where AQI was missing (df.dropna(subset=['AQI'])).
Removed duplicate records to ensure data consistency.
Converted categorical data (e.g., city names) into numerical form using Label Encoding.
3.  Exploratory Data Analysis (EDA)
Visualized AQI distribution using a histogram to observe pollution levels.
Identified correlations between AQI and pollutants using correlation heatmaps.
Sorted features by their impact on AQI using df.corr()['AQI'].sort_values().

Technologies Used
->Python, Pandas, NumPy – Data manipulation and analysis.
-> Matplotlib, Seaborn – Data visualization.
-> Scikit-learn – Data preprocessing (Label Encoding).
