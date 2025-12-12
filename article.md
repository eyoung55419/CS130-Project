# What is the best Super Bowl ad of all time?

One of the best parts of watching the Super Bowl is watching all of the creative and fun advertisements companies come up with. These ads fill the gap between the game and grab the attention of all types of people, not just the people who care about the game. Watching all these ads has led me to start thinking, what is the best ad of all time? To find out, I downloaded a data set that had lots of data on these super bowl ads. This data set contianed 219 different commercials, all from differing companies. The main companies that are featured are

- _NFL_ 
- _Doritos_
- _Budweiser_
- _Bud Light_
- _Coca-Cola_.

Another thing I set out to accomplish was find the company with the best ads, and determine what company has nailed the prodcution and execution of these ads. This article will feature my findings, as well as determine the best super bowl ad of all time.

## Amount of views per Brand

The first way I compared brands against each other was a bar graph of [average views per brand](images/first_graph.png). Finding their average number of views and making a bar graph with that data allows me to compare brands side by side to help understand the data. A piece of code I wrote to help acomplish this was `brand_views = df.groupby("Brand")["Data.Viewership.Views"].mean().sort_values(ascending=False)`. This code took the brand and specifcally the number of views from the ad and took the mean from all of their ads. This allows me to account for a really good ad or a really bad ad and find the middle ground for all companies. By looking at the graph, it is clear and obvious that Doritos has far and away the highest average view total. This indicates that Doritios has ads that a lot of people wanna watch compared to the other ad companies.

## Number of likes per Brand

In order to determine which ads generate the most amount of likes, I created a bar graph with [number of likes per brand](images/second_graph.png). This graph is created by sorting all ads by most likes and selecting the top 10 rows. Then, it creates the bar graph using the companies that are included in the first 10 rows. When this image is created, the Doritios bar is much larger then all other companies, reaching ober 250,000 likes, which is another sign that their ads have the highest number of likes by volume alone. This number can be useful because it illustrates more closely the best ad the company has created over the years. A piece of code that helped me determine this fact was `top_likes = df.sort_values("Data.Viewership.Likes", ascending=False).head(10)` which is the sentence that sorted the rows in the correct order, and then took the top 10 and put them into the graph.

## Final Score

The final graph I created was using code I had written to find what I called a [final score](images/third_graph.png). This metric weighted views, likes, and dislikes and put them into a formula. The formula I created was `df["Final_Score"] = (0.45 * df["Data.Viewership.Views"] + 0.35 * df["Data.Viewership.Likes"] - 0.20 * df["Data.Viewership.Dislikes"])`, and I felt this had a fair weighting system as views and likes matter the most, while dislikes can still affect your overall score. Putting all rows into this formula and creating a list came out as row 127 having the highest score at 79445798.80. This score can be clearly seen on the graph, as it is the Doritos bar. Three other ads came out to have a score greater then 10000000.00, and those ads belonged to Budweiser, NFL, and Coca-Cola, respectively. While these ads had a very good score, it was not even close to the final score of the Doritios ad. 

## Limitations

While this data set was very useful, one problem with the data is it is a little outdated, as the lastest year they have is 2020. If the data set included the past few years up until 2025, the data would be different and maybe a different commercial would be the best. Another limitation is I was only able to use a few columns in the data set as a few columns had only true, which limits the amount of code I could run. Finally, the data is heavily dependent on the amount of people who watch, and that fluxuates year to year, so an ad might have an advantage just because more people had the oppurtunity to watch it.

## Conclusion

In conclusion, after all the code had been run and graphs had been created, not only did the best company become obvious, but the best ad also came to fruition. 

### Best Single Ad

The best ad from the data set, and of all time was row 127. That was the Doritios ad from 2012, and it was by far the best ad. It had a ton of views, right up near the top of all commercials in total views, as well as likes. While it also had a fair amount of dislikes and a low like percantage, that can be accounted for just because of the sheer number of views. The ad has generated

- **176373378 total views**
- **275362 likes**
- **.156124 like percentage**

On the whole, using this data, and process of elimination, this ad is the best ad of this data set and more companies should strive to get the data/revenue that this ad generated.

### Best Company

After running all the tests, the best company at making super bowl ads is Doritios. They led in every statistic that I ran, and had a clear advantage in the graphs. They also dominated the total share of views between all companies, as shown in this [pie chart](images/fourth_graph.png). Finally, they not only have the best ad using the data, they also have other ads that performed very well, such as row 153. This is an ad from 2014 that saw a total number of views equal to 7952240 and total number of likes equal to 18729. It also saw a like percentage of 0.235519. Overall, Doritios has created a few very good commercials, with having the number 1, and that gives them the best super bowl ads as a company.