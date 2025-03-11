# Hawaii Climate Analysis

## Project Overview
This project analyzes climate data from Hawaii using an SQLite database. The analysis focuses on retrieving temperature and precipitation data, identifying the most active weather stations, and visualizing key weather trends using Python and SQLAlchemy.

## Technologies Used
- Python
- SQLAlchemy (for database queries and ORM)
- Pandas (for data manipulation)
- Matplotlib (for data visualization)
- SQLite (database storage)

## Data Source
The data is stored in `hawaii.sqlite`, which contains two primary tables:
1. `Measurement` – Includes precipitation and temperature observations with timestamps.
2. `Station` – Contains information about the weather stations.

## Steps and Implementation

### 1. Database Connection and Reflection
- Established a connection to `hawaii.sqlite`.
- Reflected the database schema using SQLAlchemy's `automap_base()`.
- Retrieved references to the `Measurement` and `Station` tables.

### 2. Finding the Most Recent Date
- Queried the database to find the most recent date in the dataset.
- Calculated the date one year prior to this latest date to set a timeframe for analysis.

### 3. Precipitation Data Analysis
- Queried the last 12 months of precipitation data.
- Stored the data in a Pandas DataFrame.
- Sorted the data by date and plotted a time-series chart of precipitation.
- Calculated summary statistics for precipitation data using `.describe()`.

### 4. Identifying the Most Active Weather Stations
- Queried the database to count the number of observations per station.
- Listed stations in descending order based on observation count.
- Identified the most active station for further analysis.

### 5. Temperature Data Analysis for the Most Active Station
- Queried temperature observations for the most active station over the last 12 months.
- Calculated the minimum, maximum, and average temperatures for this station.
- Plotted a histogram to visualize the temperature distribution.

## Results and Visualizations
- A time-series plot of precipitation over the last 12 months.
- Summary statistics of precipitation levels.
- A list of the most active weather stations ranked by observation count.
- The lowest, highest, and average temperature recorded at the most active station.
- A histogram showing the temperature distribution for the most active station.

## How to Run the Code
1. Ensure you have Python installed.
2. Install the required dependencies:
   ```bash
   pip install sqlalchemy pandas matplotlib
   ```
3. Run the script in a Python environment (e.g., Jupyter Notebook or a Python script).
4. Ensure that `hawaii.sqlite` is located in the `Resources/` directory.

## Conclusion
This analysis provides insights into Hawaii's climate trends by leveraging SQLAlchemy and data visualization tools. The project demonstrates how to work with SQL databases in Python, extract meaningful insights, and visualize climate data effectively.

