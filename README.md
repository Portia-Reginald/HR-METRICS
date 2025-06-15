# HR-METRICS ANALYSIS

## Project Overview

This project presents an in-depth analysis of key Human Resource (HR) metrics within an organization. It aims to provide actionable insights into employee dynamics such as satisfaction, promotion eligibility, warnings, tenure, work-life factors etc — all critical for HR decision-making and workforce planning.

The primary goal is to empower HR teams with data-driven insights to:

1. Track employee satisfaction and readiness for promotion.
2. Understand warning patterns and tenure distribution.
3. Identify potential areas for intervention or improvement.
4. Make smarter, faster HR decisions backed by visuals.

## Dataset Information

**Source:** _Collected for educational analysis._

This dataset captures a wide range of HR-related factors used to assess employee experience, satisfaction, and organizational dynamics. It supports exploration into areas such as promotion readiness, job level, income patterns, work-life balance, employee tenure etc.

The dataset consists of **1,471** rows and **20** columns, each representing employee-level data points across multiple experience markers.

**Key Column Overview:**

- **Age** – The age of the employee.
- **Attrition** – Whether the employee has left the company (Yes/No).
- **BusinessTravel** – Frequency of business travel (e.g., Rarely, Frequently, Non-Travel).
- **Department** – The department the employee works in (e.g., Sales, HR, R&D).
- **DistanceFromHome** – Distance (in kilometers/miles) between the employee’s home and workplace.
- **EmployeeNumber** – Unique identifier for each employee.
- **Gender** – Gender of the employee (Male/Female).
- **JobInvolvement** – Degree of involvement or commitment the employee has toward their job (1–4).
- **JobLevel** – Level or rank of the employee within the organization (1-5).
- **JobRole** – Specific job title or role (e.g., Sales Executive, Research Scientist).
- **JobSatisfaction** – Employee’s satisfaction level with their job (1 = Low, 4 = Very High).
- **MaritalStatus** – Marital status of the employee (Single, Married, Divorced).
- **MonthlyIncome** – Monthly income of the employee.
- **OverTime** – Whether the employee works overtime (Yes/No).
- **TotalWorkingYears** – Total number of years the employee has spent in the workforce.
- **TrainingTimesLastYear** – Number of training programs attended in the past year.
- **WorkLifeBalance** – Employee’s perception of work-life balance (1 = Very low, 4 = Very high).
- **YearsAtCompany** – Number of years the employee has worked at the current company.


## Tools Used

- Microsoft Excel – For data cleaning, formatting, and initial exploration.
  - [Need this? Click to download Microsoft Excel.](https://microsoft.com)

- Power Query – For shaping, transforming, and merging data.

- Power BI – For visual modeling, interactive dashboards, and storytelling.
  - [Need this? Click to download Power BI.](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads)

## Project Objectives

Understand the Demographic Distribution of Employees
➤ To analyze employee age, gender, marital status, department, and job level in order to understand the workforce structure and diversity.

Assess Job Satisfaction and Related Experience Metrics
➤ To examine employee satisfaction ratings (job satisfaction, relationship satisfaction, involvement, work-life balance) and how they vary across departments and roles.

Identify Employees Due for Promotion
➤ To detect staff who have stayed long in their current roles or haven’t been promoted recently and may be ready for advancement.

Flag Potential Retrenchment Risks
➤ To identify patterns such as low job satisfaction, long commute, or overtime work that may indicate burnout or disengagement.

Track Overtime and Work-Life Balance
➤ To explore the distribution of overtime work and its correlation with work-life balance and job satisfaction.

Enable Dynamic Filtering Through Interactive Slicers
➤ To provide HR decision-makers with filters (age group, distance, overtime, promotion readiness, retrenchment risk) to allow for customized exploration of employee insights.

Support Data-Driven HR Decisions Through Clear Visualizations
➤ To build a visually intuitive and interactive dashboard that makes it easy to spot trends, compare groups, and make strategic HR decisions.

## Data Cleaning & Preparation

Before any analysis could begin, the raw dataset required thorough cleaning and transformation to make it usable and reliable. 

Below are the key steps I took:

- Column Separation in Excel
  - The original dataset had all values merged into a single column. Using Text to Columns (Alt + A + E), I separated the data into appropriate individual columns for proper structuring.

RAW                                                                    |  PROCESSED          
:--------------------------------------------------------------------: | :----------------------------------------------------------------------------------:
 ![](RawData.jpg)                                                      |   ![](Separated.jpg)

- Duplicate Check
  - I scanned the dataset for duplicate records and ensured only unique entries were retained to prevent skewed insights.

- Font & Formatting Standardization
  - I ensured consistency in data presentation by standardizing font types and sizes, which helped with clarity during analysis.

- Power Query Transformations
I imported the dataset into Power Query for more structured cleaning:

  - Renamed Columns: Adjusted column names for clarity and consistency.
    
  - Replaced Values: Used the Replace Values function to improve interpretability. For instance, changing numeric values in worklife balance ratings to descriptive labels like “Low,” “High” etc.
    
  - Filtered Out Irrelevant Data: Removed null values and any columns not relevant to the analysis.
    
  - Changed Data Types: Ensured that numerical fields (e.g., Age, MonthlyIncome) and categorical fields (e.g., Department, Gender) were assigned the correct data types.
    
  - Created Custom Columns:
    To enhance the insights from the dashboard, I wrote custom DAX formulas to create calculated columns that grouped continuous variables into more interpretable categories. These included:
    
      - Age Grouping – Categorized employees into age bands (e.g., 18–30, 31–50, etc.).
        
      - Distance Bands – Grouped employee travel distances into Close 0-10, Moderate 10-20, and Far 21-30 ranges.
        
      - Years at company – Oragnized numeric ratings (1–40) into categories (e.g., 0-5 years, 6-10years etc.)
        
      - Job Level & Work-Life Balance Tiers – Reorganized internal rating scales into understandable segments for quicker comparisons.
      
        A DAX Formula I used Example:

        ![](Dax.jpg)

These engineered features made the visualizations easier to interpret and more aligned with real-world business categories.

## Data Analysis and Visualizations

![](Metrics.jpg)

![](Metrics2.jpg)

## 📊DATA ANALYSIS & VISUALIZATION

This analysis explores key workforce metrics such as age distribution, job satisfaction, job level, distance from home, overtime workload, and employee readiness for promotion or retrenchment. Using Power BI, I built interactive dashboards with slicers and logic-based categories to allow stakeholders to explore the workforce from multiple dimensions.

Explore the insights from my dashboard below:

[HR_METRICS_PROJECT.pbix](https://github.com/Portia-Reginald/HR-METRICS/blob/main/HR_METRICS_PROJECT.pbix)

👥 Workforce Demographics & Distribution

Total Employees: 1,470

Gender: 60% Male (882), 40% Female (588)

Marital Status:

Married: 673

Single: 470

Divorced: 327
This indicates a gender imbalance, which may be a point of attention for diversity efforts.Gender imbalance and marital status variations may affect flexibility needs, benefits planning, and retention priorities.
🧓 Age Distribution
The workforce was grouped into three age categories:

18–30 years: 386 employees (26%)

31–50 years: 941 employees (64%)

51–60 years: 143 employees (10%)

🔎 Insight:
The majority of the workforce (64%) falls within the 31–50 age bracket, indicating an experienced and potentially mid-to-senior level population. The smaller 18–30 group suggests room for improved early-career hiring or retention strategies.

