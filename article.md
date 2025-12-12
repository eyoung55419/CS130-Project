# What is the best Super Bowl ad of all time?
One of the best parts of watching the Super Bowl is watching all of the creative and fun advertisements companies come up with. These ads fill the gap between the game and grab the attention of all types of people, not just the people who care about the game. Watching all these ads has led me to start thinking, what is the best ad of all time? To find out, I downloaded a data set that had lots of data on these super bowl ads. This data set contianed 219 different commercials, all from differing companies. The main companies that are featured are
- _NFL_ 
- _Doritos_
- _Budweiser_
- _Bud Light_
- _Coca-Cola_.

Another thing I set out to accomplish was find the company with the best ads, and determine what company has nailed the prodcution and execution of these ads. This article will feature my findings, as well as determine the best super bowl ad of all time.

## Views per Brand
The first way I compared brands against each other was finding their average number of views and making a bar graph with that data. A piece of code I wrote to help acomplish this was `brand_views = df.groupby("Brand")["Data.Viewership.Views"].mean().sort_values(ascending=False)`. This code took the brand and specifcally the number of views from the ad and took the mean from all of their ads. This allows me to account for a really good ad or a really bad ad and find the middle ground for all companies. 
! [A bar graph of average views per brand] (images\Average Views Per Brand.png)