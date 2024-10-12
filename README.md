# JPMC Quantitative Research Job Simulation Programme
Conducted and accredited via Forage between July 2024 to Aug 2024
Access program on: https://www.theforage.com/simulations

## Outline
This project is completed under the JP Morgan Chase & Co. Quantitative Research Job Simulation on Forage. There are a total of 4 assigned tasks, including topics in analysing & forecasting, pricing models, credit risk analysis, and FICO scores. Each of the notebook corresponds to the $n$ th task. The Two Excel files "Nat_Gas.csv" and "Task3n4_Loan_Data.csv" are using in Task 1 and Task 3, 4 respectively. While the "Nat_Gas_forecast.csv" is used in Task 2.

The course contains various reading materials, which correspond to the daily work of a quant at JPMC. Besides the code and datasets, all the task instructions are available on my public GitHub repository attached below. Besides the code and datasets, all the task instructions are also marked down within.

I have also taken a further step in some of the tasks by implementing financial models such as Holt-Winters (time series forecasting) and the Logistic Regression module. Which are relatively "advanced" for the requirements of the tasks.

- Notes: The notebooks provided here are for better visual undestanding of the works only. The python code prototype is not being uploaded or shown

## Task 1: Market Forecasting: Forecasting Natural Gas Market Price
After asking around for the source of the existing data, you learn that the current process is to take a monthly snapshot of prices from a market data provider, which represents the market price of natural gas delivered at the end of each calendar month. This data is available for roughly the next 18 months and is combined with historical prices in a time series database.
After gaining access, you are able to download the data in a CSV file. You should use this monthly snapshot to produce a varying picture of the existing price data, as well as an extrapolation for an extra year, in case the client needs an indicative price for a longer-term storage contract.

Download the monthly natural gas price data. Each point in the data set corresponds to the purchase price of natural gas at the end of a month, from 31st October 2020 to 30th September 2024. Analyze the data to estimate the purchase price of gas at any date in the past and extrapolate it for one year into the future. 

Your code should take a date as input and return a price estimate. Try to visualize the data to find patterns and consider what factors might cause the price of natural gas to vary. This can include looking at months of the year for seasonal trends that affect the prices, but market holidays, weekends, and bank holidays need not be accounted for.


## Task 2: Pricing Models: Pricing Natural Gas Contracts
You need to create a prototype pricing model that can go through further validation and testing before being put into production.
Eventually, this model may be the basis for fully automated quoting to clients, but for now, the desk will use it with manual oversight to explore options with the client. 

You should write a function that is able to use the data you created previously to price the contract. The client may want to choose multiple dates to inject and withdraw a set amount of gas, so your approach should generalize the explanation from before. Consider all the cash flows involved in the product.

The input parameters that should be taken into account for pricing are:
Injection dates. 
Withdrawal dates.
The prices at which the commodity can be purchased/sold on those dates.
The rate at which the gas can be injected/withdrawn.
The maximum volume that can be stored.
Storage costs.

Write a function that takes these inputs and gives back the value of the contract. You can assume there is no transport delay and that interest rates are zero.
Market holidays, weekends, and bank holidays need not be accounted for. Test your code by selecting a few sample inputs.


## Task 3: Credit Risk Analyst: Calculate Loan Borrowers Probability of Default (PD)
The risk manager has collected data on the loan borrowers. The data is in tabular format, with each row providing details of the borrower, including their income, total loans outstanding, and a few other metrics. There is also a column indicating if the borrower has previously defaulted on a loan. You must use this data to build a model that, given details for any loan described above, will predict the probability that the borrower will default (also known as PD: the probability of default).

Use the provided data to train a function that will estimate the probability of default for a borrower. Assuming a recovery rate of 10%, this can be used to give the expected loss on a loan.

You should produce a function that can take in the properties of a loan and output the expected loss. You can explore any technique ranging from a simple regression or a decision tree to something more advanced. You can also use multiple methods and provide a comparative analysis. Submit your code below.


## Task 4: Analysing FICO Score: Bucketing FICO Scores of Loan Borrowers
Charlie wants to make her model work for future data sets, so she needs a general approach to generating the buckets. Given a set number of buckets corresponding to the number of input labels for the model, she would like to find out the boundaries that best summarize the data.

You need to create a rating map that maps the FICO score of the borrowers to a rating where a lower rating signifies a better credit score.

The process of doing this is known as quantization. You could consider many ways of solving the problem by optimizing different properties of the resulting buckets, such as the mean squared error or log-likelihood.
