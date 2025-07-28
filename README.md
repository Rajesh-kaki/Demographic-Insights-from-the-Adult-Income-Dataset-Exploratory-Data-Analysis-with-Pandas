# Exploratory Data Analysis on the Adult Income Dataset
This project performs a comprehensive Exploratory Data Analysis (EDA) on the Adult Income dataset. The goal is to understand the structure, distributions, relationships, and scaling needs of demographic variables related to predicting income levels.

🎯 Objective
To explore the dataset and prepare it for machine learning by:

Identifying data quality issues

Understanding feature distributions

Visualizing patterns between demographics and income

Standardizing numerical features

📁 Dataset Overview
File Used: adult_with_headers.csv

Each row represents a census record of an individual

Key features include:

age, workclass, education, marital-status

occupation, relationship, race, sex, hours-per-week, income

🔍 EDA Process Breakdown
1. Initial Data Inspection
Loaded data using pandas

Used .head(), .info(), and .describe() to inspect data shape, types, and summary statistics

Verified presence of null values and inconsistencies in categorical values (e.g., missing values as '?')

2. Data Cleaning
Replaced ambiguous entries like ' ?' with NaN and dropped/handled missing values

Removed whitespace in column entries to avoid mismatches

Converted categorical columns to lowercase for uniformity

3. Visualization of Feature Distributions
Plotted histograms and count plots using matplotlib and seaborn for:

Age distribution

Workclass and occupation frequencies

Gender vs. income breakdown

Used boxplots to visualize numerical features like hours-per-week and education-num grouped by income

Created correlation heatmaps to explore relationships between numerical columns

4. Encoding and Standardization
Applied Label Encoding to convert binary categorical columns like sex and income

Used One-Hot Encoding for multi-class categorical features such as workclass and education

Scaled numerical features (age, hours-per-week, fnlwgt, education-num) using StandardScaler to normalize their distribution for modeling

5. Feature Importance and Group Analysis
Grouped data by income and visualized average differences in:

Education level

Work hours

Age

Analyzed combinations like education vs. income, marital-status vs. income

🧠 Key Learnings
Income disparity is visible across features like education, occupation, and gender

Several features were skewed and required transformation or standardization

Correlation among some numerical variables was weak, supporting use of categorical predictors

🛠️ Libraries Used
pandas, numpy – Data handling and computation

matplotlib.pyplot, seaborn – Visualization

sklearn.preprocessing – LabelEncoder, StandardScaler

sklearn.model_selection – For next steps in modeling (optional)

📂 Files Included
EDA2.ipynb — Full notebook including EDA, cleaning, encoding, visualization, and scaling

adult_with_headers.csv — Raw dataset used for analysis

