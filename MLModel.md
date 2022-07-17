### Data Prepocessing
Not much data prepocessing was necessary for this set of data. The data was retrieved from the SQL database using 'psycopg2' and placed into a Pandas DataFrame. The data was then split into a training set and a test set.

### Feature Engineering
As this was a dataset with only 2 features (time, and population in thousands) those were the two features used. A time-series analysis model was used so both columns, the value and time, were necessary.

### Training/Testing Split
The dataset used had 32 rows. A train/test ratio of ~80/20 was used as that ratio is usually regarded as a generally good starting split. In this case, the last 7 entries were used as the testing set.
