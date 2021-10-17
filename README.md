# Data Science Portfolio

This repository contains the files for the Portfolio task for COMP2200/6200 in S2 2021. There are a total of 3 portfoliow with their own individual tasks. All packages have ben updated as of 15/10/21. Throughout the portfolios there are references to resources that have been used for topics that are not taught in class. 

# Portfolio 1
## Data
We’re provided with a dataset from a cyclist doing 4 different races. 2 races are from 2016 and the other two are from 2019. One of the races from each year is a time trial race and the other is a road race. The difference between the time trial and road race is one is a solo race trying to beat a time and the other is with a group of racers. 

We can appreciate the recording device is not perfect and can expect some errors. 

## Important packages
```import gpxpy
import gpxpy.gpx
from gpxutils import parse_gpx 
import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn import linear_model
from sklearn.metrics import r2_score
import seaborn as sns
from datetime import datetime
```
## Summary
After exploring the data we find that the time trial race covers about half the distance the road race covers and takes less time. These differences in the races must be considered throughout the analysis. 
Some of the goals set for this project are as follows: 
-	Are there instances where one race is faster than the other? 
-	How do the speeds compare in the races? 
-	Determine the development of the rider throughout the race. 


There is an attempt to use a simple linear regression model as extra work. The idea was to see if it is possible to use this model to determine where and how the rider can improve certain aspects of the ride to achieve better times. 

# Portfolio 2
## Data
We're provided with a dataset from the state governments of SA and QLD which has the number of voucher claims per LGA and another dataset which describes the scocioeconomic status of the LGAs. The sports voucher can be retrieved from [here for SA](https://data.gov.au/dataset/ds-sa-14daba50-04ff-46c6-8468-9fa593b9f100/details), [here for QLD](https://data.gov.au/dataset/ds-qld-3118838a-d425-48fa-bfc9-bc615ddae44e/details?q=get%20started%20vouchers) and the SEIFA data retrieved from the [ABS SEIFA data by LGA](http://stat.data.abs.gov.au/Index.aspx?DataSetCode=ABS_SEIFA_LGA#).
## Important packages
```import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn import linear_model
from sklearn.metrics import r2_score
import seaborn as sns
```

## Summary
setting up the dataframes we begin to look at some important questions of the data. These questions include: 
* Describe the distribution of vouchers by: LGA, Sport - which regions/sports stand out? 
* Are some sports more popular in different parts of the state?
* Are any electorates over/under represented in their use of vouchers?
* Is there a relationship between any of the SEIFA measures and voucher use in an LGA?
* Can we perform a comparable analysis between QLD and SA? 

We were able to discover the LGAs with the most and least amount of claims, the most popular and least popular sports. We were able to further break these down by considering the different claim rates of the top sports within the top LGAs, to get an idea of how the voucher claims vary. 

We also looked at comparing the SEIFA scores between QLD and SA as we hypothesise this would be a good indicator for the likeliness an LGA makes a claim. 

# Portfolio 3
## Data
We're provided with a dataset that mimics real data from a telecommunications company. The data represents information gathered from the customer about various features such as what type of handset they use, whether they're in a lock in contract and most importantly whether they are no longer receiving any service from the company (churn).

## Important packages
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import OneHotEncoder
from sklearn.model_selection import train_test_split
from sklearn import linear_model
from sklearn.metrics import r2_score
from sklearn.metrics import confusion_matrix, accuracy_score
from sklearn.feature_selection import RFE
from sklearn.linear_model import LogisticRegression
from sklearn.naive_bayes import GaussianNB
from sklearn.datasets import make_classification
import warnings
```
## Summary
We're first set out to explore the dataset to see if we can spot any potential relationships between th features and whether a customer churns. Afterwards, we use an logistic regression model with specified features to make the predictions. Afterwards, we compare the accuracy of the first model with that of a model that uses recursive feature selection (RFE). This function does the work for us to determine the most successful features. We also tried a Naive Bayes approach, though it is inconclusive as we require more support from tutors (via consultations) to fully understand how to implement it. 
