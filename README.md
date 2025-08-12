# HR Analytics Dashboard

![HR Analytics Dashboard Title](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/About%20Dashboard.png)



## Overview

This repository contains an HR Analytics Dashboard built to visualize and analyze employee data from a company dataset. The dashboard focuses on key HR metrics such as employee count, attrition rates, total experience, training times, job satisfaction, salary distribution, and more. It uses visualizations like bar charts, funnel charts, area charts, and tabular views to provide actionable insights for HR decision-making.

The dataset includes 1,470 employee records with attributes like age, education, job role, department, attrition status, salary, performance ratings, and work experience. The dashboard is divided into multiple pages: 
- **About Dashboard**: Introduction and purpose.
- **Employee Count Data**: Breakdowns by department, job role, age band, and overtime.
- **Salary Data**: Salary distributions by department, job role, and education.
- **Tabular Data**: Summarized views of job roles with metrics like attrition count, promotion periods, and training times.

Prepared by Kanika Jain using tools like Power BI (based on the visual style and DAX measures mentioned in the dashboard description).

## Purpose

The goal of this dashboard is to help HR teams:
- Identify trends in employee attrition and retention.
- Analyze workforce distribution across departments and roles.
- Evaluate training investments and their distribution.
- Assess salary structures and job satisfaction levels.
- Support data-driven strategies for talent management and development.

## Dataset Summary

The underlying data is from an HR employee dataset (similar to the IBM HR Analytics Employee Attrition & Performance dataset). Key columns include:
- Employee Count
- Attrition (Yes/No)
- Business Travel
- Age Band
- Department (R&D, Sales, HR)
- Education Field
- Gender
- Job Role
- Marital Status
- Over Time
- Training Times Last Year
- Age
- Daily Rate
- Education
- Job Involvement
- Job Level
- Job Satisfaction
- Monthly Income
- Monthly Rate
- Percent Salary Hike
- Performance Rating
- Total Working Years
- Years at Company
- Years in Current Role
- Years Since Last Promotion
- Years with Current Manager

Total employees: 1,470  
Total attrition: 237 (approximately 16.1% attrition rate)  
Departments: R&D (961 employees), Sales (446), HR (63)  

## Key Visualizations

Here are some of the main charts from the dashboard:

### 1. Sum of Total Experience by Department
![Sum of Total Experience by Department](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/Department%20by%20total%20experience.png)


- R&D: Highest total experience (~11,000 years), indicating a more seasoned workforce.
- Sales: ~5,000 years.
- HR: ~700 years.

### 2. Sum of Training Times Last Year by Department
![Sum of Training Times Last Year by Department](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/Count%20by%20Department.png)


- R&D: Highest training investment (~2,800 sessions).
- Sales: ~1,270 sessions.
- HR: Lowest (~200 sessions).

### 3. Count of Employees by Department
![Count of Employees by Department](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/Count%20by%20Department.png)


- R&D dominates with 961 employees (65% of total).
- Sales: 446 employees (30%).
- HR: 63 employees (4%).

### 4. Employee Count Page
![Employee Count Dashboard Page](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/Employee%20count%20data.png)


- Attrition by department: R&D has the highest count (~140), followed by Sales (~90), HR (~5).
- Job roles: Sales Executive is the most common, followed by Research Scientist and Laboratory Technician.
- Age bands: Majority in 25-34 and 35-44 groups.
- Gender split: 60% Male, 40% Female.
- Overtime employees: 416.

### 5. Salary Data Page
![Salary Data Dashboard Page](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/Employee%20salary%20data.png)


- Total yearly salary: ₹30,941,200.
- Average monthly income: ~₹6,503.
- Salary by department: R&D highest due to employee volume.
- Highest yearly rate: ₹233.9K; Lowest: ₹25K.
- Salary distribution by job role and education: Higher roles like Managers have higher salaries; advanced education correlates with better pay.

### 6. Tabular Data Summary
![Tabular Data](https://github.com/Jainkanika09/HR-Analytics-Dashboard/blob/main/Tabular%20data.png)


A summarized table by job role, satisfaction, involvement, performance, and department:
- Total Attrition Count: 237
- Sum of Last Promotion Period: 3,216 years
- Sum of Training Times Last Year: 4,115 sessions

Example rows (partial):
- Laboratory Technician (Satisfied, Medium Involvement): Attrition 10, Promotion Period 74, Training 97 (R&D).
- Sales Executive (Satisfied, Medium Involvement): Attrition 8, Promotion Period 103, Training 140 (Sales).

## Key Insights from Analysis

1. **Department Imbalance**: R&D is the largest department with 65% of employees, the most experience, and the highest training investment. This suggests R&D is a core focus area, but Sales and HR may need more resources to balance growth.

2. **Attrition Trends**: Overall attrition rate is 16.1%. R&D has the highest absolute attrition (due to size), but rates are similar across departments (~15-20%). Factors like overtime (28% of employees) and low job involvement may contribute—employees with "Yes" attrition often have higher travel and overtime.

3. **Training Distribution**: Total training sessions last year: 4,115. R&D received ~68% of training, potentially leading to better performance but highlighting underinvestment in Sales and HR, which could affect retention.

4. **Experience and Tenure**: Average total working years ~11. Employees in R&D have longer tenure (average ~11.5 years) compared to Sales (~11 years) and HR (~11 years). High experience in R&D correlates with lower relative attrition.

5. **Salary and Satisfaction**: Average monthly income ₹6,503, with hikes averaging 15%. Job satisfaction is generally medium-high, but dissatisfied employees show higher attrition. Higher education (Master's/Doctoral) links to higher salaries and roles.

6. **Demographics**: 60% male, 40% female. Age distribution skews younger (majority under 44), with under-25 having higher attrition. Marital status: Married employees have lower attrition.

These insights can guide HR strategies, such as targeted training for Sales/HR, retention programs for high-attrition roles, and diversity initiatives.

## Installation and Usage

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/hr-analytics-dashboard.git
   ```

2. Open the dashboard file (e.g., `HR_Analytics_Dashboard.pbix` if using Power BI) or view the Excel data in `HR Data - Dashboard.xlsx`.

3. To reproduce analysis:
   - Use Power BI or Excel for visualizations.
   - For custom analysis, import the data into Python (e.g., with pandas):
     ```python
     import pandas as pd

     df = pd.read_csv('hr_data.csv')  # Assuming exported CSV
     print(df.groupby('Department')['Total Working Years'].sum())
     ```

## Technologies Used

- Power BI (for dashboard creation and DAX calculations)
- Excel (for raw data)
- Visualizations: Bar charts, stacked bars, funnels, slicers, cards

## Future Improvements

- Add predictive analytics for attrition using machine learning (e.g., logistic regression).
- Integrate real-time data sources.
- Expand to include diversity metrics and employee engagement surveys.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

Prepared by Kanika Jain. For questions, reach out via GitHub issues.
