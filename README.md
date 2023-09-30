# Group Project 4: Understanding and predicting the triggers for Employee Turnover

Objective: Understand the reasons that employees are leaving Company XYZ, and the actions that may be implemented by the HR department to improve employee retention (if any).

Data Source: https://www.kaggle.com/code/keithvincentburca/salifort-motors-hr-analytics/notebook
The CSV dataset provides information about 14999 employees.
The dataset provides information about 14999 employees.

Target variable:
“left” - Employee Left the Company (yes=1, no=0)

Possible features (variable) for consideration:
* “satisfaction_level” – Employee-reported job satisfaction level (value between 0 and 1)
* “last_evaluation” – Average score of employee’s last performance review (value between 0 and 1) 
* “number_project” – Number of projects employee contributes to
* “average_monthly_hours” – Average number of hours employee worked per month
* “time_spent_company” – Number of years (tenure) employee has been with the company
* “work_accident” – Whether an employee experienced an accident while at work (yes=1, no-0)
* “promotion_last_5years” – Whether an employee was promoted in the last 5 years (yes=1, no=0)
* “department” – Employee’s department (one of 10 departments)	
* “salary” – Employee’s salary level (categories - low, medium, high)

## The project consists of three parts.

The first part of this project uses pandas in jupyter notebook to import libraries, read in the dataset, clean the data, generate charts and csv files, then exports the files into an output folder.  Seaborn is utilized to create bar charts for turnover based on salary, turnover based on department, the number of projects held versus departures, company tenure versus departures, and company salaries by department.  After generating comparison tables, dummy variables were created along with a correlation matrix to assist in identifying the proper model for machine learning.

The second part uses tableau visual analytics platform to analyze different facets of the dataset and discover/reveal any further trends for employee retention and departures.

The third part of the project uses Google Colab for machine learning to predict the factors for employee retention and departures.

Please, use the jupyter notebook file to read in the csv file, which is located in the Resources folder.

The Resource folder contains the following:
* employee_data.csv

The output_data folder contains the following:
* Fifteen files in csv format
** CSV file labeled employee_data_5 contains clean headers and includes an employee_id
* Seven bar/pie charts in png format

## Initial Findings

After cleaning the data 3,008 duplicate items were discovered; however, the team decided to keep the data for machine learning purposes.

## Turnover Findings for Department and Salary

Preliminary analysis reveals of the 14,999 records 76.2% of individuals remain with the company and 23.8% of the individuals departed the company. There are 5,144 low incomed salaries with 2,172 departing the company.  Of the 5,129 Medium salaried employees, 1,317 departed the company.  High salaried employees retained 1,155 employees with 82 departing the company.

![employee_quit_stayed_pie](https://github.com/todd-petruska/group-project-4/assets/128247739/316f136c-16d1-4f0c-a6a8-d758cb944d4a)

* Low salary: 5,144 stayed, 2,172 departed
* Medium salary: 5,129 stayed, 1,317 departed 
* High salary: 1,155 stayed, 82 departed


![Turnover_Based_on_Salary](https://github.com/todd-petruska/group-project-4/assets/128247739/fe336e1e-b059-427f-8356-7f33020cb18b)


Sales is the largest department with 3,126 employees with 1,014 departing the company and management is the smallest with 539 employees with 91 departing the company.

## Findings

The bar chart revealed the Sales department with the highest count of departures (1,014); however, the overall highest percentage occurred in the HR department with 29.09% departures (215), followed by Accounting with 26.60% departure rate.  The Management department is best overall in retention with 14.44% departures (91). 

* Hr = 29.09%
* Accounting = 26.60%
* Engineering = 25.63%
* Support = 24.90%
* Sales = 24.49%
* Marketing = 23.66%
* IT = 22.25%
* Product_mng = 21.95%
* R&D = 15.37%
* Management = 14.44%

The Salary category with the highest company departure rate is in the Low salary range with 29.68% departures followed by the Medium salary range with 20.43% departures.

Salary Range Departures:
* Low = 29.68%
* Medium = 20.43%
* High = 6.62%

Data revealed 100% of employees handling seven projects (256) departed the company followed by 65.61% employees handling only two projects (1,567).

Number of Projects Departures:
* Seven = 100.00%
* Two = 65.61%
* Six = 55.79%
* Five = 22.16%
* Four = 9.36%
* Three = 1.78%

The highest number of departures from the company occurs at Five years with a 56.55% departure rate (833), whereas employees with over Seven years with the company are unlikely to depart.

* Number of Years at Company Departures:
* Five = 56.55%
* Four = 34.80%
* Six = 29.10%
* Three = 24.61%
* Two = 1.63%
* Seven = 0.00%
* Eight = 0.00%
* Ten = 0.00%



