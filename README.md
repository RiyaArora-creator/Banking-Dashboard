# Banking-Dashboard

**Problem Statement –**
Develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

**Solution** **–** 
With our dashboards which are created using Power BI latest tools helps the company to make a decision based on the applicant’s profile like if the applicant is likely to repay the loan then approving the loan otherwise not.

**Software Used**
1. Excel
2. SQL
3. Python
4. Power BI
   
**About Dataset –** 
This dataset basically contains information about bank details ,various client details which consists of multiple tables which are interlinked with each other through keys like primary key and foreign key.
The various tables are Banking Relationship, Client-Banking, Gender, Investment Advisor and Period.

**Data Cleaning –**

**Calculated Functions –** 
Sum : 
The power bi sum function will add all the numbers in a column and the column contains numbers to sum. It returns a decimal number.
Syntax :
Sum= SUM(<column>)
Example:

Bank Deposit = 
SUM('Clients - Banking'[Bank Deposits] )

DistinctCount :
Counts the number of distinct values in a column
Syntax:
DISTINCTCOUNT(<column>)
Example :
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID] )

Sumx :
Returns the sum of an expression evaluated for each row in a table.
Syntax:
SUMX(<table>, <expression>)
Example :
Total Fees = SUMX('Clients - Banking' , [Total Loan] * 'Clients - Banking'[Processing Fees] )

Switch :
Evaluated an expression against a list of values and returns one of multiple possible result expressions
Syntax :
SWITCH(<expression>, <value>, <result>[, <value>, <result>]…[, <else>])

DATEDIFF :
Returns the number of interval boundaries between two dates.
Syntax :
DATEDIFF(<Date1>, <Date2>, <Interval>)
Example :
Engagment Days = DATEDIFF('Clients - Banking'[Joined Bank],TODAY(), DAY )

**KPI’S:** 
In which followings KPIS are present :

Total Clients : 
Total Clients KPI represents total number of clients in banking.
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID] )

Total Loan :
Total Loan gives you information about the bank loan + Business lending + credit cards balance of particular  investor , gender.
Total Loan = [Bank Loan] + [Business Lending] + [Credit Cards Balance]

Bank Loan :
Bank Loan gives you information what is the loan amount of loan to be repaid by the client to bank.
Bank Loan = SUM('Clients - Banking'[Bank Loans] )

Business Lending :
Business lending gives you information about the loan amount given to small business.
Business Lending = SUM('Clients - Banking'[Business Lending] )

Total Deposit 
Total Deposit gives you information about the amount deposited by particular investors in bank
Total Deposit = [Bank Deposit] + [Savings Account] + [Foreign Currency Account] + [Checking Accounts]

Total Fees :
Total Fees is nothing but the amount charged by the bank for account set-up , maintenance charges etc.
Total Fees = SUMX('Clients - Banking' , [Total Loan] * 'Clients - Banking'[Processing Fees] )

Bank Deposit :
Bank deposit is the money put in the bank.
Bank Deposit = 
SUM('Clients - Banking'[Bank Deposits] )

Checking Account Amount :
Checking account amount  is nothing but which offers easy access to your money for daily transactional needs.
Checking Accounts = 
SUM('Clients - Banking'[Checking Accounts] )

Total CC Amount :
Total CC Amount is a short-term source of financing for a company by a bank.
Total CC Amount = SUM('Clients - Banking'[Amount of Credit Cards] )

Saving Account Amount :
A savings account is an interest-bearing deposit account held at a bank.
Savings Account = SUM('Clients - Banking'[Saving Accounts] ) 

Foreign Currency Amount :
Foreign Currency Account means an account held in a currency that is not the currency of India or Bhutan or Nepal.
Foreign Currency Account = 
SUM('Clients - Banking'[Foreign Currency Account] ) 

Engagement Account :
Engagement Banking is nothing but puts the customer at the center and aims to deliver the digital experiences they expect.
Engagment Length = 
SUM('Clients - Banking'[Engagment Days])

Credit Cards Balance :
It is the total amount of money currently owned by a cardholder to their credit card bank.
Credit Cards Balance = SUM('Clients - Banking'[Credit Card Balance] )




**Visualization And Result –**
**Home** 
<img width="1327" height="740" alt="Banking Dashboard 1" src="https://github.com/user-attachments/assets/ef6cef1b-8087-4f5d-8c25-c3bd6c103e82" />

**Loan Analysis**
<img width="1319" height="728" alt="Banking Dashboard 2" src="https://github.com/user-attachments/assets/1c19118f-f475-4952-aa39-5aeba666ef92" />

**Deposit Analysis**
<img width="1299" height="721" alt="Banking Dashboard 3" src="https://github.com/user-attachments/assets/d5e84a42-22d2-456c-83ab-acd1bb1fe24f" />

**Summary Dashboard**
<img width="1310" height="718" alt="Banking Dashboard 4" src="https://github.com/user-attachments/assets/b9fe0609-5788-4ea3-850f-8b8b2261a5df" />


**Conclusion –**
Empowered by the latest data visualization techniques, Power BI dashboards are among the most effective resources for using in banking sector. As outlined in this write-up, a banking  operations dashboard in Power BI can be developed with key banking related metrics and KPIs.

**Future Work –**
With these dashboards banks can easily know what is the total loan amount and all other things of a particular investor.
It also helps which type of banks have more number of clients as we can see private banks have more number of clients so it can helps other banks can build their strategies to increase clients.
It also provides insights about which nationality has highest bank loans.
It gives information about various types of amount involved in different types of accounts by investors.
