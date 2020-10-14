# Exploring chocolate bar Ratings
Explorative analysis (using Python Pandas, in a Jupyter notebook) of chocolate bars, prepared for class 5007.
* Data reference https://www.kaggle.com/rtatman/chocolate-bar-ratings

## Hypotheses worth exploration 
* Lower cocoa content yield (or correlate with, rather) higher ratings
* Brand affinity is independent of bean origin (check for consistent ratings per brand, albeit bean origin variation)

### Worth further exploration 
* Data validitiy exploration (test-retest reliability test); checking the proportionality of REF (a value indicative of recentness of data entry) with the ReviewData. This check does not detemrine an ultimate reliability indicator, but could be worth considering if outliers arise. 

___

## Observations
* **Overview** The dataset hosts 3 numerical dimensions (before transforming Cocoa Percent into a fourth quantified dimension). 
    - The REF is a metric of data entry recentness, where larger values indicate a more recent data entry (ranging from 5 to 1952). 
    - Review dates indicate the year of review's publication. Half of the chocolates' reviews were published during 2013 to 2017. The oldest review in this dataset dates back to 2006. The average year is around 2012, suggesting a skewed year distribution towards older reviews~.
    - The Rating column ranges from 1 to 5 ([more details on rating scale found here](https://www.kaggle.com/rtatman/chocolate-bar-ratings)). 25% of ratings are under approximately 2.9/5, while half the 50th percentile (median) is just over 3/5 (3.25). Very few chocolates seem to converge towards the 4-5 rating, given that the 75th percentile is 3.5/5.

* **Fig.1: Box plot for cocoa percentage among rated chocolate bars** The Cocoa percent interquartile range (of rated chocolates) is 70-75%, with both the median and 25th percentile being 70%, suggesting this as a standard for fine chocolates (at least those rated). There are a number of outliers, around 448 bars (25% of 1795 total reviews = 448.75), that have a lower Cocoa percent however.

* **Fig.2.1: Cocoa percentage distribution (bins = 10)** The rated chocolate bars' cocoa distribution has an overall normal distribution, suggesting a fairly populous data sampling (with 1795 ratings). The central tendency (namely, mean) around 71.7%, which is fairly relative to the median of 70%, indicating a predominantely (70%) dark chocolate sampling.

* **Fig.2.1: Cocoa percentage distribution (bins = 35)** On a closer inspection however, it is clear that the ratings, while having an overall normal distribution, cluster heavily at the central bin (~70-71% cocoa) with occaisonal spikes in higher/lower cocoa percentages. This further emphaises the boxplot, where most chocolates rated are 70% cocoa.

### Exploring outlier cocoa percentages
* **Overview:** When looking into the outlier cocoa percentages of under 70%, we find 328 rated chocolate bars. The ratings' publication dates range from 2006 to 2016, with an approximate standard deviation of 3 years. Ratings range from 1.5 to 4, with a central tendancy (both a mean and median) of approximately 3.2. 

* **Fig. 3.1: Box plot for outlier cocoa percentages**   

* **Fig. 4: Box plot for outlier cocoa percentages (bins = 30)**   

* **Correlation between Ratings and Cocoa Percent:** Most Cocoa Percentage values tend to be in the 60-80% range, lower values have always lead to middle ratings (2.5-3)