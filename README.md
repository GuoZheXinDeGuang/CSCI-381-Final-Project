# Bike-Sharing Demand Analysis
This is done by Yunjing Yao, Zihan Liu and Sianna Fang

This repository contains code to analyze bike-sharing demand across multiple cities, with a focus on understanding the impact of weather conditions, time of day, and city-specific trends.

## Installation

To get started with this project, follow these steps:

1. **Clone the repository**:
    \```bash
    git clone [https://github.com/GuoZheXinDeGuang/CSCI-381-Final-Project.git]
    cd CSCI-381-Final-Project
    \```

2. **Install the required dependencies**:
    \```bash
    pip install -r requirements.txt
    \```

## Usage

1. **Load the Jupyter Notebook**:
   - Open the `Final_Group_Project.ipynb` file in Jupyter Notebook or Jupyter Lab.
   - Run the cells in sequence to execute the analysis.

2. **Run the analysis**:
   - The notebook includes steps for data loading, preprocessing, exploratory data analysis (EDA), weather impact analysis, and visualization of results.

## Key Functions and Code Snippets

\```python
# Data Preprocessing
data.fillna(method='ffill', inplace=True)
data['hour'] = pd.to_datetime(data['timestamp']).dt.hour

# Exploratory Data Analysis (EDA)
plt.figure(figsize=(10, 6))
sns.histplot(data['hour'], kde=False, bins=24)
plt.title('Distribution of Bike Rentals by Hour')
plt.xlabel('Hour of the Day')
plt.ylabel('Number of Rentals')
plt.show()

# Weather Impact Analysis
plt.figure(figsize=(10, 6))
sns.scatterplot(x='temperature', y='count', data=data)
plt.title('Bike Rentals vs. Temperature')
plt.xlabel('Temperature (°C)')
plt.ylabel('Number of Rentals')
plt.show()

# City-Specific Analysis
city_grouped = data.groupby(['city', 'hour'])['count'].sum().reset_index()
\```

## Results and Visualizations

The results of the analysis are presented in various visualizations such as histograms, scatter plots, and bar charts, which help illustrate the key findings related to weather impacts, temporal demand patterns, and city-specific trends.
.
