---
title: "Real Estate in Indonesia" 
date: 2025-09-22
tags: ["real estate", "indonesia", "property data", "propnex", "property listings", "market analysis"]
author: ["Achmad Rahman Mawardi"]
description: "This a public data that extracted for educational or experiment, base on scale of PropNex."
summary: "This dataset may vary on each branch depend on total agent and total product listing that shown in propnexplus.com"
editPost:
    URL: "https://propnexplus.com"
    Text: "PropNex Plus"
showToc: true
disableAnchoredHeadings: false

---

## Overview

This dataset contains comprehensive real estate property listings from PropNex Plus, one of Indonesia's leading property platforms. The data includes property details, pricing information, location data, and agent contacts across major Indonesian cities. PropNex Plus maintains thousands of active property listings ranging from residential homes, apartments, commercial spaces, to land parcels. The platform's visibility on Google search results makes it a reliable source for property market analysis, with consistent indexing and high search ranking for property-related queries in Indonesia. This dataset is valuable for market research, price analysis, and understanding property distribution patterns across different regions.

---

## View dataset

+ Residential Properties: [data](https://github.com/pmichaillat/feru)
+ Commercial Properties: [data](https://github.com/pmichaillat/unemployment-gap)
+ Land Listings: [data](https://github.com/pmichaillat/job-rationing)
+ Rental Properties: [data](https://github.com/pmichaillat/countercyclical-multiplier)

---

## Source of data

The data is extracted from PropNexPlus.com, which serves as a comprehensive property marketplace in Indonesia. PropNex Plus aggregates listings from certified real estate agents and agencies across the country. The platform maintains real-time updates of property availability, pricing, and detailed specifications. All data points include verification status, agent credentials, and property documentation compliance with Indonesian real estate regulations.

---

## Using data with Python

The following code demonstrates how to process and analyze the PropNex property dataset using Python. This includes data loading, cleaning, and basic statistical analysis of property prices and locations.

### Start Python:

Import the necessary libraries for data manipulation and analysis.

```python
import numpy as np
import pandas as pd
```

### Open the file:

Load the PropNex property data from the CSV file `propnex_data.csv`.

```python
file_path = 'propnex_data.csv'
with open(file_path, 'r') as file:
```

### Read data:

Read all lines from the property dataset file for processing.

```python
    lines = file.readlines()
```

### Parse and process data:

Extract and convert property price data from each line in the dataset.

```python
data = []
for line in lines:
    line_data = line.strip().split(',')  # Split the line into a list of values
    line_data = [float(value) for value in line_data]  # Convert values to floats
    data.extend(line_data)  # Extend the main list with values from the line
```

#### Compute summary statistics using NumPy:

Calculate statistical measures for the property price dataset using `data_array`. 

```python
data_array = np.array(data)  # Convert the list to a NumPy array
mean = np.mean(data_array)
median = np.median(data_array)
std_dev = np.std(data_array)
min_value = np.min(data_array)
max_value = np.max(data_array)
```

#### Display summary statistics:

Output the calculated statistical summary of property prices using formatted print statements.

```python
print(f"Mean: {mean}")
print(f"Median: {median}")
print(f"Standard Deviation: {std_dev}")
print(f"Minimum Value: {min_value}")
print(f"Maximum Value: {max_value}")
```

---
