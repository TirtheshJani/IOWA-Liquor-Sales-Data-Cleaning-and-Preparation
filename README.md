# IOWA-Liquor-Sales-Data-Cleaning-and-Preparation
# Stage 1: Data Cleaning
## Overview:
This phase is a comprehensive data cleaning process for the Iowa Liquor Sales dataset, covering a period from January 1, 2012, to April 1, 2023. The dataset provides insights into spirits purchased by Iowa Class "E" liquor license holders, detailing the products and their purchase dates.

### Detailed Steps:
Checking and Removing Null/Missing Values:

### Key columns with missing values include:
**Address**
- City
- Zip Code
- Store Location
- County Number
- County
- Category
- Category Name
- Vendor Number
- Vendor Name
- State Bottle Cost
- State Bottle Retail
- Sale (Dollars)
- Mapping Missing Values

A mapping is established to fill in missing data for columns: 'Store Location', 'Zip Code', 'City', and 'County Number'. A new DataFrame "store_locs_withna" is created, dropping rows with missing values and setting a unique index based on the "Store Number" column.
Filling Missing Values with Existing Mappings:

The missing values in the "Store Location," "Zip Code," "City," and "County Number" columns of the main dataset are filled using the established mapping. A lambda function maps each "Store Number" to its corresponding value in the new DataFrame, filling in the blanks.
Cleaning and Reclassifying "Category Name":

The "Category Name" column is cleaned and reclassified. The text values are converted to uppercase, and specific data is replaced based on predetermined criteria. New classifications include categories such as "WHISKY," "VODKA," "RUM," and more.
I carried out the following Steps:
1. Importing necessary libraries and modules.
2. Setting up plotting configurations.
3. Locating a mapping for filling in missing data.
4. Using the existing mapping to fill in missing values.
5. Cleaning up and re-categorizing the 'Category' column.
6. Removing outliers for numerical columns.
7. Extracting longitude and latitude from the 'Store Location' column.
8. Dropping redundant columns.
9. Dropping some rare NA items after being filled with existing mappings.
Now, I'll move on to the second notebook, "Data Cleaning, Preparation, and Dimensionality Reduction .ipynb", to extract detailed steps and processes involved in this stage.

Let's delve deeper into the second stage, "Data Cleaning, Preparation, and Dimensionality Reduction", based on the extracted details:

# Stage 2: Data Cleaning, Preparation, and Dimensionality Reduction
## Overview:
This notebook is an extended version of the data cleaning stage 1 and introduces preparation and dimensionality reduction techniques. The goal is to transform the dataset to be more suitable for analysis and modeling.

The dataset comprises over 26 million rows and 24 columns.
## Exploration:
An exploratory phase to get familiar with the dataset.
Checking and Removing Null/Missing Values:
## Key columns with missing values similar to Stage 1 include:
- Address
- City
- Zip Code
- Store Location
- County Number
- County
- Category
- Category Name
- Vendor Number
- Vendor Name
- State Bottle Cost
- State Bottle Retail
- Sale (Dollars)
- Mapping Missing Values

Similar to the first notebook, a mapping is established to fill in missing data for columns like 'Store Location', 'Zip Code', 'City', and 'County Number'. A new DataFrame "store_locs_withna" is created, which drops rows with missing values and sets a unique index based on the "Store Number" column.

## Following is the summary of steps:
1. Set up plotting configurations.
2. Locate a mapping for filling in missing data.
3. Use the existing mapping to fill in missing values.
4. Clean up and re-categorize the 'Category' column.
5. Remove outliers for numerical columns.
6. Extract longitude and latitude from the 'Store Location' column for visualization.
7. Drop redundant columns.

# Stage 3: Final Data Preparation
## Overview:
This stage focuses on the final stages of data preparation, leading up to the modeling phase. The specific steps and transformations applied to the dataset prepare it for predictive modeling or other advanced analytics tasks.

Here is the summary of everything in the notebook: 
1. Plotting configurations set up for consistent visualization outputs.
2. Exploring the relationship between 'Volume Sold' and 'Time' to understand sales trends over time.
3. TensorFlow Setup
4. One-Hot Encoding applied, converting categorical variables into a format that can be provided to machine learning algorithms to improve predictions.
5. The target variable 'Sale (Dollars)' is separated from the main dataset, indicating a supervised learning task where the goal might be to predict sales amounts.
6. Setting a random seed to ensure reproducibility across runs.
7. Dropping unnecessary columns like 'City' from the feature matrix.


Combining details from all three stages provides a comprehensive view of the data processing pipeline. The steps taken in each notebook ensure that the Iowa Liquor Sales dataset is cleaned, transformed, and prepared for subsequent analysis and modeling.
