# Retail Sales Data Analysis

## Project Overview

This repository contains two Excel datasets containing retail sales records from CleanShelf and Naivas. The datasets can be used for data cleaning, exploratory data analysis (EDA), visualization, and comparison of product activity across different branches in Kenya.

The project aims to explore retail product records, understand branch-level activity, and identify useful patterns in the available data.

## Repository Contents

The repository contains the following files:

- `cleanshelf_sales(1).xlsx` – CleanShelf sales dataset.
- `naivas_sales.xlsx` – Naivas sales dataset.
- `README.md` – Project documentation.

## Dataset Description

### 1. CleanShelf Sales Dataset

The CleanShelf dataset contains 7 records with the following columns:

| Column   | Description                          |
| -------- | ------------------------------------ |
| Branch   | Location where the sale was recorded |
| Date     | Date of the sales record             |
| Product  | Name of the product sold             |
| Price    | Recorded product price               |
| Quantity | Quantity sold                        |

The dataset includes records from Nairobi, Kisumu, Mombasa, Machakos, Meru, Embu, and Nyeri.

### 2. Naivas Sales Dataset

The Naivas dataset contains 8 records with the following columns:

| Column  | Description                           |
| ------- | ------------------------------------- |
| Date    | Date of the sales record              |
| Branch  | Branch where the product was recorded |
| Product | Name of the product                   |

The dataset includes records from February to June 2026 and covers branches in Nairobi, Kisumu, Mombasa, and Nakuru.

## Technologies Used

The following tools and technologies can be used to analyze the datasets:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Microsoft Excel

## Getting Started

### Prerequisites

Ensure Python is installed on your computer.

Install the required libraries using:

```
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### Loading the Datasets

Use the following Python code to load the datasets:

```
import pandas as pd# Load CleanShelf datasetcleanshelf = pd.read_excel("cleanshelf_sales(1).xlsx")# Load Naivas datasetnaivas = pd.read_excel("naivas_sales.xlsx")# Display the first five recordsprint(cleanshelf.head())print(naivas.head())
```

## Data Cleaning

Before analysis, clean and standardize the column names:

```
cleanshelf.columns = cleanshelf.columns.str.strip()naivas.columns = naivas.columns.str.strip()
```

Check for missing values:

```
print(cleanshelf.isnull().sum())print(naivas.isnull().sum())
```

Check for duplicate records:

```
print(cleanshelf.duplicated().sum())print(naivas.duplicated().sum())
```

## Potential Analysis

The datasets can be used to perform the following analyses:

1. Branch Analysis: Examine product records across different branches.
2. Product Analysis: Identify the products appearing in the datasets.
3. Price Analysis: Explore product prices in the CleanShelf dataset.
4. Quantity Analysis: Examine quantities sold in the CleanShelf dataset.
5. Time Analysis: Explore sales records over different dates.
6. Comparative Analysis: Compare product and branch activity between CleanShelf and Naivas.

## Limitations

- The datasets contain relatively few records.
- The Naivas dataset does not include price or quantity information.
- Revenue comparisons between the two retailers cannot be performed using the supplied columns alone.
- The currency used in the CleanShelf dataset is not explicitly specified.
- The datasets may not represent the complete sales activities of the retailers.

## Expected Outcomes

The project provides an opportunity to:

- Understand retail sales data.
- Apply Python data analysis techniques.
- Identify patterns in product and branch records.
- Develop data visualization skills.
- Generate meaningful insights from structured datasets.

## Conclusion

This project uses CleanShelf and Naivas retail datasets to explore product and branch-level sales information. Through data cleaning, exploratory data analysis, and visualization, the project provides a foundation for understanding retail data and extracting useful business insights.

## License

No license was provided with the datasets. Appropriate licensing and data-source attribution should be added before public redistribution.
