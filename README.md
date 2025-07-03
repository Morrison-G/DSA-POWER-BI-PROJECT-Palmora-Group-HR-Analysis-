# DSA-POWER-BI-PROJECT-Palmora-Group-HR-Analysis-
This Power BI work on Palmora Group HR case study aims to reduce issues on gender inequality like gender pay gap and possible issues by identifying key areas that could raise issues in the business. Key features are: Clean Data, and Visual charts to support business decision making.
## Project Overview
> This case study analyses Gender inequality in distribution, pay gap and salary structure in Palmora group company. It also identifies employees that has left the company, department no longer functional and removed from the dataset.

## Tool Used
> Power BI Desktop(Power BI Tool, visual charts).

## Data Cleaning Actions
> Some data cleaning steps were applied to make the dataset proper for analysis without errors.
## Steps
> ### Gender: created a generic for blank rows using (replace value).
> ### Department: removed rows with NULL using (Filter).
> ### Salary: removed blank rows using (remove rows in home tab).

> ## Key Business Questions Answered
Gender Distribution Analysis
1. Create a bar chart:
    - Axis: Region/Department
    - Value: Count of Employees by Gender
      
2. Use a slicer to filter by region/department.
   
3. Visualize the overall gender distribution using a pie chart.
   
4: Minimum Salary Requirement Analysis
4a 1. Create a histogram:
    - Axis: Salary Band ($10,000 increments)
    
    - Value: Count of Employees
    
2. Use a slicer to filter by region.
   
3. Calculate the number of employees below the minimum salary threshold.
   
4b Visualization:
- Histogram: "Salary Distribution by $10,000 Band"
- Bar chart: "Employees Below Minimum Salary Threshold by Region"
  
Measures
- `Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])`
  
5: Bonus Payment Calculation

1. Create a measure to calculate the bonus amount based on performance ratings.
   
2. Calculate the total amount to be paid to individual employees (salary + bonus).
   
3. Create a bar chart to visualize the total amount to be paid out per region.
   
Visualization:

Bonus Payments

- Bar chart: "Total Bonus Payout by Region"
  
- Table: "Individual Employee Bonus Payments"

Measures

- `Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)`
  
- `Total Amount to be Paid = 'Employee'[Salary] + 'Bonus Amount'`
