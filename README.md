# UK Stocks Portfolio and Performance Dashboard

### Dashboard Link: 
https://public.tableau.com/views/tableaustocksdashboard1/StocksPerformance?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Dashboard Preview:

<img width="1919" height="1079" alt="Image" src="https://github.com/user-attachments/assets/96d16505-7d27-4518-9456-e7e2883ba3ab" />


## Problem Statement

Investors track stock prices but do not always measure how these movements impact their personal investment value. This Tableau dashboard helps visualise how selected UK stocks perform over time and how a personal portfolio changes daily based on live market prices. It shows which stocks contribute most to returns and how volatile each one is across the year.

## What this dashboard shows

- Individual stock price movement

- Daily and weekly volatility

- Total portfolio performance

- Profit and loss

- Profit and loss percentage

- Top holdings in portfolio

## Data Source

Data is pulled from Google Sheets using the GOOGLEFINANCE function

 =GOOGLEFINANCE(A2, "Price", EDATE(TODAY(), -12), TODAY()) 


This returns daily closing prices for the past one year for each selected ticker. Daily percentage change was calculated in Google Sheets.

## Stocks used in this version

- BARC (Barclays)

- ENT (Entain)

- ULVR (Unilever)

- BP (BP)

- TSCO (Tesco)

## A mock portfolio sheet is included to simulate a real portfolio and contains

- Stock name

- Units bought

- Purchase price

- Purchased cost

## Data Files

Local copies of the Google Sheets data are included in this repository inside the data folder so that the project is reproducible.
These files represent the same dataset used in the dashboard and can be used for reference or testing.
The Google Sheet itself continues to update live based on the GOOGLEFINANCE formula.

Google Sheets Link: 

- UK Stocks Data For Tableau: https://docs.google.com/spreadsheets/d/1UPU-syR_2kWPn4e7TYMWlvXhWDgxj2wSEx-93GrgjW8/edit?usp=sharing
- UK Stock Portfolio: https://docs.google.com/spreadsheets/d/1tA5kHUoQgFz6DK1qKITz4b6NY68gpKYbbqpAro63sY0/edit?usp=sharing

## Steps Followed

- Created a Google Sheet with stock tickers and pulled live twelve month closing prices using GOOGLEFINANCE

- Calculated daily percentage change

- Built a mock portfolio dataset including stock name,units bought, purchased price and purchased cost
  
- Connected both Google Sheets to Tableau using a live connection and established relationships between price data and portfolio data based on stock name

- Built visualisations including area, line, bar, and bubble charts
- Created calculated fields for Current Value, Daily Value, Profit and loss and percentage,Last Closing Price,Red or Green indicator for positive or negative returns

- Created parameters for dynamic filtering, including Period and Stock Name

- Added visual filters and sheet level filters for time periods and individual stocks

- Built KPI cards to display total portfolio value, profit or loss amount and percentage

- Formatted currency values to show pound symbol and customised tooltips

- Applied color logic to highlight positive and negative performance

- Published the final dashboard to Tableau Public for sharing and interactive viewing

## Insights

- Shows how each stock performs over time

- Calculates profit and loss at stock level and portfolio level

- Highlights volatility trends

- Demonstrates the effect of daily price changes on personal investment

- Helps compare holdings and identify stronger or weaker performers

## Tools Used

- Google Sheets

- GOOGLEFINANCE

- Tableau Desktop Public

- Tableau Public

## Future Improvements

- Add more UK tickers and other countries

- Include moving averages and indicators

- Build a date scaffold to fill weekends and holidays for smoother area charts

- Use Tableau Cloud for scheduled automatic refresh

## Author

Created by Ashish Dey

Feel free to open an issue or connect for suggestions or improvements.
