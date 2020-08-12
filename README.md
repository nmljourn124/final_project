# J124 Final Project: Analyzing the Most Common and Highest Paying College Majors
### The data for this project was recorded from a survey given to recent college graduates under the age of 28. The dataset contains information about median earnings, employment status, major in college, and much more.
#### By Nicole Lee

The dataset that I used for this project was from the [FiveThirtyEight Github Data Repository](https://github.com/fivethirtyeight/data). The FiveThirtyEight dataset that I used can be found in the files of my repository or can be downloaded through this [link](https://github.com/nmljourn124/final_project/blob/master/recent-grads.csv). The original data was sourced from the American Community Survey 2010-2012 Public Use Microdata Series and can be downloaded [here](http://www.census.gov/programs-surveys/acs/data/pums.html).



## Steps I Took to Clean My Data
The data had already been cleaned, so the initial steps I took when opening the doc was just to make the sheet easier to read.
1. Secured the header row, then bolded and highlighted the values and cells to differentiate it from the rest of the table.
2. Text wrap the sheet so that everything is visible in each cell.


## Interrogating My Data
After cleaning my data, I put a filter on my entire dataset to find the highest and lowest value of each column. Here is a bulleted list of some information that piqued my interest:
* Most common major for women: Psychology (307,087)
* Least common major for women: Military Technologies (0)

* Most common major for men: Business Management and Administration (173,809)
* Least common major for men: School Student Counseling (119)

* Military Technologies was the major with the least total people employed (0)
* Psychology was the major with the most total people employed (307,933)
* Most full-time employed major: Business Management and Administration
* Least full-time employed major: Military Technologies

* Most full-time, year-round employed major: Business Management and Administration
* Least full-time, year-round employed major: Military Technologies

* Business Management and Administration and Psychology are the top two majors for having the most number of graduates with a job not requiring a college degree
* Psychology and Business Management and Administration are also the top two majors for having the most number of graduates in low-wage service jobs



## Making Sense of What I Found
#### Looking at the category of "Total People Employed," I realized that my initial finding was not as surprising as I initially believed.
Military Technologies has the least total people in a major and Psychology has the most. So taking their total number of graduates into account, the fact that those two came up as the majors with the least and most total people employed is reflective of the data. 

#### Psychology and Business Management and Administration are the top two majors with the greatest number of people unemployed
This is surprising since:
* Business Management and Administration was identified as the major with the most full-time employed graduates
* Psychology is the most part-time employed major
* Business Management and Administration has the most full-time, year-round employed
* Psychology has the most total people employed (307933)

It was also important to keep in mind that *having the greatest number of people unemployed DOES NOT mean that you have the highest unemployment rate*. Nuclear Engineering and Public Administration are the top two majors with the highest unemployment rate.This is because:

                Unemployment rate = Unemployed / (Unemployed + Employed)

So because Psychology and Business Management and Administration have far greater employed individuals, their overall unemployment rate is decreased.




## Visualizing What I Found
After everything I found through filtering, I noticed that there were a handful of majors that kept resurfacing when searching for the highest and lowest values of each column. I wanted to compare the data on the spreadsheet by majors. So after a second round of cleaning, I began to make pivot tables and graphs.

### Second Round of Cleaning

1. Deleted the following columns:
* Major code
* 25th percentile of earnings
* 75th percentile of earnings
* sample size

2. Changed the values under "sharewomen" to be percentages and then moved this column next to the "women" column
3. Created new column next to "men" called "sharemen" to reflect the percentage of males out of the total in each major. Used the following forumla to divide the males in each major over the total number of graduates:

               = D2/C2
* Applied the formula to the whole column
* Converted all the values in this new column to percentages




## Data Visualizations
As mentioned earlier, Psychology was found to be the most common major for women and Business Management and Administration the most common for men. The following graph illustrates the breakdown of both men and women in each major.


<iframe title="Most Common College Majors for Men and Women" aria-label="chart" id="datawrapper-chart-Yb0qW" src="https://datawrapper.dwcdn.net/Yb0qW/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="579"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

[pivot table](https://media.journalism.berkeley.edu/upload/2020/08/1597200393f0a197c.png)


*A realization you may have after seeing this graph is that "sharemen" and "sharewomen" do not indicate which major has more men or women. Percentages do not reflect the number of individuals in each major. So while Psychology and Business Management and Administration may not have the highest percentages of each gender in their major, they do in fact have the most women (Psychology) and men (Business Management and Administration).


The next question I asked and wanted to see the answer to visually was whether the median income of each major affects the number of people who choose that major. The following graph answers this question.


<iframe title="Median Earnings of College Majors" aria-label="chart" id="datawrapper-chart-paQ5q" src="https://datawrapper.dwcdn.net/paQ5q/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="620"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


I was surprised to find that the majority of recent graduates clustered around a median earning of 40k. After observing this distribution, I began to wonder what drew the most men and women to Business Management and Administration and Psychology. It cannot be for monetary reasons because surely there are other majors that pay more. As a result, I wanted to illustrate the difference in median earnings between the lowest and highest paying college majors to visually see the difference in pay.



<iframe title="Median Earnings of Lowest and Highest Paying College Majors" aria-label="Split Bars" id="datawrapper-chart-OKpHK" src="https://datawrapper.dwcdn.net/OKpHK/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="276"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


Digging into this dataset further, I was curious to see the percentage of recent graduates unemployed with these majors and the percentage of women in each of these majors.


<iframe title="Unemployment Rate and Percentage of Women in the Highest and Lowest Paying College Majors" aria-label="Grouped Bars" id="datawrapper-chart-S2V7P" src="https://datawrapper.dwcdn.net/S2V7P/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="367"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


## Wrapping It Up
Overall, there was a lot of insight drawn from analyzing this dataset. The information that I found made me question the way our society views, uses, and values higher education. These are some of the questions I pondered. I hope you reflect on them as well.
* What does this dataset say about the *value* of each major? (This of course can differ based on tuition cost, amongst other factors)
* What careers are deemed to be "more valuable" because they get paid more?
* Does the proposed median earnings of a major affect the major that students choose?


