# Spring 2023 VIP - Machine Learning for Financial Market
## Qing Claire Dong's Notebook
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
