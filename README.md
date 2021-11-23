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
پایگاه آماری تحلیلی استاتیستا، گزارشی منتشر کرده که نشان می دهد سرمایه گذاری در فست فودها، بیش از سرمایه گذاری در بزرگترین شرکت های تکنولوژیک، سود دارد. از طرف دیگر مارجین سود برای کافی شاپ ها 25 درصد، برای فست فود ها 9 درصد و برای رستوران های سنتی و ایرانی حدود سه تا پنج درصد است. در بیزینس فست فود با مقدار جای کمتر و نیروی انسانی کمتر میتوان به حاشیه سود بیشتر و مقدار فروش بیشتر رسید.
بنابراین رستوران پیشنهادی برای راه اندازی فست فود است.
از طرف دیگر در جدول زیر اندازه بازار فست فود با رستوران ایرانی مقایسه شده است، همون طور که می بینید اندازه مارکت این دو رستوران در تهران تقریبا برابر است


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
در این قسمت دو منطقه شمال شهر و مرکز شهر را برای پیدا کردن مکان مناسب راه اندازی رستوران باهم مقایسه میکنیم.مرکز شهر 1940 رستوران دارد که ااز این تعداد 40 درصد آنها فست فود هستند. این درحالیست که در مرکز شهر 418 رستوران وجود دارد که از این تعداد 30 درصد آنها فست فود هستند. پس شمال شهر میزان کمتری فست فود در مقایسه با مناطق دیگر دارد
از طرف دیگر میتوانیم اندازه بازار را به تفکیک این دو منطقه حساب کنیم
میزان جمعیت هر منطقه بر اساس اطلاعات ثبت شده در سایت مرکز آمار ایران در نظر گرفته شده همچنین جمعیت هر منطقه 15 درصد بیشتر از مقدار واقعی آن لحاظ شده است (به دلیل رفت و امد در هر منطقه)

Explanation | DownTown | North
------------ | ------------- | -------------
Total population | 1.700.000 | 3.700.000
If a third of people eat out(one day) | 510.000 | 1.100.000
Average number of fastfood | 752 | 131
Average number of customers - fastfood | 200 | 200
Number of of coverage | 150.000 | 26.000
Not touched | 360.000 | 1.074.000
Not touched (Percentage) | 70% | 97%

همان طور که در جدول بالا مشاهده می شود، شمال شهر تهران نسبت به مرکز شهر با اینکه از لحاظ جفرافیایی کوچک تر است حدود دو برابر بیشتر جمعیت دارد. اگر فرض کنیم از کل جمعیت قابل دسترس در هر منطقه، یک سوم انها در روز  یک بار فست فود میخورند، پس در شمال شهر با جمعیت یک میلیون نفری و در مرکز شهر با نصف این جمعیت رو به رو هستیم. با فرض اینکه در رستوران فست فود در روز به صورت متوسط به دویست نفر بتواند سرویس بدهد، پس به صورت متوسط در مرکز شهر 30 درصد از این جمعیت و در شمال شهر فقط به سه درصد از آنها در حال حاضر ظرفیت برای استفاده از رستوران های موجود وجود دارد.
بنابراین در مرکز شهر تهران 70 درصد ظرفیت برای راه اندازی یک رستوران جدید فست فود وجود دارد و در مقابل در شمال شهر تهران 97 درصد طرفیت خالی وجود دارد. بنابراین مناسب ترین منطقه برای راه اندازی رستوران فست فود، شمال تهران پیشنهاد می شود.


## Step Four: What features and price level should our restaurant have, and why?
تا این قسمت تصمیم گرفته شد یک رستوران از نوع فست فود در قسمت شمال شهر تهران راه اندازی شود. در این قسمت قصد داریم ویژگی های مختلف این رستوران را تعیین کنیم. ویژگی هایی از قبیل ساعات کاری، قیمت، ارسال رایگان و سایر ویژگی ها.
طبق جدول 37 در فایل پایتون، اغلب فست فود های شهر تهران ساعات کاری شان از ظهر (حدود ساعت 12) شروع و تا پایان شب (حدود ساعت 11 ) ادامه دارد. بنابراین پیشنهاد می  شود رستوران جدید ساعات کاری 12 ظهر تا 12 شب داشته باشد.
به صورت متوسط رستوران های فست فود امتیاز 3.5 را در سفارشات خود به دست آورد اند. علاوه بر این،  متوسط کلاس قیمتی آنها سطح دو بوده است. بنابراین در صورت اتخاذ استراتژی مشابه به با بقیه رستوران ها، کلاس قیمتی سطح دو برای رستوران جدید  توصیه  می شود.
حال در مورد مابقی ویژگی های رستوران تصمیم میگیریم. به صورت کلی  هشت ویژگی در بین فست فود های تهران وجود دارد. که توزیع آن مطابق جدول زیر است:


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