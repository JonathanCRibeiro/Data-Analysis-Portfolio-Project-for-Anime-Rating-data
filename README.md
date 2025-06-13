This file contains data that I created to work on a portofolio project and demonstrate my skills in data analysis.
The first part is about importing modules I need to use. The second part of the jupyter notebook file is about cleaning up the data. Lastly, the third part of the data is about cleaning up the graphs.

I begin by importing anything I need including:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.cm as cm
import seaborn as sns
import scipy as sp
from scipy import stats

Fixing Data
- I remove the # symbol from the personal ratings column and change the dtype to a float.
- I use a flat series to find the most common number as well as finding the mean number for the data rating columns with missing data. Then I use .fillna to replace all NaN values with the mean.
- I then take the sum of each row and divide by the number of rating columns to reapply the cumulative number column which is meant for taking the average score across all rating columns but was wrong before because of the NaN values.
- I created a new decade column by using for loops and if statements on the release year column.
- I split the genre column which has two string values seperated by a comma into two columns, the first string value being kept in the genre column and the second string value in a new subgenre column.

Creating Graphs
- I group the personal rating column by genre and get the mean value per genre and standard deviation per genre and plot it into a line graph.
- I group the ratings columns by genre and get the mean score by genre and subgenre and graph multiple lines on a graph using a for loop.
- I create two bar graphs showing the amount of shows per genre and subgenre.
- I create a Histogram that shows the number of shows by number of episodes.
- I create two scatterplots that plot Personal Rating against Episodes and Release Year with regression lines and use hue to differentiate dots by demographic in the first graph and genre in the second graph.
- I creat a function to create a scatterplot that takes any two numerical data and plots it with a regression line and correlation coefficient.
- I create two box plots, one on demographics by release year and the second on genre based on cumulative rating
- I lastly create to pie charts showing the distribution based on demographics and decade.
