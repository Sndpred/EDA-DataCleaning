**Tech Layoffs 2022–2023: Data Cleaning and EDA with SQL**

This project involves data cleaning and exploratory data analysis (EDA) on global tech layoffs using SQL. The goal is to prepare raw data for meaningful analysis and uncover trends in layoffs across industries, companies, and time.
**Dataset**

    Source: Kaggle - Layoffs 2022

    Description: Public dataset covering global tech layoffs from 2020 to 2023, including fields like company, location, total laid off, percentage laid off, stage, and funds raised.

**Data Cleaning Highlights**

To prepare the dataset for EDA, the following cleaning steps were performed in SQL:

    1. Removed Duplicate Records
    Used ROW_NUMBER() and partitioning logic to identify and delete true duplicates while preserving valid repeated entries (e.g., multiple layoffs by the same company).

    2. Standardized Inconsistent Entries

        Unified inconsistent labels (e.g., "Crypto Currency" → "Crypto").

        Cleaned trailing characters (e.g., "United States." → "United States").

    3. Handled Missing and Blank Values

        Replaced blank entries with NULL.

        Imputed missing industry values using self-joins on company.

    4. Date Formatting

        Converted date field from text to SQL DATE type using STR_TO_DATE().

    5. Removed Non-Actionable Rows

        Deleted records where both total_laid_off and percentage_laid_off were NULL, as they offered no analytical value.

**Key Insights from EDA**
    Largest Layoffs by Company
    Amazon had the highest total layoffs over the period, followed by companies like Meta and Google.

    High-Impact Layoffs (100%)
    Several startups, such as Quibi and BritishVolt, laid off 100% of their workforce, indicating shutdowns.

    Industries Most Affected
    The Retail, Consumer, and Crypto sectors had the highest number of layoffs.

    Geographic Trends
    The United States accounted for the majority of layoffs, followed by India and the United Kingdom.

    Layoff Patterns Over Time
    Layoffs peaked in late 2022 and early 2023, with a steady upward trend observed from mid-2022.


**Tools & Skills Used**
    SQL (MySQL syntax)

    CTEs, Window Functions, Aggregations, Joins

    Data Cleaning Techniques

    Exploratory Data Analysis (EDA)
