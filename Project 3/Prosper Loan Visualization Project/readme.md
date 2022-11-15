# (Prosper Credit Loan)
## by (Shoh Chama Anderson Abi-Ache)


## Dataset

> This data set contains information on peer to peer loans facilitated by credit company Prosper. There are 113,937 loans with 81 variables. For the purpose of this investigation I've taken the following 13 variables: 'Term', 'LoanStatus', 'BorrowerAPR', 'ProsperScore', 'ListingCategory (numeric)', 'EmploymentStatus', 'EmploymentStatusDuration', 'IsBorrowerHomeowner', 'DebtToIncomeRatio', 'StatedMonthlyIncome', 'LoanOriginalAmount', 'LoanOriginationDate', 'MonthlyLoanPayment'


## Summary of Findings

> - Prosper started their business in 2005. They had only 22 loans in 2005. The number of loans increased until 2008 where it dropped drastically from 11552 loans to 2047 loans in 2009. Then the loan steadily increases from 2010 with a record high number of loans in 2013. Then it reduces drastically in 2014
> - The Borrowers annual percentage rate distribution appears to be multimodal. The loan amounts are mostly right skewed with different several peaks. The most frequently loaned amount is 4,000. The loan terms are split into 3 loan terms of 12 months, 26 months and 60 months with 36 months being the most frequently used term. Most of the Loans have a current status with another substantial amount of loans have been completed. The past due loans are split into 6 groups in respect to the number of days they have exceeded.The most frequently loan category applied for is Debt Consolidation. The distribution of monthly income is right skewed. The most frequent monthly income by borrowers seems to be about 5000 with most stated montly income less than 30000.
> - Borrower Rate is negatvely correlated with the loan original amount. The higher the loan amount obtained the lower the borrowers annual rate percentage. The higher the loan amount the higher the term status given for loan repayment. Borrowers with higher monthly income have higher loan amounts. Borrowers with higher monthly income are able to pay higher monthly loan repayments. The higher the loan amount the higher the monthly repayment amount. It is obvious that borrowers that own homes have more employment history than their counterparts and non-homeowners majorly loaned amounts between the ranges of 0 - 5000 with a max of 30000. While most home owners were spread across different amounts betwwen the range of 5000 and above.
> - The 36 months term loans have borrowers annual rate percentage between 0 - 0.4 with a few outliers going to 0.5, Loans for 60 months term are concentrated more on the higher loan amounts and borrowers APR between 0.1 - 0.35, while the 12 months loan term are majorly for lowe loan amounts with a borrowerAPR between 0 - 0.35. Although, the term didn't have a significant relationship to strentheng the effects on the Borrowers annual rate percentage.
> - The effect of the loan terms on the Monthly loan payment to be paid back depending on loan amount was an interesting find. - For loans that cover only 12 months, the monthly fee tends to be more than the other terms since it is a shorter term. While the loans are more spread across for loan terms of 60 months.



## Key Insights for Presentation

> For this project i focused on the exploration of finding out the factors that have effects on the Borrowers annual rate percentage.

> Firstly, I selceted 13 variables out of the 81 original variables then i start to explore distribution of the variables one by one using histogram plots for the continuous variables and counplots for the discrete and norminal variables.

> For the bivariate analysis, I initially used a correlation map to give a overview of variables that hass any form of correlation with each other. After that i explored those that had a higher correlation than 0.2 to explore their relationships.

> Afterwards, I used a regression plot against the loan amount and the borrowers annual rate percentage as it is the most obvious factor. Then various plots like boxplots, violin plots, barplots to find the relationshio between two variables.

> Lastly,From my findings in the bivariate analysis is determined that the strongest features that affects the Borrowers annaual rate percentage are the LoanOriginalAmount, StatedMonthlyIncome and the MonthlyLoanPayment.

> This will all be shown in the presentation.
