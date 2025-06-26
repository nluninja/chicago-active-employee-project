# Chicago Active employees dataset Study

Explanation and Key Steps:

* Import Libraries: Standard data science stack.

* Load Data: Reads the CSV. Includes a try-except for FileNotFoundError.

* Initial Data Exploration:

 * df.info(): Data types, non-null counts.

 * df.head(): First few rows.

 * df.describe(): Statistical summary for numerical and object columns.

 * df.isnull().sum(): Counts missing values per column.
* Data Cleaning and Preprocessing:
 * Column Names: Standardized to lowercase with underscores.
 * annual_salary: This is crucial. It's often an object type due to $ and commas. It's converted to a float. If not present, an attempt is made to calculate it from hourly_rate and typical_hours.

* Drop NaNs/Zeros: Rows with no valid entries annual_salary are dropped as it's central to the analysis.

* EDA - Visualizations:
 * Salary Distribution: Histogram and Boxplot to see its spread, skewness, and outliers.
 * Categorical Distributions: Countplots for full_or_part-time, salary_or_hourly.
  * Top Departments: Bar chart of departments with the most employees.
  * Salary by Employment Type/Department: Boxplots to see how salary varies across these categories.

* Feature Engineering:
** For Clustering:
*** Features: annual_salary and sex_encoded are selected.
*** Scaling: StandardScaler is used because K-Means is distance-based.

* Clustering (K-Means):
** Optimal K: Elbow Method (inertia vs. K) and Silhouette Score are used to help choose the number of clusters (k).

* Model Training: K-Means is fitted with the chosen k.
  * Cluster Assignment: Cluster labels are added back to the DataFrame.

Analysis: Mean annual_salary and sex_encoded are calculated for each cluster.

Visualization: A scatter plot (if 2D) or strip/violin plot (if 1D) shows the clusters.
