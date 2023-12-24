# Lyft Driver Segmentation

## Notebook Overview

This Jupyter notebook analyzes the performance of ride-hailing drivers using real-world data from a ride-hailing service. The analysis focuses on understanding driver behavior, performance, and lifetime value, which can ultimately aid in optimizing driver strategies and improving overall service efficiency.

## Data Description

### driver_ids.csv

| Column Name        | Description                                         |
|--------------------|-----------------------------------------------------|
| driver_id          | Unique identifier for a driver                      |
| driver_onboard_date| Date on which the driver was onboarded              |

### ride_ids.csv

| Column Name        | Description                                         |
|--------------------|-----------------------------------------------------|
| driver_id          | Unique identifier for a driver                      |
| ride_id            | Unique identifier for a ride completed by the driver|
| ride_distance      | Ride distance in meters                             |
| ride_duration      | Ride duration in seconds                            |
| ride_prime_time    | Prime time applied on the ride                      |

### ride_timestamps.csv

| Column Name        | Description                           |
|--------------------|---------------------------------------|
| ride_id            | Unique identifier for a ride          |
| event              | Describes the type of event           |
| timestamp          | Time of the event                     |

### Assumptions

| Assumption          | Value  |
|---------------------|--------|
| BASE FARE           | $2.00  |
| COST PER MILE       | $1.15  |
| COST PER MINUTE     | $0.22  |
| SERVICE FEE         | $1.75  |
| MINIMUM FARE        | $5.00  |
| MAXIMUM FARE        | $400.00|

## Key Steps

1. **Data Preprocessing**: Importing necessary libraries, cleaning anomalous data entries, and loading the provided datasets.
2. **Feature Engineering**: Calculating the total ride cost formula, deriving ride events, and calculating various ride and driver-specific metrics.
3. **Driver Lifetime Value**: Estimating the driver lifetime value by projecting future rides and revenue.
4. **Exploratory Data Analysis**: Descriptive statistics, correlation analysis, and visualization of driver performance metrics.
5. **Clustering**: Grouping drivers based on their performance using KMeans clustering.

## Libraries Used

- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `yellowbrick`

## Installation

To run the notebook, make sure you have Jupyter Notebook installed. You can install the required libraries using the following command:

```bash
pip install numpy pandas seaborn matplotlib scikit-learn yellowbrick
```

## Contributing

If you want to contribute to this project, feel free to fork the repository, make your changes, and open a pull request. I appreciate your contributions!

## License

MIT
