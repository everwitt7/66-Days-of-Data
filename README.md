# 66-Days-of-Data
[Kaggle Mirco-Courses](https://www.kaggle.com/learn/overview)

## Day 1:

Downloaded some weather and energy data I had never seen before. Rather than doing comprehensive EDA I updated the index by parsing datetimes, then plotted some sns.lineplots for select variables. I repeated the same process with weather. Created the data_vis notebook.

Completed Python, Pandas, Data Cleaning, & Data Visualization courses in Kaggle (some of these courses were completed a couple days before I decided to do the 66 days of data, so I am just adding them to day 1)

Read through a [comprehensive EDA notebook](https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python) in kaggle that I plan to pursue on a later date:


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
-Mess around with running some statistical tests on data sets. Run my own permutation tests and other parametric tests

## Day 3 & 4

I successfully did nothing - off to a great start!!! I was in a car for two days, so I just thought about some things:

Thoughts:
-While driving to the Florida Keys there was an accident, and Google Maps estimated that I would get to my destination a 12:20. However, I arrived around 1:30. To give some context, the drive would have been around 2 hours without traffic. How could Google Maps have done such a terrible job at predicting this specific drive? 

On the way back there was no traffic and I got back within 1 minute of the initial arrival time. That's pretty damn good prediction for a 2 hour drive. This illustrates two things: Google Maps is great at predicting common historical trends - most drives (which are accident free) will be historically similar. The average time it takes to get from A to B may be predicted from historical data. However, Google Maps is terribly equipped to deal with outliers like the one I experienced. The arrival time is basically guaranteed to be innacurate when an accident occurs - something that is really hard to take into account/assign a quantitative value to. Using expected value doesn't make sense in this case imagine it takes 5 mins to get somewhere to get somewhere without and accident and 55 mins to get to that place with an accident, estimating 30 mins on average does not make sense. This is basically guaranteed to almost always be wrong! Furthermore, the mean is not robust to outliers, and in this case accidents will affect the expected value by a large margin.

Accidents must have enough variability to make prediction very hard. I would have guessed that the time it takes to remove the accident from the highway and the time people spend looking as they pass the accident follow some sort distribution that can be historically estimated, similar to how arrival may be estimated. It is pretty clear, however, that Google struggles to estimate the time added due to an accident. The estimated arrival time on maps would increase very slowly, only a minute or two at a time. It would just do this consistently over time and dynamically update. I would argue, if they knew how to truly estimate the timing impact of an accident, then they would have one large update to account for the difference. (in my case, the estimated time should have gone from 12:20 to 1:30 in one jump rather than many jumps of small changes)

Time series data is difficult. Things might act the same way and follow a pattern for a majority of the time, but suddently out of nowhere it behaves completely differenty. I would argue that this is something that Nassim Nicholas Taleb would call a grey swan. You know that accidents will occur, but forecasting the affect of them is incredibly difficult. Given the way Google Maps updates their arrival time estimation it appears that they might not even try to predict the effect of an accident (I know they most likely do, but the behavior of the app seems incompatible). 

-Enough about driving, let's talk about Instagram! Specifically ads. The ad designs are actually incredibly impressive; I think that I ignore ads more then the average person (but maybe 80% of the population also feels this way...) but I interacted with a couple ads recently. I am not privy to how much information these companies have on me - what are their inputs that determine what ad they should display to me (unrelated rant, but it is actually absurd that you cannot see the data that companies have on you!!!)? Instagram probably tailors ads to a degree, but it is not possible yet to create a one to one personalized ad for each person, you can group like people together and show them an ad, but it will still be more generalized that a one to one ad. I saw many a puzzle game ad that would intentionally do most of the moves to solve the puzzle correctly, but then mess up something that the viewer could catch instantly and think to themself "hey, don't do that, that's not how you do that..." The goal of the ads may have been to get the person flustered and have them interact with the ad - I am not too sure, but it defenitely worked on me. I have attached an image of one ad that stood out in particular, one where you tried to draw a shape in one continuous motion without overlapping on previously drawn lines. I have attached an image of one so that anyone can recreate my experience. I think this ad took it a different approach then making an obvious mistake to upset the viewer; I beleve this drawing ad gave an impossible puzzle that was framed rather easily. I actually still do not know if the object is possible to trace in one continuous motion without overlapping lines, but that is besides the point. The ad got me hooked - it did an incredible job! I even visited their Instagram page to see if there was a solution or if anyone was pleasantly frusturated like myself. 

Though I do not have this information, I would love to know what the conversion rates are of ads that mess something up intentionally and the viewer knows they can solve the puzzle in the ad. If I saw an almost perfectly set table and one person keeps messing up the placement of a cup, then tries again, and messes up the placement again. I would want to stop being the observer and take action myself and place the cup in the right location! That is how I view these ads; they are slightly unsatisfying and you want to fix it. Very very interesting stuff.

## Day 5

I completed the Kaggle Introduction to SQL micro-course. I had some previous experience with SQL but this introduced some knew things and actually helped me understand the logic behind some more advanced queries I had seen but did not fully understand. I also downloaded PostgreSQL and PG Admin to play around with setting up my own local database. 

Thoughts:
-Reading and understanding the theory behind certain models and concepts is very important. However, I like to play with things on my own... I would prefer to have a dataset and have a faint idea of what I am doing and then change inputs, and see how my outputs change. To play around one needs to have the right tools! In the Data Science context that would mean and familiarity and understanding of databases and design, a language like Python (or R) to interact with the pulled data, and Linux to access the database that is on a cloud (or maybe remote) server. The point is something like Linux, which might seem unecessary for someone doing datascience, might actually be integral to a part of the process. So you have to learn these things.

## Day 6

I completed the Advanced SQL micro-course, spent some time doing 3 problems on [StrataScratch](https://www.stratascratch.com/). I also watched some videos from [Data Science Jay](https://www.youtube.com/c/DataScienceJay/videos) that went through mock interviews/problem solving. 

Thoughts:
-Maybe the material is just fresh, but i was able to solve all of the problems I attempted with relative ease. I expected them to be harder; to be fair, I realize I should be more comfortable with datetimes and passing inputs into aggregate and analytical functions, but that will come with practice. 

ToDo:
-Write Anki notecards based on the information that I have learned so far. The best way to continue to learn and practice SQL is to write queries, struggle, do things wrong, see how others performed the task, understand why their approach was better, then insert that information into Anki. Using an SRS system for practice like this will probably be useful (I assume) and help internalize that approaching certain problems in a certain way (e.g. I realize can use a left join here to find the missing values between these tables). 

## Day 7, 8

I spent a majority of my time working on a baseball analytics project. Being able to write clean, well documented code is still important (and thinking through the structure of your code).

## Day 9

I went through some example [videos](https://www.youtube.com/watch?v=TYHWv1vT0Pk) of manipulating and extracting dates in SQL. It's rather important because month, year, and year-month timing stratification is incredibly common.

## Day 10

Created SQL cards for Anki. Now this won't just be a 66 day thing but an everyday thing.

## Day 11, 12

Spent time working on a baseball analytics project again. Nothing crazy, but lots of coding - fixing bugs and creating new ones. 

## Day 13






