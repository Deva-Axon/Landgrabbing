Land Grabbing Data Analysis Project
Overview
This project focuses on analyzing land acquisition (land grabbing) data, including the size of land (in hectares) acquired by various companies (landgrabbers) in different countries and over time. The data is processed, cleaned, and visualized using R.
Project Contents
1. Data Files:
•	grain.xlsx: Contains two sheets with data on land acquisition. Columns include country (landgrabbed), company (landgrabber), hectares acquired, year, projected investment, and other details.
2. R Scripts:
•	Data Cleaning and Transformation:
o	Standardizes country names.
o	Removes rows with missing or invalid data (e.g., empty hectares, invalid years).
o	Converts years to a consistent numeric format.
o	Cleans the "Projected investment" column by removing non-numeric characters and adjusting for terms like "billion."
o	Filters data by year, removing rows where the year is greater than 2017.
•	Data Visualization:
o	Creates line charts for:
	Country vs. Total Hectares
	Year vs. Total Hectares
Dependencies
•	readxl: For reading Excel files.
•	dplyr: For data manipulation.
•	ggplot2: For data visualization.
Usage
1. Data Cleaning and Preprocessing
The script performs the following operations:
•	Standardizing Country Names:
o	Replaces abbreviations like "AUS" with "Australia", "Arg" with "Argentina", and "RUS" with "Russia."
•	Handling Projected Investment:
o	Removes currency symbols (e.g., "US$") and handles terms like "billion" by multiplying the number by 1,000.
•	Year Adjustments:
o	Converts 0 to 2000 and 17 to 2017.
o	Filters out years beyond 2017.
•	Removing Invalid Rows:
o	Removes rows with missing or invalid "Hectares."
o	Removes rows where the "Base" or other critical columns contain invalid values (e.g., "---").
2. Data Visualization
The project generates several visualizations to help understand land acquisition trends:
•	Country vs. Total Hectares: Displays total hectares acquired in each country.
•	Year vs. Total Hectares: Presents land acquisition trends over time, up to the year 2017.

