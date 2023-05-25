# Maotai Stock Analysis

## Project Summary

Please use Python for programming to solve the following problems, with the organization of the necessary results.

Database: mydatabase.sqlite

## Document Storage Operations

FIRST, get data from 6 tables in "mydatabase.sqlite" with the help of Sqlite3.

NEXT, create a new folder and store the data in it in pickle mode. Then compress the stored  PKL documents with zipfile, and delete the corresponding PKL documents after the compression. 

FINALLY, unzip the compressed document and re-open the PKL document.

## Data cleaning

Process data from Maotai stocks with steps below:

* Convert the DATE column to the type of datetime and character string.

* Illustrate by ploting as well as see whether there were any null values.

* Process null values with these steps:
  
  - Fill it with 0
  
  - Pre-process data
  
  - Linear interpolation processing

* Change anything other than three standard deviations to three standard deviations.

* Calculate the z-score value of the data in a rolling window of 60 data points.

* Convert the data to a monthly frequency and calculate a momentum of 12-1.

* Calculate the annual rate and draw a histogram to illustrate it.

## Strategy Construction

Re-extract the SQL data and clean it, then complete the following questions:

* Construct the CAPM model for Maotai stocks. RM uses the CSI 300 index. We could assume that the rf is equal to the interest rate of one-year treasury bonds(2%). 

* CSI 300 Index(hs300), China Securities 500 Index(zz500), China Bond 10-year Treasury Total Wealth Index(bond10), The Bond Total Wealth Index of 3-5 year Bonds(bond3-5) and The Bond Total Wealth Index of Credit Bonds(credit) build a monthly frequency adjustment warehouse risk parity model, and write the strategic results:
  
  * Scroll through a review window of 60 consecutive days to calculate the weights assigned to each period of the risk parity (optimal)
  
  * Calculate the annualized yield, annualized volatility, Sharpe ratio(rf = 2%) and maximum retracement of the risk parity portfolio.
