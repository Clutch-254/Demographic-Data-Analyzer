# Demographic Data Analyzer

A Python script that analyzes demographic data from the 1994 Census database to answer some interesting questions about income, education, and work patterns.

## What It Does

This analyzer crunches through census data to find patterns and answer questions like:

- How does education level affect earning potential?
- Which countries have the highest percentage of high earners?
- What's the relationship between work hours and income?
- What occupations are most common among high earners in different countries?

## Requirements

- Python 3.x
- pandas library

Install dependencies:
```bash
pip install pandas
```

## Data Source

The script expects a file called `adult.data.csv` with census data including:
- age
- sex
- education level
- occupation
- hours worked per week
- native country
- salary (categorized as ≤50K or >50K)
- race

## Usage

```python
from demographic_analyzer import calculate_demographic_data

# Run with printed output
calculate_demographic_data()

# Run without printing (just return the dictionary)
results = calculate_demographic_data(print_data=False)
```

## What Gets Analyzed

**Race Distribution** - Shows how many people of each race are in the dataset

**Average Age of Men** - Calculates the mean age for male respondents

**Education Levels** - Finds what percentage of people have Bachelor's degrees

**Education vs Income** - Compares earning potential between those with advanced education (Bachelors, Masters, or Doctorate) and those without

**Work Hours** - Identifies the minimum hours worked per week and what percentage of minimal workers earn over 50K

**Geographic Analysis** - Determines which country has the highest percentage of people earning over 50K

**Occupation Insights** - Finds the most popular occupation for high earners in India

## Output Format

The function returns a dictionary with all calculated values and also prints them in a readable format:

```
Number of each race:
 White                 27816
Black                  3124
Asian-Pac-slander     1039
...

Average age of men: 39.4
Percentage with Bachelors degrees: 16.4%
Percentage with higher education that earn >50K: 46.5%
...
```

## Notes

- All percentages are rounded to 1 decimal place
- "Higher education" is defined as having a Bachelors, Masters, or Doctorate degree
- The salary threshold of >50K is from 1994, so adjust your expectations accordingly!
- The script preserves the original data - nothing gets modified

## Use Cases

This is great for:
- Learning pandas data manipulation
- Understanding how to analyze demographic datasets
- Exploring socioeconomic patterns in census data
- Practice with data filtering, grouping, and aggregation

Feel free to modify the analysis or add your own questions! The data has plenty more insights waiting to be discovered.
