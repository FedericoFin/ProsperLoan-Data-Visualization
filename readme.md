# Effects of Borrower Characteristics on Loan Conditions and Loan Outcome - Prosper Loan Case Study
## by Federico Finetti


## Dataset

The dataset analyzed was originally composed by 81 details (columns) of 113937 Loans (rows). 
The dataset can be found [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1554486256021000), with feature documentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).

In the analysis the focus is on 12 columns: 
* 3 main features of interest: *ProsperRating (numeric)*, *BorrowerRate* and *LoanStatus*
* 9 additional features: *DebtToIncomeRatio*, *StatedMonthlyIncome*, *IncomeVerifiable*, *Term*, *EmploymentStatus*, *EmploymentStatusDuration*, *AmountDelinquent*, *DelinquenciesLast7Years* and *Recommendations*

In this analysis, I wanted to investigate how the Borrower characteristics (such as debt/income ratio, monthly income, emplyment status, number of delinquencies and their amount) affected the Rating given by the Company, the Loan conditions (*borrower rate*) and ultimately the Loan Outcome (*LoanStatus*).

From the original dataset, approximately 37,000 records were removed because duplicates or with missing values. 
Also other 51,700 records were removed because still ongoing (*Current* status), therefore without a conclusive outcome. These rows would have been non-value-added in understanding how good the risk evaluation strategy of the company is, as there isn't the *label* stating whether or not the borrower was able to pay the debt back.


## Summary of Findings

From the Univariate Exploration, I discovered that the Rating was normally distributed, as well as the Borrower Rate. 
*"Current"* was by far the most frequent Loan Status, then there were *"Completed"* and *"Chargedoff"* on the top of the frequencies. 
*"Employed"* was by far the most frequent Employment Status. After removing the *"Current"* Loan statuses, remained only one record for *"Not employed"* and *"Self-employed"* statuses.

In the Bivariate Exploration, I found out that the *ProsperRating* was directly correlated to the positivity of the *LoanStatus* and strongly negatively to the *BorrowerRate*. Consequently, the *BorrowerRate* appeared inversely correlated to the positivity of the *LoanStatus* and positively correlated to the *ProsperRating*.

With regard to the Monthly Income, this shows a strong positive correlation to the *ProsperRating*, and negative with the *BorrowerRate*. Vice-versa for the *DebtToIncomeRatio*.

From the *EmploymentStatus* vs *ProsperRating* analysis, I discovered that the rating increases if the borrower is employed by a company over if he is self-employed or retired, and if the employee works full-time over if he works part-time.

Also I found out that the higher is the *AmountDelinquent* and the *DelinquenciesLast7Years*, the lower is the rating. Also, the higher the number of delinquencies, the higher is the amount delinquent.

The additional discoveries found during the Multivariate Exploration were that the debt/income ratio is strongly related to the Rating for the *"Employed"* and *"Employed"* Employment Statuses, and up to a vlue of 0.8. Apart from that the relation is weaker. Also the zone with the highest Rating is for Retired, Part-timers, Full-timers and Employed up to a maximum of 0.2 debt/income ratio.
Very similar pattern but with opposite signs between the Borrower Rate and the Rating.



## Key Insights for Presentation

For the presentation, I focused on the stongest relations, leaving out most of the weaker or meaningless ones.

I started by introducing the relation between the tree main features of interest through a chromatic point-plot, showing the strong negative correlation between the Rating and the Borrower rate, as well as the negative correlation between the Borrower rate and the Loan Status.

Using heat-maps,I showed then how the Employment Status and the Debt/Income Ratio impacted the Prosper Rating and the Borrower Rate. I highlighted that the hypotesized patterns (as the Employment Status becomes more stable and the Debt/Income Ratio decreases, the Rating increases and the Borrower Rate decreases) are stronger for the *"Employed"* and *"Employed"* statuses (and as they are more numerous, that also had an impact on the overall) and up to 0.8 debt/income ratio.

Using a 3-Dimensional scatter plot I showed that both the Amount Delinquent and the Number of Delinquencies in the previous 7 years are negatively related to the Prosper Rating, and that the number of delinquencies and their amount are positively related.

Finally, the last heat-map displays the breakdown of the Stated Monthly Income by Employment Status and Loan Status, showing that the more stable the employment status is, the higher is the average income, except for the part-timers, as they work fewer hours. And again another overall pattern (positive correlation between the positivity of the outcome and the income) is not consistent through the different employment statuses, as it seems mainly due to the *"Employed"* status being the one with the majority of the data-points.