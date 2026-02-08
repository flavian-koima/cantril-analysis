Cantril Ladder Wellbeing Analysis (2011–2021)
 
 Project Overview

This project analyses the relationship between life satisfaction (Cantril ladder score) and key socio-economic indicators using real-world global datasets.

The goal is to identify which factors are most strongly associated with reported wellbeing.
_________________________________________________________________________________________________
 Data Sources

GDP per capita

Homicide rate

Life expectancy

Cantril ladder score (wellbeing)

All datasets were cleaned, aligned by country and year, and merged into a single analysis-ready file.
_______________________________________________________________________________________________________
Tools & Technologies

-Bash scripting

-awk, sort, join

-Linux command-line tools

-Statistical correlation (Pearson’s r)
____________________________________________________
Workflow

1. Validate and clean raw datasets

2. Filter observations (2011–2021)

3. Merge datasets by country and year

4. Compute correlations with Cantril ladder scores

5. Identify the strongest predictor of wellbeing

📈 Key Findings

GDP per capita and life expectancy show positive correlations with wellbeing

Homicide rate is negatively correlated with life satisfaction

Life expectancy emerged as the strongest overall predictor


How to run:
   bash data_cleaning.sh gdp.tsv homicide.tsv life_expectancy.tsv
   bash correlation_analysis.sh cleaned_data.tsv
_________________________________________________________________________

-
My project did two main things:

🔹 Part A: Data cleaning & integration (Bash + awk)

From the second script:

Took three datasets:

GDP per capita

Homicide rate

Life expectancy

Ensured:

Files were tab-separated

Column counts were consistent

Data was filtered to years 2011–2021

Unnecessary columns (e.g. Continent) were removed

Sorted datasets by:

Country

Year

Merged all datasets into one clean, aligned dataset using join

👉 Result: a single, clean dataset ready for analysis
This is real data engineering, not beginner stuff.

🔹 Part B: Statistical analysis (correlation with Cantril ladder)

From the first script:

Used awk to compute Pearson correlation coefficients

Compared Cantril ladder scores against:

GDP per capita

Population

Homicide rate

Life expectancy

Calculated:

Correlation per predictor

Mean correlation

Automatically identified the best predictor of wellbeing.
👉 Result: identified which socio-economic factor best explains life satisfaction.
