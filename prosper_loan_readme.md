# The effect of different loan attributes on Prosper's Loans Status outcomes
## by Rujeko Musarurwa


## Dataset

> The loan dataset for Prosper is a large dataset that contains over 100k customer loans information and has 81 different variables such as loan creation date, loan amount, loan status and much more. The aim of this analysis is to assess the data and any relationships that may exist between the different loan attributes.

>  I focused on 12 attributes for this project that I believe will assist the most in the assessing and analyzing of the data.
The final dataset used after data wrangling has 106 219 rows with 12 feautures(the unique listing key for each loan, loan term,loan status,Annual percentage rate(APR), interest rate, state borrower lives in, occupation, monthly income, months since loan was taken, original loan amount, yearly quarter loan was taken up and monthly loan repayment amount). 
There are 7 numerical variables and 5 strings variables. 
>Loan Status is the most interesting feature as it can be used to assess and find out which other features influence the outcome and status of a loan.

>I removed rows with null values because the dataset is large enough for us to remove them and additionally because borrower state and occupation is data we can not fill in with mean or median values I also removed two rows with very large stated monthly income values in excess of usd500k as this variables average is usd5600.
> I would have liked to use credit ratings but credit grade(before 2009) and prosperRating(after july2009) use two different methods that are further complicated by the method used for listing creation date.

> The monthly income and monthly loan repayment variables both had very large values and very small values. I used a square root transform because of the zero values that existed I could not use a log transform.
Under the transformation the monthly income variable is unimodal with a peak at 5000 and the monthly repayments variable is bimodal with peaks at 200 and 400.




## Summary of Findings


### Bivariate relationship findings

> Completed loans not surprisingly have the highest above monthly payments associated with them. Completed loan status also have lowest interest rate assoictaed with them which also assists in people in this category paying up their loans better. High interest rates are prevalent amongst past due and charged off loans which may make sense as to why these loans enter past due status.

> With regards to monthly income, loans in their final payment stages also have the highest average monthly incomes associated with them with default and charged off loans being associated with lowest average monthly incomes. Surprisingly, past due loans have average stated monthly incomes higher than those stated for completed loans.

> Most loan statuses are all associated with an original loan amount of USD4000, but the current loans tend to have original loan values of either USD4000, USD10 000 or USD15 000.

> A relationship between loan status and occupation does seem to exist to some extent but with the major occupation category of 'other' being the most significant it is difficult to really conclude to a relationship. The relationship between state and origination quarter shows that the state of California has overtime taken up the most loans.

### Multivariate relationship findings

> A positive relationship between original loan amount and monthly payment exists and when combined with the loan status variable it can be noted that a much steeper line for completed loans is seen. This implies that for the same original loan amount taken up, completed loan customers paid on average more towards the loan than for the other loan status customers.

> Original loan amount and loan term have a strong positive relationship but have no additional effect on 36 and 60 month term loans when considering loan status. However for 12month loans, the range of orignal loans are very wide with very large original loan amounts associated with 1-30 day past due loan statuses.

> Current and completed loans are associated with lower interest rates but also lower monthly payments.

> Lower original loan amounts are associated with higher interest rates but for completed, chargedoff and defaulted loans the interest rates go higher than 0.33 yet for the other loan statuses, 0.33 is the highest interest rate associated with them.

> Surprisingly, there exists some borrowers with very low monthly payments of around USD200 and average original loan amounts but still have abnormally high interest rates near the maximum of about 0.35.


## Key Insights for Presentation

> The selection criteria I used to decide which results to put in my explanatory analysis was that I looked at the correlation matrix of all the numerical variables and saw that there are some that seem to not have a relationship at all with the other variables and those I did not include. I also did not include the other categorical variables such as occupation and state as they do not seem to have much of an effect on loan status either.

> I decided to look at original loan amount, monthly payment and interest rate and their effects on loan status.

> I named the graph axes and gave them titles and also adjusted the sizes of some graphs.
