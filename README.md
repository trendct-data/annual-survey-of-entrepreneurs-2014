# Annual survey of entrepreneurs, 2014

This is new data from the U.S. Census Bureau. It supplements the
every-five-years "Survey of Business Owners" and adds a new data point, the age
of businesses in years of operation.

# Files

* Annual survey of entrepreneurs.ipynb - Python analysis
* data/* - Raw data and metadata from the Census Bureau, used in the analysis file above
* output/* - Sheets generated as output in the analysis script meant to be useful either to other researchers or for making charts for my own stories

# output/* files

### states_* pivots

The root level docs starting with states_ show data tables generated at the state level, one-line per state and D.C. The raw data includes multiple rows per state, which makes a lot of analysis difficult. I pivoted out key rows into columns relating to certain topics, ending: _sex.csv _race.csv and _years_in_business.csv

### output/multi/*

I had to combine dimensions to answer a question: How do minority and women owned businesses change as a proportion of overall businesses in the same age group? I only used the Connecticut tables for my story, but I generated the same table for every state and D.C.

There are six files per state: Three topics (age, sex and veteran status of owner), and 2 tables for each topic ("nominal" and percentage).

The files are named [STATE]_[TOPIC]_mulit_[nom/pct].csv. Example: Alabama_RACE_GROUP.display-label_multi_nom.csv

The columns are self explanatory for the most part. However, it's important to note that the percentage columns, prefixed PCT_, refer to each row's portion of the column, not the row. So, Alabama_RACE_GROUP.display-label_multi_pct.csv can be read as, "80% of Alabama businesses newer than two years old are white-owned" NOT TO BE CONFUSED WITH "80% of all businesses are white-owned."

