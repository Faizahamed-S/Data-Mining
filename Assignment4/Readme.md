# Q1. D3.js Visualizations for Chickenpox Data in Hungary

Visualizing chickenpox cases across different regions in Hungary using D3.js.

## Overview

This repository provides various interactive D3.js visualizations for chickenpox cases in Hungary. Through a combination of charts and maps, the dataset's intricacies come to life, offering insights into the spread and concentration of cases across regions and over time.

## Features

- **Stacked Area Chart**: Visualize chickenpox cases over time for each region. The stacking allows for easy comparison between regions and highlights trends in case volume.
- **Mock Choropleth Map**: A representational map that shades regions based on the total number of chickenpox cases. Note: This is a placeholder visualization pending actual GeoJSON data for Hungary's regions.
- **Multi-Line Chart with Focus+Context**: A detailed view of chickenpox cases across multiple regions over time. The main chart provides a zoomed-in view of a specific timeframe, while a smaller chart below offers the entire timeline for context.

# Q2. # EDA Using sweetviz
Sweetviz is an open-source Python library that generates beautiful, high-density visualizations to kickstart the exploratory data analysis (EDA) process with just a couple of lines of code. The output is an HTML report that provides a concise overview of the dataset, comparing distributions, correlations, missing values, and more.
y key visualizations or plots.

# Q3. Apache Beam Data Processing Pipeline

## Overview

This document outlines the process of creating a data processing pipeline using Apache Beam. The pipeline reads weekly counts of chickenpox cases from a CSV file, processes the data to calculate monthly totals for each region, and writes the results to an output file.

## Steps Involved:

1. **Data Loading**: Loaded the provided `hungary_chickenpox.csv` file and inspected its structure.
2. **Beam Pipeline Components**:
   - **ParDo Transformation**: Applied an element-wise operation to parse each row and extract the date and case counts.
   - **Windowing**: Segmented the data into monthly windows.
   - **Triggers**: Defined a trigger to emit early results after processing a certain number of elements.
   - **Composite Transform**: Encapsulated the parsing, windowing, and aggregation steps into a composite transform.
   - **IO**: Read data from the CSV and wrote the processed results to an output file.
3. **Pipeline Execution**: Created and executed the Beam pipeline.

