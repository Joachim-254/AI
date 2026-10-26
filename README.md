ARetail Sales Data
This repository contains two Excel datasets with retail sales records
from branches in Kenya. The files can be used for basic data cleaning,
exploratory data analysis, reporting, and comparison of product activity
across branches and dates.
Repository Contents
---
File                         Description                    Records Columns
---
`cleanshelf_sales(1).xlsx`   CleanShelf sales                     7 5
records,  
including unit  
price and  
quantity sold
`naivas_sales.xlsx`          Naivas sales                         8 3
activity by  
date, branch,  
and product
Each workbook contains a single worksheet named `Sheet1`.
Dataset Details
CleanShelf sales
The CleanShelf workbook contains the following fields:
Column       Description
---
`Branch`     Branch/location where the sale was recorded
`Date`       Date of the sales record
`Product`    Product name and package size
`Price`      Recorded product price
`Quantity`   Quantity sold
The supplied records are dated 7 February 2026 and cover Nairobi,
Kisumu, Mombasa, Machakos, Meru, Embu, and Nyeri.
Naivas sales
The Naivas workbook contains the following fields:
Column      Description
---
`Date`      Date of the sales record
`Branch`    Branch/location associated with the record
`Product`   Product recorded
The supplied records span February to June 2026 and include Nairobi,
Kisumu, Mombasa, and Nakuru.
Getting Started
Requirements
Python 3.9 or later
`pandas`
`openpyxl`
Install the dependencies:
``` bash
pip install pandas openpyxl
```
Load the workbooks
``` python
import pandas as pd

cleanshelf = pd.read_excel("cleanshelf_sales(1).xlsx")
naivas = pd.read_excel("naivas_sales.xlsx")

print(cleanshelf.head())
print(naivas.head())
```
Possible Uses
Explore product activity across branches.
Summarize sales quantities and prices in the CleanShelf dataset.
Compare recorded product activity by branch and date.
Create charts, pivot tables, and summary reports.
Practice data cleaning and exploratory data analysis with Excel data
in Python.
Data Notes and Limitations
The files contain small sample datasets (7 CleanShelf rows and 8
Naivas rows).
The CleanShelf dataset includes both `Price` and `Quantity`, while
the Naivas dataset does not include price or quantity fields. Direct
revenue or sales-volume comparisons between the two datasets are
therefore not supported by the supplied columns.
The CleanShelf column names `Product` and `Quantity` contain
trailing spaces. Consider normalizing column names before analysis.
Currency is not explicitly identified in the workbook, so do not
assume a currency without confirming the source.
The data is presented as supplied; completeness, accuracy, and
whether the records represent all sales have not been independently
verified.
Suggested Data Preparation
You can standardize column names before analysis:
``` python
cleanshelf.columns = cleanshelf.columns.str.strip()
naivas.columns = naivas.columns.str.strip()
```
License and Attribution
No license or data attribution information was included with the
supplied workbooks. Add the appropriate license and source attribution
before redistributing this repository.
