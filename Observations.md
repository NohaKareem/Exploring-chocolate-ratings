# Exploring chocolate bar Ratings
Explorative analysis (using Python Pandas) of chocolate bars, prepared for class 5007.
* Data reference https://www.kaggle.com/rtatman/chocolate-bar-ratings

## Hypotheses worth exploration 
* Lower cocoa content yield (or correlate with, rather) higher ratings
* Brand affinity is independent of bean origin (check for consistent ratings per brand, albeit bean origin variation)

### Worth further exploration 
* Data validitiy exploration (test-retest reliability test); checking the proportionality of REF (a value indicative of recentness of data entry) with the ReviewData. This check does not detemrine an ultimate reliability indicator, but could be worth considering if outliers arise. 

## Observations
* **Fig.1: Cocoa Percent stand deviation among rated chocolate bars** The Cocoa percent interquartile range (of rated chocolates) is 70-75%, with both the median and 25th percentile being 70%, signaling this as a standard for fine chocolates. There are a number of outliers, around 448 bars (25% of 1795 total reviews = 448.75), that have a lower Cocoa percent however.

* **Fig.2: Cocoa Percent distribution** The Cocoa percent interquartile range (of rated chocolates) is 70-75%, with both the median and 25th percentile being 70%, signaling this as a standard for fine chocolates. There are a number of outliers, around 448 bars (25% of 1795 total reviews = 448.75), that have a lower Cocoa percent however.

* **Correlation between Ratings and Cocoa Percent:** Most Cocoa Percentage values tend to be in the 60-80% range, lower values have always lead to middle ratings (2.5-3)
