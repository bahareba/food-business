# What's the problem?
We want to set up a food business (restaurant, cafe, etc.) near the Tehran downtown according to the available database of Iranian restaurants.
we can do analysis by answering the following questions:

1. Is Tehran downtown a good option for starting the business? Is there another option? (If you have another option, you can do the rest of the analysis based on it. You can also use the whole city of Tehran as an option if it becomes easier.)
2. What kind of restaurant do you recommend?
3. If possible, provide your suggested approximate geographical coordinate for setting up the restaurant.
4. What features and price level should our restaurant have, and why?
5. If possible, show the distribution of restaurants in Tehran.
so let's get started!

****Used libraries: pandas, numpy, json, folium, seaborn, sklearn ****


## Step One: Is Tehran downtown a good option for starting the business?
According to the U.S. Census Bureau, there are approximately 78 full-service restaurants per 100,000 Americans, and annual restaurant sales amount to $704.18 per person. Since people in Iran don't eat out all the time (just like what they do in let's say the USA) and they mostly prefer homemade food, so I will multiply 100/000 to 10  in order to have a better indicator for Iran's cities.

So we shall have 78 restaurants for each 1 Million people.  If the currently available restaurants are less than the given estimation then we suppose that demands are less than supply in that city. In the same way, if restaurants are more than the population then it shows us that we have a high rate of demands there and finally if both meters match each other, it simply means that we have equality in demand to supply rate.
( We assume that the current data set contains the whole restaurants of the cities)

Therefore the best restaurant for establishing our restaurant is Kish since the number of available restaurants is 1200 times more than the standard (78 restaurants for each 1M).
So we come to this conclusion that the market size is big enough in this city.

We will put Tehran city in second place as the current number of restaurants in the city are 300% bigger than our considered standard.

From Tehran to other cities in lower ranks we see that demand to supply rates are equal and launching a new restaurant in those cities doesn't seem to be a good economic decision.

Calculations and information corresponding that are well written in the first part of the Python code.


## Step Two: What kind of restaurant do you recommend?
Since the numbers of samples available in the selected city (Kish restaurants) is not big enough, to achieve the analysis and better results, we continue the analysis based on Tehran restaurants.
Statista statics portal has released a report which shows the rate of investments in Fast-Food industry is much more profitable than technological companies. On the other side, the profit margins for coffee shops are 25% and 9% for fast foods and around 3% to 5% for traditional Iranian restaurants.

In fast foods even with less human resources and workspace compared to the others, you will gain more profit margin so I suggest launching a fast food business among all available options.

On the other hand, we have compared the market size of fast foods with traditional Iranian restaurants in the following table. As it is obvious, the market sizes are almost equal.

Explanation | Num
------------ | -------------
Total population of Tehran | 8.600.000
If a third of people eat out(one day) | 2.500.500
Number of fastfoods | 883
Number of Iranian | 721
Average number of customers - fastfood | 200
Average number of customers - Iranian | 174
Percentage of coverage - fastfood | 7%
Percentage of coverage -  Iranian | 6%

## Step Three: If possible, provide your suggested approximate geographical coordinate for setting up the restaurant.
In this section, we are comparing two regions, one in Northside of the city and the other in the downtown, to find a suitable place for setting up our restaurant. 
We have 1940 restaurants within the downtown of which 40% are fast food. This is while we have 418 restaurants in the northern region from which 30% are fast foods.
So we come to this conclusion that the north side of the city holds the lesser amount of fast foods compared to the other regions.

We can calculate the size of the market separately sorted by these two regions.
We have considered the population size of each region ( considering 15% higher than the actual amount to cover commuting among the regions) based on the registered information on the website of the Statistical Centre of Iran.

Explanation | DownTown | North
------------ | ------------- | -------------
Total population | 1.700.000 | 3.700.000
If a third of people eat out(one day) | 510.000 | 1.100.000
Average number of fastfood | 752 | 131
Average number of customers - fastfood | 200 | 200
Number of of coverage | 150.000 | 26.000
Not touched | 360.000 | 1.074.000
Not touched (Percentage) | 70% | 97%

As you can see in the above table, although that geographically northern side is smaller than the downtown, we have 2 times more population in the north side of the city compared to the downtown.
Based on this assumption that from the whole available population, 1/3 of them eat fast food once a day, so we are dealing with around 1 million population in the northern side and half of them in the downtown.

With this assumption that each fast food is capable of serving 200 customers per day, so on average, they are capable of serving only 30% of the downtown population and 3% of the northern side population.

ُ Therefore, there is 70% capacity in the downtown and on the other side 97% availble capacity on the northern side to launch a new fast food.
So the most suitable place for setting up a new fast food is the northern side of Tehran.

## Step Four: What features and price level should our restaurant have, and why?
Until now, it has been decided to set up a fast food restaurant in the northern part of Tehran. In this section, we intend to determine the different features of this restaurant. Features such as working hours, price level, free delivery and other features.
According to Table 37 in the Python file, most fast foods in Tehran start at noon (around 12 o'clock) and continue until the end of the night (around 11 o'clock). Therefore, it is suggested that the new restaurant be open from 12 noon to 12 pm.
On average, fast food restaurants scored 3.5 on their orders. In addition, their average price class was level two. Therefore, if you adopt a similar strategy to other restaurants, a level two price class is recommended for the new restaurant.
Now we decide on the other features of the restaurant. In general, there are eight features among fast foods in Tehran. Whose distribution is according to the following table:

Features | Percentage
------------ | -------------
pos | 99%
free delivery | 76%
free internet | 19%
parking | 9%
outdoor | 5%
tobacco | 3%
view | 1%
music | 1%

Naturally, the characteristics of the restaurant depend on its marketing strategies and entering the market. On the other hand, the first two features are very important for the restaurant due to their distribution. However, we ignore these assumptions and use the AHP method to determine the weight and importance of each feature, respectively.

The main purpose of  this sessection is to determine best charactrestics of a new restuant to start it. Features like ​type of the resturan , location and other feature about it. In our sproject we concentrate on factors one should take into account base on avaiable data. Now, we present a hierarchical model where both qualitative and quantitative factors can be taken into account by using analytic hierarchy process (AHP) technique. The analytic hierarchy process (AHP)  is a method used to solve multicriteria problems, which includes both quantitative and qualitative data. 
AHP has three major steps:
a) Problem Decomposition: The problem is decomposed into elements, which are grouped at different levels to form a chain of hierarchy and each element is further decomposed into sub-elements until the lowest level of hierarchy.
b) Comparative Analysis: The relative importance of each element at a particular level is measured by a procedure of pairwise comparisons. Decision makers must make a series of pairwise comparisons, which are made on the basis of nine scale.
c) Synthesis of Priorities: The third step is synthesizing the priorities of the elements to establish the overall priorities for decision alternatives. 

According to Table "Features_A_minmax", the weight (importance) of each feature is as follows,respectively:

Features | Weight
------------ | -------------
outdoor | 63%
free internet | 44%
pos | 42%
free delivery | 37%
parking | 29%
tobacco | 17%
view | 11%
music | 5%


## Step Five: show the distribution of restaurants in Tehran.
This is shown in the Python file.



# End