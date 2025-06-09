# Nashville Housing Data Cleaning Project

## Overview

This project is dedicated to cleaning and preparing the Nashville housing dataset using SQL. The objective is to enhance data quality and ensure consistency for accurate analysis of the Nashville housing market.

## Table of Contents

- [Project Description](#project-description)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Data Cleaning Steps](#data-cleaning-steps)
- [Contributing](#contributing)
- [License](#license)

## Project Description

The Nashville Housing Data Cleaning project utilizes SQL to preprocess raw housing data. The focus is on managing missing values, correcting data types, and eliminating duplicates to prepare the dataset for further analysis and reporting.

## Dataset

The dataset contains information on various housing listings in Nashville, including attributes such as:

- Price
- Square footage
- Number of bedrooms and bathrooms
- Location
- Year built

The raw data is stored in a SQL database for efficient querying and manipulation.

## Technologies Used

- SQL (MySQL)
- MySQL Workbench
- Data Visualization Tools (e.g., Tableau, Power BI)

## Installation

To set up the project locally, follow these steps:

**Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/nashville-housing-data-cleaning.git
   cd nashville-housing-data-cleaning


-- Remove duplicates
DELETE FROM housing_listings
WHERE id NOT IN (
    SELECT MIN(id)
    FROM housing_listings
    GROUP BY price, square_footage, bedrooms, bathrooms, location, year_built
);


## Data Cleaning Steps

- Loading Data: Import the dataset into the SQL database.
- Handling Missing Values: Use SQL queries to identify and address NULL values.
- Correcting Data Types: Ensure that columns have appropriate data types (e.g., converting strings to dates).
- Removing Duplicates: Identify and delete duplicate records based on key attributes.
- Outlier Detection: Use SQL queries to find and handle outliers in numerical fields.
- Final Data Export: Export the cleaned dataset or create views for reporting.
