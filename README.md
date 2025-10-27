# AirBnB Listing Analysis - Paris

## Description

This project analyzes Airbnb listing data for Paris using Python libraries within a Google Colab environment. The primary goal is to explore the dataset and investigate the potential impact of regulations introduced around 2015 on the influx of new hosts and the average listing prices in the city.

## Data Source

The analysis uses a dataset named `Listings.csv`, which contains information about Airbnb listings. Key columns utilized in this notebook include:
* `host_since`: The date the host first listed on Airbnb.
* `neighbourhood`: The neighbourhood of the listing in Paris.
* `city`: The city of the listing (filtered to "Paris").
* `accommodates`: The number of guests the listing can accommodate.
* `price`: The nightly price of the listing.

## Objectives & Analysis Steps

The notebook is structured around the following objectives:

1.  **Data Loading and Preprocessing:**
    * Import the `Listings.csv` file using pandas.
    * Cast the `host_since` column to the datetime format.
    * Filter the dataset to include only listings located in "Paris".
    * Select and keep relevant columns: `host_since`, `neighbourhood`, `city`, `accommodates`, and `price`.

2.  **Data Quality Assurance (QA) & Exploration:**
    * Check for missing values in the filtered Paris dataset.
    * Calculate descriptive statistics (min, max, average) for numerical fields (`accommodates`, `price`).
    * Investigate rows where `price` or `accommodates` might be zero.

3.  **Grouped Analysis:**
    * Calculate the average listing price grouped by `neighbourhood` (`paris_listings_neighbourhood`).
    * Identify the most expensive neighborhood and analyze the average price based on the number of `accommodates` within that neighborhood (`paris_listings_accomodates`).
    * Analyze trends over time by grouping data by the year of `host_since` to see the count of new hosts and average price per year (`paris_listings_over_time`).

4.  **Visualization & Insights:**
    * Create bar charts to visualize average prices by neighborhood and by accommodation capacity (in the most expensive neighborhood).
    * Create line charts to show the trend of new hosts joining over time and the trend of average prices over time.
    * Generate a dual-axis line chart comparing the count of new hosts and the average price over time to visually assess the potential impact of the 2015 regulations.

## Potential Findings

The analysis, particularly the time-series visualizations, suggests a potential correlation between the introduction of regulations around 2015 and:
* A decrease or stabilization in the rate of new hosts joining the platform in Paris.
* An increase in the average listing prices.

*(Note: Further statistical analysis would be needed to confirm causation.)*

## Requirements

This project primarily uses the following Python libraries:
* `pandas` for data manipulation and analysis.
* `numpy` for numerical operations.
* `matplotlib.pyplot` for creating visualizations.

The analysis is performed within a Google Colab environment (e.g., Google Colab, Jupyter Lab/Notebook).

## Usage

1.  Ensure you have Python and the required libraries (`pandas`, `numpy`, `matplotlib`) installed.
2.  Obtain the `Listings.csv` dataset.
3.  Place the `AirBnB_Listing_Analysis.ipynb` notebook and the `Listings.csv` file in an appropriate directory structure.
4.  **Important:** Update the file path in the notebook cell where the CSV is loaded (`pd.read_csv(...)`) to point correctly to your `Listings.csv` file location. If using Google Colab, you might need to upload the CSV or mount your Google Drive as shown in the initial cells.
5.  Run the cells sequentially in the Jupyter Notebook to perform the analysis and generate visualizations.
