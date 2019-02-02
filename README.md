# Communicate Data Findings 

#### Table of Contents

1. [Installation](#Installation)
2. [Project Motivation](#ProjectMotivation)
3. [File and Data Descriptions](#FileDescription)
4. [Results](#Results)
5. [Licensing, Authors and Acknowledgements](#Licensing)

###  Installation
<a name="installation"></a>

The libraries used in the project are as follows:

- NumPy
- pandas
- Matplotlib
- Seaborn

### Project Motivation
<a name="ProjectMotivation"></a>

The visualizaton analysis is done to find an answer to 2 questions. They are;

1. What affect the interest rate borrower is charged with?
2. Is there any differences between large and small loans, if any, how large 
loans are different from small loans in terms of terms, interest rate and/or
orher variables.

### Data and File Description
<a name="FileDescription"></a>

Dataset contains 113,937 loans with 81 variables on each loan, including loan
amount, borrower rate, loan original amount, borrower income and many others.
For the project, I take a subset of features which is 17 variables out of 81
variables. The data is from  https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv.

The final data including new variables that I use in exploratory and 
explanatory analysis is saved and named as clean_data.csv.

In the exploratory and explanatory analysis, I use interest rate, borrower's 
rate and borrower rate interchangeably. Similarly, I use credit risk score, 
Prosper Score, risk score, credit score interchangeably.

The files in the folder are;

exploratory.ipynb - includes exploratory data analysis 

exploratory.html - html page of EDA

explanatory.ipynb - includes explanatory data analysis

clean_data.csv - csv file including cleaned data

output-toggle.tpl - file to make it possible to hide code cells and only 
display visualizations in the output cells when creating a slide deck


### Results
<a name="Results"></a>

#### Exploratory Analysis

I look at the bivariate and multivariate relationships between borrower's rate
and other variables to find an answer to the first question. When I cannot see
an obvious relationship, I do not include that part in explanatory analysis. 
Term and credit score are important for borrower's rate. So I try to account 
for these effects in the visualizations.

Since I include many variables in the project, there are many visualizations 
that can be put into explanatory analysis.

Generally I start with what I think the most appropriate plot for the
variables. If the relationship is not obvious or the plot is not good at 
revealing it, I try another kind of plot and include what I think the best 
one(s) revealing the relationships.

Main findings from exploratory analysis are as follows: The price the 
borrower pays for the loan (borrower's rate) decreases as

- credit risk score of the borrower increases (for different term values)
stated monthly income increases,

- the debt to income ratio falls,

- the number of current credit lines increases up to 10, after this value 
there is no clear correlation

- the loan original amount increases

- the term of the loan decreases when the credit score is greater than 6. 
For scores smaller than 6, borrower's rate decreases as term increases from 36 months to 60 months

- the number of inquiries in the last 6 months decreases.

Large loans are different from smaller loans in terms of

- Loans with a large original loan amount have a longer term; while small 
loans have 12 months term, large loans have 36 or 60 months terms.

- While small loans can be of any value, large loans are mostly multiples of
 5k, ie. 10k, 15k, 20k, 25k..

- For each term value, the price of the loan gets smaller as the loan amount increases. So large loans generally have smaller interest rates compared to smaller loans.

- The stated monthly income of borrowers who can take out large loans are 
larger compared to those of borrowers who take smaller loans

- Larger loans require good credit scores. For instance, borrower needs to 
have a credit score of at least 5 to get a loan of 30k or 35k.

- The debt to income ratios of borrowers who get larger loans are generally 
lower compared to those who get smaller loans.



### Licensing, Authors and Acknowledgements
<a name="Licensing"></a>

MIT License
