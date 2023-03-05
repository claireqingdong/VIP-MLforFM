# Spring 2023 VIP - Machine Learning for Financial Market
## Qing Claire Dong's Notebook
### Week 8, Mar 3
Weekly team meetings:
1. Discussed the paper we would like to replicate: https://onlinelibrary.wiley.com/doi/epdf/10.1111/1475-679X.12429
2. Saniya and Johnny: introduction, rest of us: timeline
3. Finish indivudual paragraphs by Wednesday
4. Finish literature review by Thursday: [Link to shared sheets](https://gtvault-my.sharepoint.com/:x:/g/personal/ssavla30_gatech_edu/EZYnl749yj5BsbG2dMM01woB20z7OMseI7b99zkw4pd5Hw?e=83fvha)

### Week 7, Feb 24
Guest speaker in class
### Week 6, Feb 17
Valuation Basics Notes
- Methods of valuation
    - Relative/comparable firm
        - Identify comparable assets
        - Convert market values into standardized values
            - Using earning multiples(PE - price per share/earnings per share), book value, revenue, 
        - Controlling difference between firms
        - Too subjective, difference still exist
    - DCF
        - Intrinsic valuation(+expected cash flows)
        - Start from dividend discount model, divided both sides by earning per share -> FCFE model
        - Higher PE rations: higher growth firms, lower risk firms, lower reinvestment needs(actually not that reliable)
        - Value/earning, value/cash flow
    - Real Options
    - Simulations  
      
Accessing finance and economic data Notes
- WRDS
    - Finance / accounting data
        - Company financial statement, stock related data
        - Sources: fillings, trading price, industry specific, events and transactions, institutional investors, firm behavior
        - COMPUSTAT: US&CA, global, annual/quarterly/monthly/daily
            - Example: search Wharton compustat
            - Using python 
                - Pip install words
                - .get_table
        - CRSP: stock market data
        - Institutional ownership data(Those-Reuters)
        - Bank regulatory data
        - Fixed income: FINRA requirement, Municipal bonds(Bloomberg)
        - Others: dealscan(commercial loan), execucomp(executives’ salary), institutional brokers, ravenpack
        - Econ data - FRED St. Louis
        - Cartography: starupcartography.com
        - County-level and related: eg. consumerfinance.com

### Week 5, Feb 10
In class, we discussed multiple cash flow models
Group meeting one: formed two subteams -- stocks prediction using company earning and use external factors. Each subteam would try to replicate a relavant paper for the coming weeks.  
  
Notes for Bootcamp videos, Accounting I & II  
Three type of Accounting
- Financial accounting: 
    - US GAAP, FASB responsible for setting US GAAP, SEC monitor FASB. Other countries use IFRS for standards
    - 10-K, 10-Q
    - to external user(investor, creditors, suppliers, customers)
    - Assess the timing, amounts and uncertainty of future cash flows
    - Balance sheet(point in time, assets = liabilities + equity), Income statement(period of time, SE_t = SE_(t-1)+ NI - Dividends + shares issued - share repurchased), cash flow statement(period, operating(direct/indirect90% methods)), notes, audit option
            - Notes: general information, specificity, info related but not yet recognoized
    - Additional requirement: 10-Q, 8-K(major events), proxy statement(stockholder’s right), additional 
- Managerial accounting: to internal user(used for asset management)
- Tax accounting: to tax authorities(IRS)
- Exercise - prepare the balance sheet for the baron
    - Assumptions of reporting model(separate entity, periodicity, monetary units, going concern(go bankrupt?))
    - Balance sheet: Asset: wheat, ox, land, plow…; Liabilities: payable, owner investment, earnings
    - Income statement: Revenue, Expenses
    - Statement of changes in shareholder equity: Beginning value, net income, dividend payment
    - Metrics to determine who performs better: ROE, yield, profit margin

Part 2, mechanics of FA
- Assets
    - Liability + equity
    - Changes in net assets: investment by owners(changes in contributed capital), comprehensive income(revenue-expense), disbursement to owner(changed in earned captial)
- Journal entries and t-accounts: Debits = Credits
- Posting: updating account balances to reflect events recorded in the general journal
- The Debit-Credit Framework
    - Any transaction requires: adjustments to at least two accounts; at least 1 debit and 1 credit
    - debit + on the left, credit - on the right
    - Exerise
        - Invest 10000 to start  new business: Dr. Cash 10k; Cr. Equity
        - Paid 900 in cash for gift basket: Cash, Inventory credit
        - Paid 800 rent: cash, prepaid rent credit
        - Bought 400 equipment: cash, equipment credit, inventory debit
        - Sold 2200 gift basket: Accounts Receivable; Revenue 2.2k
        - Bought 1500 straw to make basket on credit payable in 90 days: inventory debit, account payable credit
        - Found had 1800 supplies remaining
        - Collected 400 from her credit sales: cash debit, accounts receivable credit

Part 3, statement of cash flows  
        - Financing activities  
            - Inflows: cash from sales, borrowing  
            - outflows: cash to owners, retire stock, repay principal   
        - Operating  
            - Inflow: customers, revenue, dividend from investment  
            - Outflows: purchase, operating expenses, interest on debt, income taxes

### Week 4, Feb 3
In class, we were forming teams. I decided my research interest would be on analyzing external factors of the stock market.  
Team meeting time: Friday 5 pm.

### Week 3, Jan 27
1/22 Research proposal completed

I was always trying to think about what factors determine one's gains and losses from the financial market, which is also to say, which factors act on stock prices and buy/sell actions. In an overly idealized situation, I wish to uncover a formula, which is a linear or non-linear combination of multiple factors, and that formula tells us if we should buy/sell a stock. Therefore I am interested in selecting factors/trading strategies as my broad research topic.

As I researched potentially useful financial metrics, I noticed Research and Development (R&D) Expenditure (Note: I was also interested in risk levels, but as SEC does not require risk factors to be in XBRL form, this restrain us from getting sufficient data.). Some articles present that high expenditure not necessarily indicates good performance, while some research demonstrated the high rate of return to invest in R&D. Some also indicate that it depends on sectors. If worth delving deeper into, my research question would be: Do companies' R&D Expenditures have correlations with stock prices, either in the short or long term?

There are two kinds of data sources I need, which would be price and company R&D data. For price data, I could use Yahoo finance to access daily close prices. For the latter one, I would use XBRL US to extract information on 10-K forms. Possible variables would be R&D cost amount, time, and sector.

One of the tools I would use would be machine learning, outputting future prices according to input variables. I would also like to learn about how to apply statistics in finance and be able to test whether a factor is significant for stock prices. Also, I am willing to know more about the existing research on finance and ML and be able to build upon those research.  

1/25 Programming HW revised
### Week 2, Jan 20  
1/17 Programming HW completed  
1/18 XBRL account & credential requested 
* Excel template downloaded, FullReport-DimensionPivot-Template.xlsx, tutorial: https://www.youtube.com/watch?v=S_ZCnQr_8WU  
  - Hard to get streamline data
* Python template: xbrl_us_api-Revenues.ipynb; https://mybinder.org/v2/gh/RomanChychyla/xbrl-api/HEAD?urlpath=lab/tree/xbrl_us_api-Revenues.ipynb
  - contains methods for generating access token, making API queries
  - Examples in the template: revenue from 10-K
1/21 SEC data, dataset intro: https://www.sec.gov/files/aqfs.pdf
  - data we could get: Balance Sheet, Income Statement, Cash Flows, Changes in Equity, and Comprehensive Income) and page footnotes; 10-K, 10-K/A, 10-KT, 10-KT/A, 10-Q, 10-Q/A, 10-QT, 20-F, 20-F/A, 40-F, 40-F/A, 6-K, or 6-K/A
  - 2009 - 2022

### Week 1, Jan 13  
1/15 CITI RCR training completed  
1/16 Video: XBRL in Academic Research  
Link to the recording: https://www.fasb.org/academics#section-5  
Link to slides: https://www.fasb.org/document/blob?fileName=XBRL__Academic_Research-A_Workshop_on_How_to_Pull_XBRL_Data.pdf  
- XBRL: eXtensible Business Reporting Language
    - financial information that is machine-readable
    -  Each number has a link, so a machine can read it
    - Each link has information of tag, time, number…
- Key features: 
    - Label used in filling(name on the chart) is not the element name. Element name = the long tag
    - Elements can be standard across firm or custom defined by the firm(extension)
    - Presentation metadata
- Get tagged: Number , table, accounting policies
- institutions: XBRL international, XBRL US help implement, FASB published, SEC oversight
- How can XBRL help
    - More details inside tags
    - Comparison made easy
    - As-reported(no selective reporting), presentation, text
- Research about XBRL
    - Data quality, regulation, disclosure choices, firm characteristic
- Challenges with using XBRL in research
    - Identifying relevant XBRL elements
    - ? Standardizing compression across firm
    - Errors like duplication, incorrect scale, sign
- How can I access XBRL data?  
  
Hands-on Exercises: Gather data on Revenue 
1. Identify common US GAAP revenue elements 
- Yeti: details of all US GAAP elements - http://xbrlview.fasb.org/yeti/resources/yeti-gwt/Yeti.jsp
    - Browse and get the Name
- EDGAR
    - Company name, filing type, interactive data(or documents), select chart, name, details  
2. Download facts for US GAAP revenue elements - see slides for instruction
- With instruction of python and postgresql, calcbench
- Difference and tradeoffs of standardized data and raw data
3. Search for dimensional data and custom extensions
- Culcbench demonstration, and in python and in postgresql
- Company might use one year standard, one year custom
4. Cleaning data, dimensional data, footnote text search and analysis, metadata

Thought Questions: 1. How to get the data: free resources  - XBRL US and SEC for filing data, Yahoo and S&P for price data  
2. What questions interest me: risk management, statistical testing?

To-do:
1. Coding task and proposal due 1/26 
2. Know how to use XBRL API & SEC
