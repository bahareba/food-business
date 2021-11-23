# What's the problem?
We want to set up a food business (restaurant, cafe, etc.) near the Tehran downtown according to [the available database of Iranian restaurants](data/iranian-restaurants-db.json).
we can do analysis by answering the following questions:

1. Is Tehran downtown a good option for starting the business? Is there another option? (If you have another option, you can do the rest of the analysis based on it. You can also use the whole city of Tehran as an option if it becomes easier.)
2. What kind of restaurant do you recommend?
3. If possible, provide your suggested approximate geographical coordinate for setting up the restaurant.
4. What features and price level should our restaurant have, and why?
5. If possible, show the distribution of restaurants in Tehran.
so let's get started!

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
 The main purpose of  this sessection is to determine best charactrestics of a new restuant to start it. Features like ​type of the resturan , location and other feature about it. In our sproject we concentrate on factors one should take into account base on avaiable data. Now, we present a hierarchical model where both qualitative and quantitative factors can be taken into account by using analytic hierarchy process (AHP) technique. The analytic hierarchy process (AHP)  is a method used to solve multicriteria problems, which includes both quantitative and qualitative data. 
AHP has three major steps:
a) Problem Decomposition: The problem is decomposed into elements, which are grouped at different levels to form a chain of hierarchy and each element is further decomposed into sub-elements until the lowest level of hierarchy.
b) Comparative Analysis: The relative importance of each element at a particular level is measured by a procedure of pairwise comparisons. Decision makers must make a series of pairwise comparisons, which are made on the basis of nine scale.
c) Synthesis of Priorities: The third step is synthesizing the priorities of the elements to establish the overall priorities for decision alternatives. 








# How to fork the project and send the result back to us?

1. Click on the fork button ![Fork Button](images/readme/fork-button.png)
   ![GitLab Fork Icon](images/readme/gitlab-fork-icon-blur.png)
2. Fill in the "Fork Project" form, then press the "Fork project" blue button.
3. Do your stuff, at the end give us access to your forked repository by the following steps:
   1. Click on the "Project information" on the left menu, then click on the "Members".
   2. Fill in the form:
      * GitLab member or Email address: *@fanap.plus.co*
      * Select a role: *Developer*
   3. Then press the "Invite" blue button.


According to the U.S. Census Bureau, there are approximately 78 full-service restaurants per 100,000 Americans, and annual restaurant sales amount to $704.18 per person. 