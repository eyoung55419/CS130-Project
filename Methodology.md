# What is the best Super Bowl Ad of all time?
## Data Source
I found this csv file about Super Bowl ads online at [Corgis](https://corgis-edu.github.io/corgis/csv/). This data source was selected because I love football and I always am intrigued by the ads that run during the biggest football game of the year. One of the biggest talking points around the super bowl is the ads, and it generates a lot of revenue for the companies that run the ads.
## Data Preperation/Cleaning
In order to make the data a little easier to work with, I did a few things. First, I changed a few important variable names in order to make writing the code easier. I changed 3 different variable names
- _Data.Viewership.Views_ 
- _Data.Viewership.Likes_ 
- _Data.Viewership.Dislikes_ 

In all 3 of these names, I replaced the periods with underscores in an effort to make the code simplier to write. The end result was
- **Data_Viewership_Views**
- **Data_Viewership_Likes**
- **Data_Viewership_Dislikes**

 Another thing I did was create two new variables, 'Likes Divided by Views', and 'like_percentage'. These variables helped me create another metric to grade these ads off. They are related because the like percantage is just the likes divided by views times 100.
## Assumptions
Some assumptions I made when I looked over the data was that every ad ran for the same amount of time, whatever that time was. The reason I made this assumption to level the field for all ads so one ad didn't have an advantage on another. A second assumption I made was that if the ad had been played at a different time during the game, the views would have been the same. I did this so it was easier to just calculate values and use the data to show the true best ad, not just the best ad based on when it was shown. I also turned this thought process into the year and that every year the same amount of people has the oppurtunity to watch the ads.
## Limitations
One limitation I ran into when using this data was every single true false value was true. This created a problem because it limited the amount of experiments and code I could run on the data. Another limitation was it only has gone up until 2020, so the past few years are not included in the data set. If these ads had been included, the data would have been different and the best ad might have changed. Finally, the number of people who watch the super bowl every year fluxuates, so if there is a spike in views or a lull in views, ads might be made out to look better or worse then they should have. 