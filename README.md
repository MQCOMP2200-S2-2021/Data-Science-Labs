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

# Portfolio 3
## Data
## Important packages
```import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import OneHotEncoder
from sklearn.model_selection import train_test_split
from sklearn import linear_model
from sklearn.metrics import r2_score
import seaborn as sns
%matplotlib inline
```
## Summary
