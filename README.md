# Loan Lending Club Case Study
> Consumer finance company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface. Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

## Table of Contents
* [Data understanding](#general-information)
* [Data cleaning](#technologies-used)
* [Data Analysis](#conclusions)
* [Recommendations](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## Data understanding
- To identify the driving factors, we have analyzed the past loan data for all loans issued through the time period 2007 to 2011. 
- To start with the data analysis, the data set had to be cleaned and prepared for the analysis, then analyzed and visualized.
- Below steps were performed to draw the conclusion 
	1. Columns with more than 50% of null values were dropped. 
	2. Columns like emp_title, url etc were dropped as these columns do not add value to the data analysis. 
	3. Missing values were imputed so that all the NULL and NAN values were removed.
	4. Once the data set was cleaned, univariate, bivariate and mulitvariate analysis were performed 
	5. Visualization techniques were used to draw charts and graphs
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Data cleaning
- Multiple columns with more than 30% of null or missing values were dropped as imputing values to high percentage of missing values is not advisable. Columns like    tot_hi_cred_lim,total_bal_ex_mort,total_bc_limit,total_il_high_credit_limit etc. which had more that 50% of null values were dropped. 
- Descriptive columns like url, employee_title, loan description and idenitity columns like id, employee_id were dropped as these columns do not add value to data analysis. Only columns like loan_status, interest_rate, loan_amount etc were retained using which driving factors could be determined. 
- Default value was imputed to few of the numeric column where values were NAN. Values were imputed keeping in mind that the new values inserted do not adversely impact the data analysis.
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Data Analysis
- In our analysis we are interested only in defaulted loans. 
- Loan_status column was considered to check how many loans were fully paid and how many were defaulted.
- From this analysis, it was inferred that over 30,000 loans were fully paid and just over 5000 loans were defaulted.

- Two columns are analyzed in Bivariate Analysis to visualize the effect of one value on another. 
- Multiple columns were analyzed against loan_status column to visualize the effect of different parameters on defaulting a loan.
- Bar graphs, Histogram, line graphs were used to visualize the data
- Interest rate Vs Loan_status	
1) The effect of Interest rate of the loan, on loan defaulting was analyzed
2) Interest rates were divided in 4 buckets as 5-10, 10-15, 15-20, 20-25  
3) It was inferred that loan with interest rate between 20-25 has the highest chances of defaulting
4) Loans with lower rate of interest between 5-10 has less chances of defaulting.
5) There is a steady growth in the changes of defaulting with increase in interest rate. So higher the interest rate, the more chances of loan getting defaulted.

- Purpose of loan Vs Loan_status	
1) Purpose of loan column was analyzed against loan_status column to visualize loan taken for what purpose are defaulted the most
2) Loans that are taken for 'Small Business' has the highest changes of defaulting
3) There is no significant difference in the chances of defaulting between the other purpose of loans

- Loan_grade Vs Loan_status
1) Loan_grade was analyzed against loan_status column to visualize what grade of loans are bound to default.
2) Loan_grade 'A' is least to default
3) Loan_grade 'F' and 'G' has highest chances of defaulting

- The effect of multiple columns were analyzed against loan_status. 
1) The influence of loan amount and purpose of loan on the status of loan was visualized .
2) The loan amounts were divided into different buckets of 0-5000, 5000-10000, 10000-15000, 15000-20000, 20000-25000, 25000+
3) All the loan that fell into the each bucket were further divided based on the purpose of loan and were plotted
4) Loan with 'Other' Purpose and loan amount greater than 25000 has the highest ration of defaulting.

#### LIBRARIES USED:
- Seaborn & Matplotlib used to visualize and Pandas & Numpy were used for analysis.

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Recommendations
- After the data clean up and analysis, below are few of the insights that were visualized
1) Around 14% of all the loans get defaulted
2) Higher the loan interest rate, higher the chance of loan getting defaulted
3) There is higher chance of loan getting defaulted if the loan is taken for the purpose of ‘Small Business’ or ‘Debt Consolidation’
4) Chances of loan default is more if the income of the borrower is less than 25000 and the loan purpose is ‘Other’.
5) Longer the term higher the Defaulters 
6) Dti_Range, defaulter rate increases with increase in dti ratio.
7) Higher the Grade , higher the Defaulters
8) Lower Income customers are likely to get defaulted

## Contact
Created by [@rajivsimhadri] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
