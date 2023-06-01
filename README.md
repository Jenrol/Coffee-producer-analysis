# Coffee-producer-analysis
Author: Abosede
Date: 04/05/2022

## Introduction
This project aims to analyze data on coffee producers in three regions: Africa and the Middle East, Americas, and Asia and the Pacific. The dataset includes information on conventional production, organic production, and the area of land covered by each producer. The code provided performs various analyses, including outlier detection, aggregation of variables by region, and visualization using stacked bar charts.

## Getting Started
To run the code in this project,The following packages are required:

ggplot2
ggthemes
dplyr
## You can install the packages using the following code:

install.packages("ggplot2")
install.packages("ggthemes")
install.packages("dplyr")

## After installing the packages, load them into the R environment using the following code:
library(ggplot2)
library(ggthemes)
library(dplyr)
## Data Import
 the dataset is available in a CSV file named "Producerdata.csv". The code reads the CSV file into the variable "mydata" using the read.csv() function. You may need to modify the file path in the code to match the location of the CSV file on your system.

## Data Preprocessing
The code performs some data preprocessing tasks before the analysis. It converts certain variables from character format to numeric format using the as.numeric(as.character()) function.

## Outlier Detection
The code uses box plots and the boxplot.stats() function to detect outliers in the "Production.conventional" variable. Outliers are values that significantly differ from the rest of the data. The code identifies the outliers and lists the corresponding rows in the dataset.

## Aggregation by Region
The code performs aggregation of variables by region using the summarise() function from the dplyr package. It calculates the sum of the variables "Area.total," "Area.conventional," "Area.organic," "Production.conventional," "Production.Organic," and "Production.total" for each region. The results are stored in the "Aggregate" dataframe.

## Visualization
The code visualizes the aggregated data using stacked bar charts. It uses the ggplot2 package to create the plots.

## Eliminating Outliers
The code provides an optional step to eliminate outliers from the dataset. It calculates the interquartile range (IQR) and removes values that fall outside the range [Q1 - 1.5 * IQR, Q3 + 1.5 * IQR] for the "Production.conventional" variable. The resulting dataset, without outliers, is stored in the "eliminated" dataframe. Aggregation is performed on this updated dataset, and the results are stored in the "Aggregateoutlier" dataframe.

## Conclusion
This project offers an initial analysis of coffee producer data, including outlier detection, aggregation by region, and visualization.





