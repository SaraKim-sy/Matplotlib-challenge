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
* The bar chart shows that the number of unique mice tested on each drug regimen was 24 or 25, and it seems that it was fairly distributed. 
* The pie chart shows that female versus male mice's distribution was almost similar, as female mice take up about 49.6%, and male mice take up about 50.4%. We can say that this helped the study results not to be affected by the gender of mice. 
* Seeing the outliers and a box plot, we can notice that there is a potential outlier in the final tumor volumes among the mice treated with Infubinol; therefore, we should consider it when we analyze the results. This might affect the test results analysis, but for the other 3 treat regimens, it seems that there are no potential outliers that would affect the analysis. Also, from the boxes and whiskers' location in the box plot, we can notice that the final tumor volumes of mice treated with Ramicane and Capomulin are generally smaller than the final tumor volumes of mice treated with Infubinol and Ceftamin. This may show that Ramicane and Capomulin in treating tumors can be more effective than Infubinol and Ceftamin.
* The line plot of tumor volume versus time point for s185 treated with Capomulin shows that the tumor volume decreased from 45 mm3 to about 23 mm3 by the time pass. It seems that Capomulin was very effective in treating the tumor of s185. It would be needed to see line plots of tumor volumes versus the time point of other mice treated with Caomulin as well to prove the indisputable effectiveness of Capomulin.
* Looking at the scatter plot with the linear model, we can notice a strong positive correlation between mouse weight and average tumor volume for the Capomulin regimen. The fact that the correlation coefficient was about 0.84 also proves this relationship. From this, we can assume mouse weight can significantly affect tumor volume. In other words, the heavier the mouse weight may cause a larger tumor volume. 

## <a name="final-report"></a> Study Results Report
The notebook displays the whole study results analysis is available in this link: [Analysis Report](https://nbviewer.jupyter.org/github/SaraKim-sy/Matplotlib-challenge/blob/main/Pymaceuticals/.ipynb_checkpoints/pymaceuticals-checkpoint.ipynb)

### <a name="summary-statistics"></a> Summary Statistics
* A summary statistics table of mean, median, variance, standard deviation, and SEM of the tumor volume for each regimen.
* Calculated by two methods, one uses groupby and summary statistical methods, the other uses the aggregation method.

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

![Box Plot](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/box_plot.png?raw=true)

### <a name="line"></a> Line Plot
* A line plot of tumor volume vs. time point for a mouse (s185) treated with Capomulin
* Outcome:

![Line Plot](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/line_plot.png?raw=true)

### <a name="scatter"></a> Scatter Plot
* A scatter plot of average tumor volume vs. mouse weight for the Capomulin regimen
* Outcome:

![Scatter Plot](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/scatter_plot.png?raw=true)

### <a name="correlation-regression"></a> Correlation Coeifficient & Linear Regression Model
* Calculated the correlation coefficient and linear regression model for mouse weight and average tumor volume for the Capomulin regimen
* Generated a scatter plot of Average Weight vs. Average Tumor Volume and plot the linear model on top of scatter plot
* Outcome:

![Scatter and Linear Plot](https://github.com/SaraKim-sy/Matplotlib-challenge/blob/main/Images/scatter_linear_plot.png?raw=true)
  
## <a name="technologies"></a> Technologies
Project is created with:
* Python 3.8
* Jupyter Notebook
* Pandas
* Matplotlib
