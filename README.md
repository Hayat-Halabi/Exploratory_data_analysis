# Exploratory_data_analysis (EDA)

Exploratory Data Analysis in SQL is all about digging into the data using queries to see what’s really going on. It helps me understand the dataset, find interesting patterns, and spot anything unusual. While exploring, I usually clean up the data too fixing missing values or inconsistencies so it’s ready for deeper analysis later on.

I'll be working with the cleaned data from [data_cleaning_with_sql](https://github.com/Hayat-Halabi/data_cleaning_with_sql/tree/main) project to perform further exploration and analysis.

I'm kicking off this analysis by looking at companies that had a 100% layoff on a single day. I found 43 entries with various sizes, and it looks like the largest company among them was the construction firm, KATERRA.
![image alt](https://github.com/Hayat-Halabi/Exploratory_data_analysis/blob/main/ss10.png?raw=true)

Next, I wanted to take a closer look at companies that had the highest cumulative number of total layoffs across the whole timeline. This query shows the largest and most significant companies that have cut the most staff overall:
```sql
SELECT company, SUM(total_laid_off)
FROM layoffs2
GROUP BY company
ORDER BY 2 DESC;
``` 
![image alt](https://github.com/Hayat-Halabi/Exploratory_data_analysis/blob/main/ss11.png?raw=true)
