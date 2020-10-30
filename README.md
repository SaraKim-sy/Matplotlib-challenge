# Matplotlib-challenge - Pymaceuticals Inc.

## Table of contents
  * [Introduction](#introduction)
  * [Observations and Insights](#insights)
  * [Study Results Report](#final-report)
    * [Summary Statistics](#summary-statistics)
    * [Bar Chart](#bar)
    * [Pie Chart](#pie)
    * [Quartiles and Outliers](#quartiles-and-outliers)
    * [Box Plot](#box)
    * [Line Plot](#line)
    * [Scatter Plot](#scatter)
    * [Correlation Coeifficient & Linear Regression Model](#correlation-regression)
  * [Technologies](#technologies)

## <a name="introduction"></a> Introduction
This project is to analyze the study of Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this repository, you will find all of the tables and figures needed for the technical report of the study and also a summary of the study results.

* Inside a Pymaceuticals folder, you will find the following:
  * A jupyter notebook file called [**pymaceuticals.ipynb**](./Pymaceuticals/pymaceuticals.ipynb), which is the main script to run for analyzing the study results.
  * A "data" folder that contains two CSV files used; one is called [**Mouse_metadata.csv**](./Pymaceuticals/data/Mouse_metadata.csv). This dataset is composed of five columns: `Mouse ID`,	`Drug Regimen`,	`Sex`,	`Age_months`,	`Weight (g)`. The other dataset is called [**Study_results.csv**](./Pymaceuticals/data/Study_results.csv). This dataset is composed of 4 columns: `Mouse ID`,	`Timepoint`,	`Tumor Volume (mm3)`, `Metastatic Sites`. I imported and merged these two datasets, and checked the data for any mouse ID with duplicate time points and removed any data associated with that mouse ID to analyze the study results using Pandas library and Jupyter Notebook, created the tables and figures needed for the report using Matplotlib, and draw observations and insights based on the data.

* The [**final report**](#final-report) includes:
  * Summary Statistics
  * Bar charts that show the number of total mice for each treatment regimen throughout the course of the study
  * Pie plots showing the distribution of female versus male mice
  * Quartiles and potential Outliers of the final tumor volume four treatment regimens
  * A box plot of the final tumor volume of each mouse across four regimens
  * A line plot of tumor volume vs. time point for a mouse treated with Capomulin
  * A scatter plot of average tumor volume vs. mouse weight for the Capomulin regimen
  * The correlation coefficient and linear regression model for mouse weight and average tumor volume for the Capomulin regimen.
   
* Inside an Images folder, you will find the charts and plots created in the report as png image files.

## <a name="insights"></a> Observations and Insights

## <a name="final-report"></a> Study Results Report
The notebook displays the whole study results analysis is available in this link: [Analysis Report](https://nbviewer.jupyter.org/github/SaraKim-sy/Pandas-challenge/blob/main/Pymaceuticals/.ipynb_checkpoints/pymaceuticals-checkpoint.ipynb)

### <a name="summary-statistics"></a> Summary Statistics
* A summary statistics table of mean, median, variance, standard deviation, and SEM of the tumor volume for each regimen.
* Were calculated by two methods, one is using grouby and summary statistical methods, the other is using the aggregation metod. 

### <a name="bar"></a> Bar Charts
* Bar charts that show the number of total mice for each treatment regimen throughout the course of the study
* Two identical charts were created using both Pandas's DataFrame.plot() and Matplotlib's pyplot
* Outcome:

![Bar Chart](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/bar_plot.png?raw=true)

### <a name="pie"></a> Pie Charts
* Pie charts showing the distribution of female versus male mice
* Two identical plots Were created using both Pandas's DataFrame.plot() and Matplotlib's pyplot
* Outcome:

![Pie Chart](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/pie_plot.png?raw=true)

### <a name="quartiles-and-outliers"></a> Quartiles and Outliers
* The final tumor volume of each mouse across four of the treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin
* The quartiles and IQR were calculated to determine potential outliers across four treatment regimens

### <a name="box"></a> Box Plot
* A box plot of the final tumor volume of each mouse across four regimens
* Highlighted any potential outliers in the plot by changing their color to red.
* Outcome:

![Box Chart](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/box_plot.png?raw=true)

  
## <a name="technologies"></a> Technologies
Project is created with:
* Python 3.8
* Jupyter Notebook
* Pandas
* Matplotlib
