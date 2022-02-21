# Movies-ETL

## Project Overview

The purpose of this analysis is to use the Extract, Transform, and Load process in order to make a database using cleaned movie data from Wikipedia, Kaggle, and ratings. We extracted the data from their respective files, transform the datasets through cleaning rows, formatting datatypes, joining data, and then loading the cleaned dataset in to a SQL database.

## Overview

The goal of the analysis is to create a pipline that extracts, transforms and loads the data. The analysis consisted of four parts. Each step built upon extracting data and function testing, through transforming and cleaning the data. The entire ETL process for this analysis can be executed throught the ETL_create_database.ipynb (jupyter notebook file). In order to get to that jupyter notebook file the ELT process was broken down into 3 other jupyter notebook files:

### ETL_function_test.ipynb
- extract and read data from the JSON and CSV files.
- transform data into Pandas data frames
- extracting the JSON file requires loading in the file first and then transforming it into a data frame

### ETL_clean_wiki_movies.ipynb
- building of data done in the previous jupyter notebook file to merge the Wikipedia data with the Kaggle metadata
- extracting the IMDb IDs using regular expression string and dropping duplicates

### ETL_clean_kaggle_data.ipynb
- extract and transform the Kaggle metadata and MovieLens rating data. Converting the transformed data into seperate DataFrames
- then merge the Kaggle Metadata DataFrame with the Wikipedia movies DataFrame to create NEW DataFrame
- then merge the MoviesLens rating data DataFrame with the NEW DataFrame to create the NEXT DataFrame

### ETL_create_database.ipynb
- add the NEW DataFrame and MovieLens rating CSV data to a SQL database
