# Los-Angeles-Metro-Bike-Share

The code provided is performing data interpretation, preprocessing, and statistical testing on a dataset using various Python packages. Let's break down what each section is doing and how it works:

1. Python Libraries:
The code begins by importing several Python libraries, including pandas, NumPy, Seaborn, matplotlib.pyplot, plotly.graph_objs, plotly.offline, chi2_contingency, and warnings. These libraries provide various functions and tools for data analysis, visualization, and statistical testing.

2. Matplotlib Settings:
This section sets up the default settings for Matplotlib, a plotting library in Python. It defines various parameters such as grid lines, figure size, legend location, etc., to customize the appearance of the plots generated later in the code.

3. Output settings:
This section sets options for displaying output in the code. For example, it specifies the display format for floating-point numbers, suppresses the printing of scientific notation, and sets the precision for numpy arrays.

4. Data understanding:
The code provides an overview of the dataset being analyzed. It describes the columns present in the dataset and their corresponding descriptions. It also displays the first few rows of the dataset using the pandas `read_csv` function.

5. Data preprocessing:
This section focuses on preprocessing the data before analysis. It performs various operations on the dataset, including checking for missing values, eliminating rows with missing values using `dropna`, and checking the shape of the dataset. It also summarizes the data by counting the occurrences of different categories in specific columns using `value_counts` and creating visualizations using seaborn's `countplot` and `heatmap`.

6. Data transformation:
This section involves transforming the data by modifying the data types and creating new columns based on existing columns. It converts the 'start_time' and 'end_time' columns from object data type to datetime format using the `pd.to_datetime` function. It then creates four new columns ('start_day', 'start_month', 'start_year', 'start_hour') using the `dt` accessor to extract different components (day, month, year, hour) from the 'start_time' column.

7. Statistical tests:
The code performs statistical tests on the dataset. It calculates the average duration for each passholder category using `groupby` and `mean`. It then conducts a chi-square test of independence to determine the association between two categorical variables ('start_station' and 'end_station') using `pd.crosstab` and `chi2_contingency`. Finally, it performs t-tests to compare the mean duration between different passholder types using `stats.ttest_ind`, and plots the p-values for the t-tests using Matplotlib's `bar` function.

Overall, the code provides a comprehensive analysis of the dataset, including data understanding, preprocessing, transformation, and statistical testing. It utilizes various Python libraries and functions to perform these tasks efficiently.
