# 66-Days-of-Data

## Day 1:

Downloaded some weather and energy data I had never seen before. Rather than doing comprehensive EDA I updated the index by parsing datetimes, then plotted some sns.lineplots for select variables. I repeated the same process with weather. Created the data_vis notebook.

Completed Python, Pandas, Data Cleaning, & Data Visualization courses in Kaggle (some of these courses were completed a couple days before I decided to do the 66 days of data, so I am just adding them to day 1)

Read through a comprehensive EDA notebook in kaggle that I plan to pursue on a later date:
https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python

Thoughts:
-With Kaggle and all these online resources, it is easy to find a data set, look at it, do some computation, then move onto the next one. This is not realistic - if I were working on a problem I would be using the same dataset every single data, thinking about how to enhance that data set and testing out many different models on the same dataset. 
-Having metadata or an understanding of the columns is inredibly important. Given these datasets, what do I want to predict? What can be considered important to predict? Once I want to predict an output column that I deem important, I can then go into feature engineering and plot a heatmap of a correlation matrix to see what variables I might want to use to do some prediction. However, without the high level understanding of the information columns contain this is useless
-The direction of causality between variables comes from a human's better understanding of the problem. That is why column metadata is important - a human still must be familiar with the available data to structure a model correctly. An example, a model might predict weather based on ice cream sales, but the human knows the nature of that relationship is reversed. Ice cream sales do not change the weather, but the weather does change the number of ice cream sales

ToDo:
-Display probability distributions. I always enjoyed reading NNT The Black Swan and wanted to create interactive visuals to illustrate his points. This is the first step to creating those visually appealing diagrams with interactive widgets.

## Day 2:

Worked on some more visualization. I wanted these graphs to look nicer than the data_vis ones and wanted to get a better idea of how to mix seaborn, matplotlip, probplots. I played around with simple probability visualizations - given an empirical distribution, plotting it in hisplots, kdes, and probplots is a good way to understand the type of distribution you are working with. If you see variables you are working with do not conform to a certain distribution, then you can maybe think about transforming that variable. I play around with creating a skew normal variable and then transforming it by shifting then taking the log, but this still does not work. You can tell, however, that the shape of the data does change when you take the log of the original empirical distribution

Thoughts:
-Knowing why you should use a certain visualization is important. Visualization just help us intuitively understand what is going on - a visualization that is not easily readable and understandable is probably useless. 

ToDo:
-Visualize some shape transformations. We like to rescale and normalize data, what transformation maintain the shape of the original data, which transformation change it? Subtracting by the min and dividing by a number will maintain shape, but taking the log will change the shape



