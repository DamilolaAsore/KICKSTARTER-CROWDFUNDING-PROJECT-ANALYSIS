# KICKSTARTER-CROWDFUNDING-PROJECT-ANALYSIS

An Excel data analytics project analyzing Kickstarter crowdfunding projects from 2009 to 2018. The dataset covers project categories, countries, funding goals, pledged amounts, backers, and outcomes to uncover insights into success rates, funding performance, category trends, and country-level project success.


## Table of Content

-	Project Overview
-	Project Scope
-	Business Objective
-	Document Purpose
-	Use Case
-	Data Source
-	Dataset Overview
-	Data Cleaning and Processing
-	Data Analysis and Insight
-	Recommendation
-	Conclusion

##	Project Overview

This project analyzes Kickstarter crowdfunding projects from 2009 to 2018 using Excel. The dataset contains over 375,000 rows covering projects across different categories, subcategories, and countries, with information on campaign goals, pledged amounts, number of backers, launch and deadline dates, and project outcomes.
The analysis focuses on understanding crowdfunding project performance by examining success rates across categories, goal completion performance, success rates across years, and project characteristics associated with successful outcomes.
Excel was used throughout the project for data cleaning, transformation, analysis, and visualization, with PivotTables used to summarize the data and support the analysis.



##	Project Scope

The scope of this project includes:
-	Time Period: Analysis of Kickstarter project data covering 2009 to 2018.
-	Project Focus: Kickstarter crowdfunding projects across different categories, subcategories, and countries.
-	Funding Focus: Project funding goals, pledged amounts, goal completion percentage, and number of backers.
-	Project Outcome: Analysis of project states, including Successful, Failed, Cancelled, Live, and Suspended projects.
-	Key Variables: Project ID, project name, category, subcategory, country, launch date, deadline, goal, pledged amount, backers, and project state.

### Analysis:

-	Evaluating project success rates across different categories.
-	Identifying categories with higher and lower numbers of successful projects.
-	Comparing project success rates across years.
-	Identifying project characteristics and types associated with successful crowdfunding outcomes.
-	Using Excel Pivot Tables to summarize and visualize findings.
-	Generating insights that can help understand patterns in crowdfunding project success and funding performance


##	Project Objective

The project aims to:

-	Analyze and compare project success rates across categories and years to identify patterns in crowdfunding outcomes.
-	Evaluate funding performance by comparing project goals with pledged amounts and calculating goal completion percentages.
-	Identify project characteristics and types associated with successful crowdfunding outcomes.
-	Generate data-driven insights that improve understanding of Kickstarter project performance and factors that may contribute to successful campaigns.


## Document Purpose

The purpose of this document is to provide a clear record of the Kickstarter data analytics project documenting the processes and decisions made throughout the analysis. It covers the data cleaning and preparation steps, analytical approach, Excel PivotTables, calculations, findings, interpretations, and key insights generated from the Kickstarter dataset.
The document serves as a reference for understanding how the analysis was conducted and provides a structured record of the methods and results used to evaluate project success and funding performance.

##	Use Case

The findings from this analysis can be used by:

-	Kickstarter Project Creators: To understand success patterns across categories and assess funding performance when planning future crowdfunding projects.
-	Entrepreneurs and Project Planners: To identify project types and characteristics associated with successful crowdfunding outcomes.
-	Crowdfunding Analysts: To evaluate trends in project success, funding goals, pledged amounts, and backer participation.
-	Investors and Backers: To better understand project categories, funding performance, and historical success patterns when evaluating crowdfunding projects.
-	Marketing and Business Professionals: To gain insights into crowdfunding performance that can support campaign planning and engagement strategies.

##	Data Source

The dataset utilized for this analysis was obtained from Maven Analytics Website, a reputable online platform known for providing data analytics training, resources, and practice datasets. Maven Analytics offers a wide range of datasets across various domains, allowing users to enhance their analytical skills through hands-on experience with real-world data.

##	Dataset Overview

The Kickstarter dataset contains over 375,000 crowdfunding project records covering the period from 2009 to 2018. Each record represents an individual Kickstarter project and provides information about the project, its category and subcategory, location, funding target, funding received, backer participation, campaign dates, and project outcome.

The dataset contains 11 fields.

- ID – Internal Kickstarter project identifier
- Name – Name of the project
- Category – Main project category
- Subcategory – Specific project type within the category
- Country – Country of the project
- Launched – Date the project was launched
- Deadline – Crowdfunding campaign deadline
- Goal – Funding amount required in USD
- Pledged – Amount pledged by backers in USD
- Backers – Number of people who supported the project
- State – Project outcome or current condition as of January 2, 2018


##	Data Cleaning and Processing

**1. Initial Data Assessment:** The Kickstarter dataset was initially reviewed in Excel to understand its structure, size, fields, and overall data quality before analysis.
The dataset contained over 375,000 project records covering the period from 2009 to 2018 and included 11 columns; ID, Name, Category, Subcategory, Country, Launched, Deadline, Goal, Pledged, Backers, and State.
The initial assessment focused on identifying missing values, duplicate records, invalid or unusual values, and inconsistencies that could affect the accuracy of the analysis.

**2. ID Validation:** The ID column was checked for missing and duplicate values to ensure that each project could be uniquely identified.

- Total records: 374,847
- Blank IDs: 0 
- Duplicate IDs: 0
- No missing or duplicate ID values were identified. Therefore, no changes were required to the ID column.

**3. Category, Subcategory, and Country Validation:** The Category, Subcategory, and Country columns were reviewed to identify missing or blank values that could affect category-level, subcategory-level, and geographical analysis.

- Category: No blank values identified.
- Subcategory: No blank values identified.
- Country: No blank values identified.
  
Since all three fields contained values for the project records, no records were removed or modified based on missing Category, Subcategory, or Country values.

**4. Date Validation and Processing:** The Launched and Deadline columns were checked to ensure that the dates were properly formatted and suitable for analysis. The date fields were reviewed for blank values and invalid entries, and no issues were identified.

To support time-based analysis, four additional columns were created from the Launched date:

### New Columns and Excel Formulas


| New Column | Excel Formula |
|---|---|
| Launched Year | `=YEAR(F2)` |
| Launched Month Name | `=TEXT(F2,"MMMM")` |
| Launched Month Number | `=MONTH(F2)` |
| Launched Day Name | `=TEXT(F2,"DDDD")` |
| Deadline Year | `=YEAR(K2)` |
| Deadline Month Name | `=TEXT(K2,"MMMM")` |
| Deadline Month Number | `=MONTH(K2)` |
| Deadline Day Name | `=TEXT(K2,"DDDD")` |



The formulas were filled across the dataset. The resulting date fields contained no blank values or errors. The Launched Year field showed that the projects covered the period from 2009 to 2018, which was used for the analysis of project success across years.

**5. Goal Validation:** The Goal column was reviewed to ensure that project funding targets were available and suitable for analysis.

- Blank Goal values: 0
- Highest Goal value: $166,361,391
- Goal values equal to $0: 4 records

The four projects with a $0 Goal were identified and recorded as unusual values because a zero-funding target does not provide a meaningful basis for calculating funding performance or goal completion percentage. The remaining Goal values were retained for analysis.



**6. Pledged Amount Validation:** The Pledged column was reviewed for missing, negative, and zero values.

- Blank Pledged values: 0
- Negative Pledged values: 0
- Zero Pledged values: 51,802

The zero-pledged records were further reviewed by examining their project states. The records included projects with states such as Live, Suspended, Canceled, and Failed. Since projects with no pledged funding cannot provide meaningful information for the funding performance and goal completion analysis, the 51,802 zero-pledged records were removed from the analysis dataset. All remaining Pledged values were retained for analysis.


**7. Backers Validation:** The Backers column was reviewed to identify missing and negative values and to ensure that the number of backers was suitable for analysis.

- Blank Backers values: 0
- Negative Backers values: 0
- Zero Backers values: Present

Zero values were retained because a project having no backers is a valid observation and does not, by itself, indicate that the data is incorrect. No records were removed or modified based on the Backers column.


**9. State Validation:** The State column was reviewed to identify the different project outcome categories and ensure that the values were suitable for analysis.

The dataset contained the following project states:

Successful
Failed
Canceled
Live
Suspended

The State values were retained because each represents a distinct project condition and can provide useful information for analyzing project outcomes. No records were removed or modified based on the State column.





**10. Final Dataset Validation**
    
A final validation was performed after completing the cleaning and processing steps to ensure that the dataset was ready for analysis.
The final checks confirmed that;

-	374,847 records were present in the original dataset.
-	51,802 records with zero Pledged amounts were removed.
-	The ID column contained no blank or duplicate values.
-	Category, Subcategory, and Country contained no blank values.
-	The Launched and Deadline fields contained no identified blank or invalid values.
-	The Goal column contained no blank values.
-	The Pledged column contained no blank or negative values after cleaning.
-	The Backers column contained no blank or negative values.
-	The State column contained valid project outcome categories.

The cleaned dataset was then used for the analysis and PivotTable stage of the project.


##	Data Analysis and Insight

**Analysis Question 1:**

## Which project category has the highest success percentage, and how many successful projects does it have?

The first analysis examined the success rate of Kickstarter projects across different project categories. The purpose was to determine which category had the highest proportion of successful projects and to understand how the number of successful projects differed across categories.

PivotTable Setup

A PivotTable was created in Excel using the cleaned Kickstarter dataset.

| PivotTable Area | Field |
|---|---|
| Rows | Category |
| Values | ID – Count |
| Columns | State |


The Category field was placed in the Rows area to group the projects by category. The State field was placed in the Columns area to separate projects according to their outcomes: Canceled, Failed, Live, Successful, and Suspended. The ID field was added to the Values area and summarized using Count. This provided the number of projects within each category and each project state.

The PivotTable contained 374,846 project records across the listed categories and states.

- Success Percentage Calculation: To determine the success rate for each category, the number of successful projects was compared with the total number of projects in that category.
  
Success Percentage = Successful Projects ÷ Total Projects × 100
For example, the Dance category had 2,338 successful projects out of 3,767 total projects:
2,338 ÷ 3,767 × 100 = 62.07%
This calculation was applied across all categories.


### Category Performance Results

| Category | Total Projects | Successful Projects | Success Percentage |
|---|---:|---:|---:|
| Dance | 3,767 | 2,338 | 62.07% |
| Theater | 10,911 | 6,534 | 59.88% |
| Comics | 10,819 | 5,842 | 54.00% |
| Music | 49,529 | 24,105 | 48.67% |
| Art | 28,149 | 11,508 | 40.88% |
| Film & Video | 62,691 | 23,612 | 37.66% |
| Games | 35,225 | 12,518 | 35.54% |
| Design | 30,064 | 10,549 | 35.09% |
| Publishing | 39,377 | 12,300 | 31.24% |
| Photography | 10,778 | 3,305 | 30.66% |
| Food | 24,599 | 6,085 | 24.74% |
| Fashion | 22,812 | 5,593 | 24.52% |
| Crafts | 8,809 | 2,115 | 24.01% |
| Journalism | 4,754 | 1,012 | 21.29% |
| Technology | 32,562 | 6,433 | 19.76% |





![](https://github.com/DamilolaAsore/KICKSTARTER-CROWDFUNDING-PROJECT-ANALYSIS/blob/main/Kickstarter%20Pictures/Kickstarter%20Success%20Percentage%20by%20Category.png)









#### Analysis: The analysis shows considerable variation in success percentages across Kickstarter categories.

-	Dance recorded the highest success percentage at 62.07%, meaning that 2,338 of its 3,767 projects were classified as successful. This was followed by Theater at 59.88% and Comics at 54.00%.

-	Music recorded 24,105 successful projects, making it one of the categories with the largest number of successful projects. However, its success percentage was 48.67%, which was lower than Dance, Theater, and Comics. This demonstrates that the number of successful projects and the success percentage measure different aspects of project performance.

-	At the other end of the results, Technology had the lowest success percentage at 19.76%, with 6,433 successful projects out of 32,562 total projects. Journalism had a success percentage of 21.29%, while Crafts, Fashion, and Food recorded success percentages between approximately 24% and 25%.

-	The results therefore show that categories with a larger number of projects do not necessarily have the highest success percentage. For example, Film & Video had 23,612 successful projects, but its success percentage was 37.66%, while Dance had only 2,338 successful projects but a much higher success percentage of 62.07%.
  

#### Key Insight

The analysis indicates that success rates varied substantially by project category. Dance had the highest proportion of successful projects in the dataset, while Technology had the lowest. The comparison also highlights the importance of considering both success percentage and absolute number of successful projects when evaluating Kickstarter project performance.


**Analysis Question 2:**

## Which countries have the highest number of successful Kickstarter projects?

The second analysis examined Kickstarter project outcomes across different countries to identify the countries with the highest number of successful projects. The purpose was to understand the geographical distribution of successful Kickstarter projects within the dataset.

PivotTable Setup

A PivotTable was created in Excel using the cleaned Kickstarter dataset.

| PivotTable Area | Field |
|---|---|
| Rows | Country |
| Columns | State |
| Values | ID – Count |

The Country field was placed in the Rows area to group the projects by country. The State field was placed in the Columns area to separate projects according to their outcomes, including Cancelled, Failed, Live, Successful, and Suspended.
The ID field was added to the Values area and summarized using Count to determine the number of projects within each country and project state.

#### Analysis 

-	To answer the question, the Successful column of the PivotTable was examined and compared across countries.
-	The analysis focused on the number of successful projects, rather than success percentage. The countries were therefore compared based on their total count of projects with a Successful state.
-	The successful project counts were then arranged from highest to lowest to identify the top five countries.

### Successful Kickstarter Projects by Country

| Country | Successful Projects |
|---|---:|
| United States | 109,298 |
| United Kingdom | 12,067 |
| Canada | 4,134 |
| Australia | 2,117 |
| Germany | 937 |


The United States recorded the highest number of successful Kickstarter projects, with 109,298 successful projects. The United Kingdom followed with 12,067 successful projects, while Canada recorded 4,134. Australia and Germany completed the top five with 2,117 and 937 successful projects respectively.



![](https://github.com/DamilolaAsore/KICKSTARTER-CROWDFUNDING-PROJECT-ANALYSIS/blob/main/Kickstarter%20Pictures/Top%205%20Countries%20by%20the%20number%20of%20successful%20projects.png)



#### Analysis

-	The results show a substantial difference in the number of successful Kickstarter projects across the countries represented in the analysis.
-	The United States accounted for the largest number of successful projects by a considerable margin, with 109,298 successful projects. This was followed by the United Kingdom with 12,067, meaning that the number of successful projects recorded for the United States was substantially higher than that of the other countries in this comparison.
-	Canada ranked third with 4,134 successful projects, followed by Australia with 2,117 and Germany with 937.
-	The results should be interpreted as counts of successful projects, rather than evidence that projects in one country had a higher probability of success. The number of projects submitted from each country differs considerably, so a country with a larger project volume can naturally have more successful projects.

#### Key Insight

-	The analysis identifies the United States, United Kingdom, Canada, Australia, and Germany as the five countries with the highest numbers of successful Kickstarter projects in the dataset.
-	The United States had by far the largest count of successful projects, while the remaining four countries recorded substantially smaller totals. This provides a clear view of where successful Kickstarter projects were most concentrated geographically within the dataset.
-	For a more complete assessment of country-level performance, the number of successful projects could be considered alongside the total number of projects and success percentage	
	



	
	
**Analysis Question 3:**

## How does the success rate of Kickstarter projects change over the years?

The purpose of this analysis is to examine the success rate of Kickstarter projects across different launch years. This helps identify periods where projects had higher or lower success rates and understand how project success changed over the period covered by the dataset.

##### Analysis

A PivotTable was used to calculate the percentage of projects that reached each Kickstarter state for every launch year.
The PivotTable was configured as follows:

-	Rows: Launched Year 
-	Columns: State 
-	Values: Count of ID 
-	Value Display: % of Row Total 

The State field was retained with all available states:

-	Cancelled 
-	Failed 
-	Live 
-	Successful 
-	Suspended
  
Using % of Row Total allowed the percentage of successful projects to be calculated against the total number of projects launched in each year.
The analysis then focused on the Successful percentage for each year.

### PivotTable Result

| Launched Year | Successful |
|---|---:|
| 2009 | 44.28% |
| 2010 | 44.20% |
| 2011 | 46.40% |
| 2012 | 43.45% |
| 2013 | 43.23% |
| 2014 | 31.56% |
| 2015 | 28.01% |
| 2016 | 33.05% |
| 2017 | 35.16% |
| 2018 | 0.00% |

##### Key Insights

**1. Early years recorded relatively high success rates**

From 2009 to 2013, the success rate remained relatively consistent and stayed above 43%.

-	2009: 44.28% 
-	2010: 44.20% 
-	2011: 46.40% 
-	2012: 43.45% 
-	2013: 43.23%
  
The highest success rate in the dataset's completed years was recorded in 2011 at 46.40%.

**2. Success rate declined significantly between 2013 and 2015**

A substantial decline occurred from 2013 onward.

The success rate decreased from:
43.23% in 2013 → 31.56% in 2014 → 28.01% in 2015
The 2015 success rate of 28.01% was the lowest meaningful annual rate in the analysis.

**3. Success rate began to recover after 2015**

After reaching 28.01% in 2015, the success rate increased in the following two years:

-	2016: 33.05% 
-	2017: 35.16% 
This indicates an increase in the proportion of projects classified as successful during this period.

**4. 2018 should not be interpreted as a normal annual result**

The PivotTable shows 0.00% for 2018. This result should not be interpreted as meaning that no Kickstarter projects were successful in 2018.
The dataset's State information is current as of 2018-01-02, meaning 2018 does not represent a complete year of activity. Therefore, the 2018 value is not directly comparable with the completed years from 2009–2017.




![](https://github.com/DamilolaAsore/KICKSTARTER-CROWDFUNDING-PROJECT-ANALYSIS/blob/main/Kickstarter%20Pictures/Kickstarter%20Project%20Success%20Rate%20by%20Year.png)





##### Chart Interpretation

The line chart shows relatively stable success rates from 2009 to 2013, followed by a noticeable decline between 2013 and 2015.
The lowest point occurs in 2015 at 28.01%. The rate then increases in 2016 and 2017, reaching 35.16% in 2017.

##### Conclusion

The analysis shows that Kickstarter project success rates varied across the years. Success rates were relatively high and stable from 2009 to 2013, reaching a high of 46.40% in 2011. The rate then declined considerably, reaching its lowest meaningful point of 28.01% in 2015, before recovering to 35.16% in 2017.
The 2018 result of 0.00% was not used to assess the annual trend because the dataset contains an incomplete 2018 period.



**Analysis question 4:**

## Which Kickstarter categories receive the highest average amount of money pledged by backers?

#### Purpose of the Analysis

The purpose of this analysis is to compare Kickstarter categories based on the average amount of money pledged by backers. This helps identify the categories where projects receive higher average financial contributions and highlights differences in funding levels across project categories.

#### Analysis

A PivotTable was created to calculate the average amount pledged for each Kickstarter category.

### PivotTable Configuration

| PivotTable Area | Field |
|---|---|
| Rows | Category |
| Values | Pledged – Average |

The Pledged (USD) field was changed from its default Sum calculation to Average using Value Field Settings.
The categories were then sorted from Largest to Smallest based on the average pledged amount.

### PivotTable Result

| Category     | Average Pledged (USD) |
| ------------ | --------------------: |
| Design       |            $24,421.45 |
| Technology   |            $21,070.37 |
| Games        |            $21,043.94 |
| Comics       |             $6,610.45 |
| Film & Video |             $6,218.70 |
| Fashion      |             $5,712.87 |
| Food         |             $5,114.29 |
| Theater      |             $4,006.42 |
| Music        |             $3,911.63 |
| Photography  |             $3,572.23 |
| Dance        |             $3,453.81 |
| Publishing   |             $3,390.82 |
| Art          |             $3,221.43 |
| Journalism   |             $2,615.79 |
| Crafts       |             $1,632.91 |


### Key Insights

**1. Design had the highest average pledged amount**

Design recorded the highest average amount pledged at $24,421.45 per project.
This was the highest average across all 15 Kickstarter categories analyzed.

**2. Technology and Games also recorded high average funding**

Technology ranked second with an average pledged amount of $21,070.37, while Games ranked third with $21,043.94.
Technology and Games were almost identical, with only $26.43 separating their average pledged amounts.

**3. The top three categories were significantly higher than the remaining categories**

The three highest categories were:

### Top 3 Categories by Average Pledged

| Category   | Average Pledged (USD) |
| ---------- | --------------------: |
| Design     |            $24,421.45 |
| Technology |            $21,070.37 |
| Games      |            $21,043.94 |

The next category, Comics, had an average of $6,610.45.
This shows a substantial difference between the top three categories and the remaining categories.

**4. Comics had the highest average among the remaining categories**

After Design, Technology, and Games, Comics recorded the fourth-highest average pledged amount at $6,610.45.
It was followed by:

-	Film & Video — $6,218.70 
-	Fashion — $5,712.87 
-	Food — $5,114.29
  
**5. Crafts recorded the lowest average pledged amount**

Crafts had the lowest average pledged amount at $1,632.91 per project.
This was followed by Journalism at $2,615.79 and Art at $3,221.43.

**6. Overall average pledged amount**

The Grand Total average was $9,121.24.
This provides a benchmark for comparing the average pledged amount of individual categories.




![](

### Chart Interpretation

The visualization clearly shows that Design, Technology, and Games stand out from the other Kickstarter categories in terms of average pledged amount.
Design has the longest bar, confirming that it has the highest average pledged amount. Technology and Games follow closely behind.
There is then a substantial drop to Comics, which is the fourth-highest category. Crafts has the shortest bar, representing the lowest average pledged amount.

### Conclusion

The analysis shows significant differences in the average amount of money pledged across Kickstarter categories. Design recorded the highest average pledged amount at $24,421.45, followed by Technology at $21,070.37 and Games at $21,043.94.
In contrast, Crafts recorded the lowest average pledged amount at $1,632.91. The overall average pledged amount across the categories was $9,121.24.
The results indicate that the level of average financial backing varies considerably across Kickstarter categories, with Design, Technology, and Games receiving substantially higher average pledged amounts than most other categories.



