# Exploring chocolate bar Ratings
Explorative analysis (using Python Pandas, in a Jupyter notebook) of chocolate bars, prepared for class 5007.
* Data reference https://www.kaggle.com/rtatman/chocolate-bar-ratings

## Hypotheses worth exploration 
___
* Lower cocoa content yield (or correlate with, rather) higher ratings
* More recent chocolates are better chocolates (evident through high ratings in more recently published ratings)
* Brand affinity is independent of bean origin (check for consistent ratings per brand, albeit bean origin variation)

### Worth further exploration 
* Data validitiy exploration (test-retest reliability test); checking the proportionality of REF (a value indicative of recentness of data entry) with the ReviewData. This check does not detemrine an ultimate reliability indicator, but could be worth considering if outliers arise. 

___
## Observations
___
* **Overview** The dataset hosts 3 numerical dimensions (before transforming Cocoa Percent into a fourth quantified dimension). 
    - The REF is a metric of data entry recentness, where larger values indicate a more recent data entry (ranging from 5 to 1952). 
    - Review dates indicate the year of review's publication. Half of the chocolates' reviews were published during 2013 to 2017. The oldest review in this dataset dates back to 2006. The average year is around 2012.
    - The Rating column ranges from 1 to 5 ([more details on rating scale found here](https://www.kaggle.com/rtatman/chocolate-bar-ratings)). 25% of ratings are under approximately 2.9/5, while half the 50th percentile (median) is just over 3/5 (3.25). Very few chocolates seem to converge towards the 4-5 rating, given that the 75th percentile is 3.5/5.

* **Fig.1: Box plot for cocoa percentage among rated chocolate bars** The Cocoa percent interquartile range (of rated chocolates) is 70-75%, with both the median and 25th percentile being 70%, suggesting this as a standard for fine chocolates (at least those rated). There are a number of outliers, around 448 bars (25% of 1795 total reviews = 448.75), that have a lower Cocoa percent however.

* **Fig.2.1: Cocoa percentage distribution (bins = 10)** The rated chocolate bars' cocoa distribution has an overall normal distribution, suggesting a fairly populous data sampling (with 1795 ratings). The central tendency (namely, mean) around 71.7%, which is fairly relative to the median of 70%, indicating a predominantely (70%) dark chocolate sampling.

* **Fig.2.1: Cocoa percentage distribution (bins = 35)** On a closer inspection however, it is clear that the ratings, while having an overall normal distribution, cluster heavily at the central bin (~70-71% cocoa) with occaisonal spikes in higher/lower cocoa percentages. This further emphaises the boxplot, where most chocolates rated are 70% cocoa.

### Exploring outlier cocoa percentages
* **Overview:** When looking into the outlier cocoa percentages of under 70%, we find 328 rated chocolate bars. The ratings' publication dates range from 2006 to 2016, with an approximate standard deviation of 3 years. Ratings range from 1.5 to 4, with a central tendancy (both a mean and median) of approximately 3.2. 

    - Outliers with lighter cocoa content suggest higher ratings overall, given the higher quartile values. This suggestion is affirmed through the non resistant metric, the mean, where darker cocoa rankings yield around 2.96 average rating, and lighter cocoa rankings yield an approximate rating of 3.19.

* **Fig. 3.1: Box plot for outlier cocoa percentages (< 70%)** and **Fig.  3.2: Box plot for outlier cocoa percentages (> 75%)** show less outliers outside the interquartile range, where most cocoa percentages reside within 61-67% and 79-85% respectively. This highlights how, even in the case of outliers, most chocolates rated had a relatively high cocoa content (the overall dataset's minimum cocoa content is 42%, and maximum is 100%).

* **Fig. 4: Outlier cocoa percentage distribution** The distribution highlights how most outlier cocoa percentages still cluster around the overal ratings' central tendencies, where extreme values tend to be more rare (with exceptions, such as 100% cocoa) 

___
* **Fig. 5: Box plot for review dates** The interquartile range covers a five-year data sampling with 75% of the ratings being published after 2010; whereas the entire review date range covers 11 years (2006 to 2017). This, as well as the second histogram in **Fig. 6**, showcase a skewing towards more recent years, potentially increasing the data's relevance today.

* **Fig. 6: Comparing REF metric and Review Dates** There seems to be far more data entry points than there are unique review publication years. This may reflect multiple reviews per year, or accumulated data entry points. Given the lack of mapping functionality with the REF metric however, not much can be assumed from this metric. 
___
* **Fig. 7: Ratings box plot** The median rating is 3.25, while (from earlier descriptive statistics) the overall mean is around 3.19. This central tendency similarity is mirrored in an overall bell-shaped curve in **Fig. 8** indicating overall ratings distribution. There tends to be some spikes however around the interquartile range. 
___

* **Correlation between Ratings and Cocoa Percent:** Most Cocoa Percentage values tend to be in the 60-80% range, lower values have always lead to middle ratings (2.5-3)
___
* **Correlation between Review Year and Rating:** Earlier ratings (years 2006-2008) showcase a wider range, where ratings as low as 1, or as high as 5, were present. Most recent ratings on the other hand reflect a far more naunced range. As illustrated in the box plot, and shown in the desriptive statistics that follow, ratings after 2016 ranged from 2.5 to 3.75 with a mere standard deviation of 0.33. 
