# oil future portfolio
I want to build a commodity curve strategy by trading WTI futures.  

The commodity curve strategy takes a long position of an optimally-chosen contract and a short position of another contract at any time in order to capture the commodity's term struture premium.

Here are the steps for portfolio construction and rebalancing:

Step 1: At each month-end date, I consider contracts on tenors from T2 to T12. (T1 contract would not be considered since it has less than 1 month to expiration).

Step 2A: For each tenor contract, calculate the expected rolling return if holding the contract for one month based on the current term structure.  (Let's assume the expiration dates of two adjacent contracts are always exactly one-month away).
Step 2B: Among the 11 contracts (from T2 to T12), build a portfolio with one long position in the contract with the highest expected rolling return, and one short position in the contract with the lowest expected rolling return.

Step 3: Hold the portfolio till the next month-end and rebalance the portfolio.

I run a back-test for the strategy from 1/31/2000 to 1/31/2019, calculate the strategy's monthly returns, and deliver the following results:
1. Assume investing $1 in the strategy from day 1, i.e., 1/31/2000, plot the value of the investment over time.
2. Calculate the strategy's calendar year returns, i.e., cumulative returns in each year from 2000 to 2019.
3. Calculate the annualized return, annualized risk, and Sharpe ratio (let's assume risk-free rate of 0) of the strategy.
4. Identify the maximum drawdown period for this strategy.


