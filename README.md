# Analysis-of-Publisher-Book-Quality

## Research Proposal Data

This dataset has been compiled by user Soumik and uploaded for public use on kaggle. The author cites creating this dataset for "bookies" desiring a "good clean dataset of books" that displayed information easily. The data is a compilation of books that have been reviewed on Goodreads. The information includes the books' details (title, author, publisher, language, number of pages, and publication date), as well as the books' average rating, number of ratings, and how many text reviews there were for each book. 

I am interested in seeing how the ratings of books corresponds to its publisher, and thus determining if there is a significant difference between the different publishers and their book quality. To accomplish this, I will focus on two columns: the average rating and the publisher. Since there are multiple publishers, I will narrow down my data to the top 3 publishers in terms of amount of books published. This will allow me to use the publishers with the most data and make it easier to run different comparison tests.

## Research Design and Audience

1. Research Design

My hypothesis is that there is no discernable difference between publishers and the quality of books that they publish. Potential authors can rest easy knowing that for whichever publisher they choose, it will not be an indication of their quality. It will also allow customers to choose from a wider selection of books, knowing that there will not be a dip in quality between publishers.

First, I will create a new dataframe that contains only the top 3 publishers in terms of the amount of books published by that publisher, and the rating of each of those books.

I will test this data for normality by plotting the data on histograms. Then, after running a visual test for normality and observing the skewness and kurtosis for confirmation of normality, I can follow two paths. 

If the data is normally distributed, I will conduct another normality test by using the one-way ANOVA test (since there are three groups to compare) and check the resulting p-value against my desired alpha (I will be using .05). This will check for any significant differences in publisher quality. I will then run a Turkey's Honest Significant Differences Test to check for any groups that may stand out and reject the NULL hypothesis. 

If the data is not normally distributed, I can perform a non-parametric test, namely the Kruskal-Wallis test. Logically, it is similar to the one-way ANOVA test, so  I can still check the p-value against the alpha to determine if there is a siginificant difference between the three publishers in terms of review quality, as well as the size of the "H-value". A large H-value will indicate that one of the groups differs meaningfully from the other groups (in this case publishers). If any stand out, I can create a boxplot to determine which publisher stands out, thus rejecting the NULL. If I have a small H-value and a P-value > .05, I will have failed to reject the NULL hypothesis. 

2. Audience

This research will be valuable to book lovers who are looking to find quality books between different publishers. If my hypothesis is correct, they will be able to choose from a large selection of publishers without worrying about a significant difference in book quality. 

Potential authors would also find this study valuable when determining which publisher to use for their book. They'll know that there isn't a significant difference in quality between publishers, thus allowing them to shop for advantageous publisher rates and fees without worrying that their work will suffer to sell due to a perceived difference in quality for the publisher of their book. 
