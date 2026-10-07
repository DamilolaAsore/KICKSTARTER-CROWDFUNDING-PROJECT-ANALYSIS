# KICKSTARTER-CROWDFUNDING-PROJECT-ANALYSIS
An Excel data analytics project analyzing Kickstarter crowdfunding projects from 2009 to 2018. The dataset covers project categories, countries, funding goals, pledged amounts, backers, and outcomes to uncover insights into success rates, funding performance, category trends, and country-level project success.
Table of Content
•	Project Overview
•	Project Scope
•	Business Objective
•	Document Purpose
•	Use Case
•	Data Source
•	Dataset Overview
•	Data Cleaning and Processing
•	Data Analysis and Insight
•	Recommendation
•	Conclusion

•	Project Overview
This project analyzes Kickstarter crowdfunding projects from 2009 to 2018 using Excel. The dataset contains over 375,000 rows covering projects across different categories, subcategories, and countries, with information on campaign goals, pledged amounts, number of backers, launch and deadline dates, and project outcomes.
The analysis focuses on understanding crowdfunding project performance by examining success rates across categories, goal completion performance, success rates across years, and project characteristics associated with successful outcomes.
Excel was used throughout the project for data cleaning, transformation, analysis, and visualization, with PivotTables used to summarize the data and support the analysis.



•	Project Scope
The scope of this project includes:
	Time Period: Analysis of Kickstarter project data covering 2009 to 2018.
	Project Focus: Kickstarter crowdfunding projects across different categories, subcategories, and countries.
	Funding Focus: Project funding goals, pledged amounts, goal completion percentage, and number of backers.
	Project Outcome: Analysis of project states, including Successful, Failed, Cancelled, Live, and Suspended projects.
	Key Variables: Project ID, project name, category, subcategory, country, launch date, deadline, goal, pledged amount, backers, and project state.

Analysis:
	Evaluating project success rates across different categories.
	Identifying categories with higher and lower numbers of successful projects.
	Comparing project success rates across years.
	Identifying project characteristics and types associated with successful crowdfunding outcomes.
	Using Excel Pivot Tables to summarize and visualize findings.
	Generating insights that can help understand patterns in crowdfunding project success and funding performance


•	Project Objective
The project aims to:
	Analyze and compare project success rates across categories and years to identify patterns in crowdfunding outcomes.
	Evaluate funding performance by comparing project goals with pledged amounts and calculating goal completion percentages.
	Identify project characteristics and types associated with successful crowdfunding outcomes.
	Generate data-driven insights that improve understanding of Kickstarter project performance and factors that may contribute to successful campaigns.


•	Document Purpose
The purpose of this document is to provide a clear record of the Kickstarter data analytics project documenting the processes and decisions made throughout the analysis. It covers the data cleaning and preparation steps, analytical approach, Excel PivotTables, calculations, findings, interpretations, and key insights generated from the Kickstarter dataset.
The document serves as a reference for understanding how the analysis was conducted and provides a structured record of the methods and results used to evaluate project success and funding performance.

•	Use Case
The findings from this analysis can be used by:
	Kickstarter Project Creators: To understand success patterns across categories and assess funding performance when planning future crowdfunding projects.
	Entrepreneurs and Project Planners: To identify project types and characteristics associated with successful crowdfunding outcomes.
	Crowdfunding Analysts: To evaluate trends in project success, funding goals, pledged amounts, and backer participation.
	Investors and Backers: To better understand project categories, funding performance, and historical success patterns when evaluating crowdfunding projects.
	Marketing and Business Professionals: To gain insights into crowdfunding performance that can support campaign planning and engagement strategies.

•	Data Source
The dataset utilized for this analysis was obtained from Maven Analytics Website, a reputable online platform known for providing data analytics training, resources, and practice datasets. Maven Analytics offers a wide range of datasets across various domains, allowing users to enhance their analytical skills through hands-on experience with real-world data.

•	Dataset Overview
The Kickstarter dataset contains over 375,000 crowdfunding project records covering the period from 2009 to 2018. Each record represents an individual Kickstarter project and provides information about the project, its category and subcategory, location, funding target, funding received, backer participation, campaign dates, and project outcome.
The dataset contains 11 fields.
ID – Internal Kickstarter project identifier
Name – Name of the project
Category – Main project category
Subcategory – Specific project type within the category
Country – Country of the project
Launched – Date the project was launched
Deadline – Crowdfunding campaign deadline
Goal – Funding amount required in USD
Pledged – Amount pledged by backers in USD
Backers – Number of people who supported the project
State – Project outcome or current condition as of January 2, 2018


•	Data Cleaning and Processing

1. Initial Data Assessment: The Kickstarter dataset was initially reviewed in Excel to understand its structure, size, fields, and overall data quality before analysis.
The dataset contained over 375,000 project records covering the period from 2009 to 2018 and included 11 columns; ID, Name, Category, Subcategory, Country, Launched, Deadline, Goal, Pledged, Backers, and State.
The initial assessment focused on identifying missing values, duplicate records, invalid or unusual values, and inconsistencies that could affect the accuracy of the analysis.

2. ID Validation: The ID column was checked for missing and duplicate values to ensure that each project could be uniquely identified.
Total records: 374,847
Blank IDs: 0 
Duplicate IDs: 0
No missing or duplicate ID values were identified. Therefore, no changes were required to the ID column.

3. Category, Subcategory, and Country Validation: The Category, Subcategory, and Country columns were reviewed to identify missing or blank values that could affect category-level, subcategory-level, and geographical analysis.
Category: No blank values identified.
Subcategory: No blank values identified.
Country: No blank values identified.
Since all three fields contained values for the project records, no records were removed or modified based on missing Category, Subcategory, or Country values.

4. Date Validation and Processing: The Launched and Deadline columns were checked to ensure that the dates were properly formatted and suitable for analysis. The date fields were reviewed for blank values and invalid entries, and no issues were identified.
To support time-based analysis, four additional columns were created from the Launched date:
