Project Workflow

1. Data Cleaning
Feature Selection: Dropped columns that didn't significantly impact price (e.g.,area_type,availability,society,balcony).
Handling Null Values: Removed rows with missing values as they represented a very small percentage of the total dataset.

2. Feature Engineering
BHK Creation: Extracted the number of bedrooms from the size column and converted it to an integer.
Total Square Feet Normalization: Handled the total_sqft column by:
Converting single values to floats.
Taking the average of range values (e.g., '2100 - 2850').
Removing non-standard units (e.g., 'Sq. Meter').
Price per Sqft: Created a new feature price_per_sqft to help identify price anomalies.

3. Dimensionality Reduction
Location Tagging: There were over 1,200 unique locations. Any location with fewer than 10 data points was tagged as 'other'. This prevents the "Curse of Dimensionality" when performing One-Hot Encoding later.

Tech Stack
Python
Pandas (Data Manipulation)
NumPy (Mathematical Operations)
Matplotlib (Data Visualization)

How to Run
Upload the bengaluru_house_prices.csv to your Google Colab environment.
Run the cells sequentially to see the data transformation.
