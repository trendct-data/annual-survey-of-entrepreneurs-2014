# output/* files

### states_* pivots

The root level docs starting with states_ show data tables generated at the state level, one-line per state and D.C. The raw data includes multiple rows per state, which makes a lot of analysis difficult. I pivoted out key rows into columns relating to certain topics, ending: _sex.csv _race.csv and _years_in_business.csv

### output/multi/*

I had to combine dimensions to answer a question: How do minority and women owned businesses change as a proportion of overall businesses in the same age group? I only used the Connecticut tables for my story, but I generated the same table for every state and D.C.

There are six files per state: Three topics (age, sex and veteran status of owner), and 2 tables for each topic ("nominal" and percentage).

The files are named [STATE]_[TOPIC]_mulit_[nom/pct].csv. Example: Alabama_RACE_GROUP.display-label_multi_nom.csv

The columns are self explanatory for the most part. However, it's important to note that the percentage columns, prefixed PCT_, refer to each row's portion of the column, not the row. So, Alabama_RACE_GROUP.display-label_multi_pct.csv can be read as, "80% of Alabama businesses newer than two years old are white-owned" NOT TO BE CONFUSED WITH "80% of all businesses are white-owned."

### Re-bucketed data

The below files compare each state based solely on the age of business stock, but not using the Census-defined age buckets and instead look at business ages in five and 10-year buckets.

* /output/states_5_y_buckets.csv
* /output/states_10_y_buckets.csv



# Source files

Source files from the Census Bureau can be found ../data of this repo.