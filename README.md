# Drug Therapy Animal Study

## Background Information

In this theoretical project application, I assumed the role as a data analyst for Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

In Pymaceuticals Inc. most recent animal study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. For this assessment, I generated all of the tables and figures needed for the technical report of the study, along with an overview summary of the study results at the beginning of the Jupyter Notebook.

Programming dependencies and languages used within this repository: Pandas, Matplotlib, and Jupyter Notebook.

## Data Visualization Procedure

* It is important to understand factors within a research study that may skew the results or interpretation of the data, such as duplicates within the dataset. Prior to creating any of the tables or figures for the technical report of the study, I checked the data for any mouse ID with duplicate time points and remove any data associated with that mouse ID. There was only one ID that was duplicated within the dataset (`Mouse ID g989`), and once removed the dataset was reduced by 13 entries.

* Original Dataframe:

![Original](Images/original_df.png)

* Reduced Dataframe:

![Reduced](Images/duplicate_drop_df.png)

* For an initial statstical overview, I generated a summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

  * I generated a summary statistics table using Pandas' .groupby() method:

  ![groupby](Images/groupby_summary_stats.png)

  * And recreated the same summary statistics table using Matplotlib's .aggregate() method:

  ![agg](Images/agg_summary_stats.png)

* Generate a bar plot using both Pandas's `DataFrame.plot()` and Matplotlib's `pyplot` that shows the total number of measurements taken for each treatment regimen throughout the course of the study.

  * **NOTE:** These plots should look identical.

* Generate a pie plot using both Pandas's `DataFrame.plot()` and Matplotlib's `pyplot` that shows the distribution of female or male mice in the study.

  * **NOTE:** These plots should look identical.

* Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Calculate the quartiles and IQR and quantitatively determine if there are any potential outliers across all four treatment regimens.

* Using Matplotlib, generate a box and whisker plot of the final tumor volume for all four treatment regimens and highlight any potential outliers in the plot by changing their color and style.

  **Hint**: All four box plots should be within the same figure. Use this [Matplotlib documentation page](https://matplotlib.org/gallery/pyplots/boxplot_demo_pyplot.html#sphx-glr-gallery-pyplots-boxplot-demo-pyplot-py) for help with changing the style of the outliers.

* Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

* Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

* Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. Plot the linear regression model on top of the previous scatter plot.

* Look across all previously generated figures and tables and write at least three observations or inferences that can be made from the data. Include these observations at the top of notebook.

### Copyright

Trilogy Education Services © 2020. All Rights Reserved.
