# data-analysis-project: The Tips Data Set 
## Elizabeth Daly

### HDip Data Analytics 2019 Fundamentals of Data Analysis Assessment

Git-hub repository at:
https://github.com/elizabethdaly/data-analysis-project.git

- Jupyter notebook: tips-data-analysis.ipynb
- Dataset: tips.csv

![Tips](images/tip.jpg)

# Table of contents
1. [Introduction](#introduction)

2. [Description of the data set](#section1)

3. [Regression](section2)
    
3. [Relationships between variables](#section3)
    
4. [Work done by other people on the Tips data set](#section4)
    
5. [Conclusion](#conclusion)

6. [References](#references)

## 1. Introduction <a name="introduction"></a>
This README describes work done on the Tips data set for the Fundamentals of Data Analysis module assessment due 29 November 2019. Resources used include Python and associated packages Jupyter, matplotlib, and Seaborn. The analysis takes the form of a single Jupyter notebook of filename given above. To view this file, download it from this repository and run Jupyter notebook, which comes as part of the Anaconda distribution of Python (as do the other packages listed above). Alternatively, view a static version of the notebook (by providing its GitHub url) using Jupyter Nbviewer. The Tips data set is incuded in the Seaborn visualization library. It can be loaded provided one has access to the internet when running the notebook. For the sake of completeness, I have downloaded the data set from the site referenced in the project instructions, and I include it in this repository as a csv file. I have also tried to break the Jupyter notebook into sections which roughly correspond to the sections of this README.

##  2. Description of the data set <a name="section1"></a>
The Tips data set contains 244 rows of data relating to tips left in a restaurant. It includes the total bill, tip, number in the party, day of week, time of day, gender of the diner, and whether or not they are a smoker. I would say that the basic question is: does the tip amount depend on the total bill? One can also ask if the other variables influence the tip amount. Some of these questions will be addressed in section 3. <!--put in a ref-->
I often use sites such as Medium.com to see how other people have investigated data sets using Python. Two examples of such exploratory data analyses are given in the reference list. The very first step is always to check if the data needs cleaning by looking for duplicate rows, zero values or NaNs where they shouldn't be, etc. Our data set is small enough to inspect visually and it looks fine. Counting the number of valid entries in each column confirms this. 

Pandas **decribe()** can provide a quick summary of the data set as outlined in the notebook. However, without looking at the data in more detail, we cannot yet state what we think a typical diner is. What I mean is, just because most of the diners are male, smokers, and eating dinner on Saturday when we consider one variable at a time, that doesn't mean that all of these conditions are met simultaneously. 


##  3. Regression <a name="section2"></a>
For this part of the assessment, we have been asked to analyse if there is a relationship between the total bill and the tip amount. The simplest relationship would be a linear one. That's reasonable when we consider that tips (especially in the US) are usually a fixed percentage of the total bill. In the notebook we first use Seaborn to visualize any linear realtionships beween our two variables of interest using regplot. This does not give us any fitting parameters such as the slope and intecept of the linear fit, or any metrics to assess the quality of the fit, but it's a good start. We then move on to using two packages, Statsmodels and scikit-learn, to perform linear regression and return fitting parameters and metrics. Statsmodels is a Python package for performing statistical analysis of data - we are interested in the OLS (Ordinary Least Squares) module for performing linear regression. OLS involves fitting a linear model with coefficients to minimize the residual sum of squares between the observed data points and the targets predicted by the linear approximation. Scikit-learn is a machine learning package which can also perform OLS fitting. Strictly speaking there is no need to perform regression with both packages, but I will do it once and then stick to scikit-learn which will be useful if we want to make any predictions using the dataset. $R^2$ is the coefficient of determination, a measure of how close the data points are to the regression line; or how much of the variation in the data is explained by the linear model. It ranges from 0 to 1, and in general, higher values of $R^2$ are better. However, as the minitab link in the references discusses, that's not the full story.
Summary y=mx+c Rsquared. 
. Why one over other? ML predict classify?

## 4. Relationships between variables <a name="section3"></a>

## 5. Work done by other people on the Tips data set <a name="section4"></a>

## 6. Conclusion <a name="conclusion"></a>

## 7. References <a name="references"></a>
- [1]  Anaconda Distribution
https://www.anaconda.com/
- [2] Python Software Foundation
https://www.python.org/
- [3] Project Jupyter
https://jupyter.org/
- [4] Sharing Jupyter notebooks
https://nbviewer.jupyter.org/
- [5] seaborn: statistical data visualization
https://seaborn.pydata.org/index.html#
- [6] matplotlib: Python plotting library
https://matplotlib.org/
- [7] The Tips dataset from Michael Waskom
https://github.com/mwaskom/seaborn-data/blob/master/tips.csv
- [8] Description of what is contained in the tips set
https://www.kaggle.com/ranjeetjain3/seaborn-tips-dataset
- [9] How to investigate a data set with Python
https://towardsdatascience.com/hitchhikers-guide-to-exploratory-data-analysis-6e8d896d3f7e
- [10] Data analysis with Python
https://medium.com/@onpillow/01-investigate-tmdb-movie-dataset-python-data-analysis-project-part-1-data-wrangling-3d2b55ea7714
- [11] Python for Data Analysis: Data Wrangling with Pandas, NumPy, and IPython. 
Wes McKinney. ISBN-13: 978-1491957660 ISBN-10: 1491957662
- [12] Pandas In 10 Minutes || Wes McKinney
https://www.youtube.com/watch?v=1MGCD8SQp3k
- [13] Good description of quartiles on Seaborn plots
https://towardsdatascience.com/analyze-the-data-through-data-visualization-using-seaborn-255e1cd3948e
- [14] Ordinary Least Squares in statsmodels
https://www.statsmodels.org/dev/examples/notebooks/generated/ols.html
- [15] Generalized Linear Models in scikit-learn
https://scikit-learn.org/stable/modules/linear_model.html#ordinary-least-squares
- [16] How to run Linear regression in Python scikit-Learn
https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/
- [17] A beginner’s guide to Linear Regression in Python with Scikit-Learn
https://towardsdatascience.com/a-beginners-guide-to-linear-regression-in-python-with-scikit-learn-83a8f7ae2b4f
- [18] Regression Analysis: How Do I Interpret R-squared and Assess the Goodness-of-Fit?
https://blog.minitab.com/blog/adventures-in-statistics-2/regression-analysis-how-do-i-interpret-r-squared-and-assess-the-goodness-of-fit
- [19] PYTHON MACHINE LEARNING EXAMPLE – LINEAR REGRESSION
https://devarea.com/python-machine-learning-example-linear-regression/#.XbbfgOj7Q2w
- [20] STAT 503 Case Study 1: Restaurant Tipping
https://dicook.public.iastate.edu/stat503/05/cs-tips2.pdf
