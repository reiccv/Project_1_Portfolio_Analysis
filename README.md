# Project 1 Portfolio Analysis - Tech Stocks vs Consumer Stocks

We will be projecting future returns of a portfolio comprised of five consumer stocks as well as a a portfolio comprised of 5 tech stocks over a 15 and 20 year period in order to evaluate the better long term buy. The asset allocation between between stocks and bonds will remain the same between both portfolios.

The Stocks we will be analyzing are

Consumer Stocks:
* P&G
* Johnson and Johnson
* Walmart
* Kellogg
* Coca Cola

Tech Stocks:
* Amazon
* Meta
* Google
* Tesla
* NVIDIA


# Table of Contents
 - [Installation](#installation)
 - [Usage](#usage)
 - [Results](#results)
 - [Contributors](#contributors)

 
# Installation

### Requirements

Python 3.x
Required libraries: pandas, yfinance, numpy, os, requests, json, dotenv, alpaca_trade_api, matplotlib.pyplot

Pandas:
To install pandas, you can use pip by typing `pip install pandas` in your command prompt or terminal.

yfinance:
To install yfinance, you can use pip by typing `pip install yfinance` in your command prompt or terminal.

NumPy:
To install numpy, you can use pip by typing `pip install numpy` in your command prompt or terminal.

os:
The os library is a built-in Python library, so you don't need to install it separately.

Requests:
To install requests, you can use pip by typing `pip install requests` in your command prompt or terminal.

JSON:
The json library is a built-in Python library, so you don't need to install it separately.

dotenv:
To install dotenv, you can use pip by typing `pip install python-dotenv` in your command prompt or terminal.

alpaca_trade_api:
To install alpaca_trade_api, you can use pip by typing `pip install alpaca-trade-api` in your command prompt or terminal.

Matplotlib.pyplot:
To install Matplotlib, you can use pip by typing pip install matplotlib in your command prompt or terminal. Then, to use the pyplot module, you can import it in your code using `import matplotlib.pyplot as plt`.

# Usage

This is a Python code that analyzes stock market data from 2005 to 2023. The code starts by selecting tech stocks and consumer stocks from a larger dataset of all stocks. It then calculates the average share price for each category of stocks and displays the head of each dataframe.

The code then plots the share prices for tech stocks and consumer stocks over the period, as well as the average share prices for both categories. Next, it calculates the daily returns for the tech and average tech stocks and displays their respective head and description statistics. Similarly, it calculates the annualized returns and standard deviation for tech stocks, consumer stocks, and the S&P 500 index.

Finally, it computes the variance and covariance between the daily returns of each tech stock and the S&P 500 index


### First we are importing the neccesary libraries needed to compute the following code.

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image0.PNG)

### The data is then pulled from the csv and placed into a pandas dataframe

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image1.PNG)

### The tech stocks data average is calculated and is then pulled and placed in a seperate dataframe

(repeat steps for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image2.PNG)

### SP500 Data is pulled and placed in seperate dataframe

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/sp500image3.PNG)

### The share price from tech stocks is then plotted using `tech_stocks.plot`

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image4.PNG)

### The average share price from tech stocks and consumer stocks is then plotted together

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/avgtechavgconimage5.PNG)

### Calculating Daily returns for tech stocks and for tech stocks over 18 years

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image6.PNG)

### Daily returns average for tech stocks

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image7.PNG)

### Calculating and Plotting cumulative returns for tech stocks

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image8.PNG)

### Plotting average cumulative returns for SP500, tech and consumer stocks

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image9.PNG)

### Annualized returns and annualized standard deviation

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image10.PNG)

### Calculating variance, covariance and beta for Tech stocks

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image11.PNG)

### Rolling metrics plotted for tech stocks

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image12.PNG)

### Daily returns for SP500 and tech stocks plotted/visualized

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image13.PNG)

### Sharpe ratio for all data

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image14.PNG)

### Loading in API keys, setting tickers and time frame in order to create portfolio

(repeat for consumer stocks)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image15.PNG)

### Implementing code for montecarlo simulation; calculating cumulative returns with an 80/20 split over 10 years

(repeat for consumer stocks and SP500)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image16.PNG)

### Plotting 10 year simulation distribution 

(repeat for consumer stocks and SP500)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image17.PNG)

###  Summary Statistics for Tech stocks simulations

(repeat for consumer stocks and SP500)

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image18.PNG)


### SP500 Summary Statistics

![text](https://github.com/reiccv/Project_1_Portfolio_Analysis/blob/main/images/image21.PNG)


### Results

Our initial hypothesis that centering a portfolio around tech stocks outperforming the market was disproved somewhat. Although both have outperformed the sp500 index, both consumer and tech stock portfolio simulations had yielded similar portfolio valuations. We believe that the results would be altered somewhat if different funds were used to track these industries or adjusting the timeframe to allow for a more volatility in historical NAVS. However, the main takeaway from our exercise was significance of investing etfs/index funds vs in any one stock portfolio. In this exercise we were able to reach extremely high portfolio valuations with investments in a portfolio asset allocation comprising of indvidual stocks, however this also yielded extremely high standard deviation values - indicating our previous portfolio asset allocation was not nearly diverse enough to lower volatility within the portfolio; furthermore it would be very difficult and therefore unrealistic to replicate the degree of cumulative returns projected to 10 years for a collection of a few hyper sucessful stocks as an investment strategy. Based on the above results, we would recommend for investors seeking capital appreciation to pick tech or consumer based etfs with low expense ratios and high allocations to the large cap assets we had investigated earlier, as these stocks seem to have the ability to retain value over time while also having significant enough avenues for capital appreciation. For the more conservative investor, we would recommend investing in the S&P 500, providing more modest returns but captures the market as a whole and posing fewer unsystematic risks.

# Contributors

### Kaushik Basavaraju, Monica Estrada, Christian Hernandez


