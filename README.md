# Property Data Analysis

This project focuses on analysis of rental properties in Barcelona in Python. The data was obtained by web scraping of idealista.com on 22.02.2025, by a Python script, using the Beautiful Soup library.

## Resources

In order to use the Beautiful Soup script provided, you need to install requests, a library for making HTTP requests, as well as the Beautiful Soup, a web-scraping library.

```bash
pip install requests
```

```bash
pip install beautifulsoup4
```

## Data Acquisition

The file Web_scraping-Property_data_analysis contains the script used to obtain the data. The code itinerates through all the result pages of rental apartments in Barcelona and accesses each listing page to extract the data. The data obtained are:
- Title of the listing
- Price
- Neighbourhood
- Type of person who placed the listing: a real estate agency or a private individual
- Number of rooms
- Square meters
- Location in the building (interior/exterior)
- Floor number
- Lift (yes or no)
- Garage (yes or no)

The data is saved to a CSV file: Data/Property_data_idealista_20-02-2025.csv. 4579 entries were scraped.

## Data cleaning and analysis

Details of all the operations performed can be found in the Jupyter Notebook file Notebooks/2_Data_cleaning_and_analysis.ipynb.

The data is formatted to handle missing values, a new column is created (price per square meter) and outliers are removed. A statistical analysis is performed, to identify the distribution of the values, such as mean, median and mode. Univariate and bivariate analysis is performed and plotted, to visualize the distribution. The analysis of the data gives insights into the distribution of apartment prices, prices per square meter and apartment sizes in each neighborhood.

## Final CSV file

Cleaned data is saved to another CSV file: Data/Property_data_cleaned.csv.

## Python packages used

- **Data scraping**: Requests, Beautiful Soup
- **Data manipulation**: Numpy, Pandas, Scipy
- **Data visualization**: Matplotlib, Seaborn
