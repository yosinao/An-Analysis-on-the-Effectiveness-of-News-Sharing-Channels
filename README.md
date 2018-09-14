# Project-1 - An Analysis on the Effectiveness of News Sharing Channels

This project's objective was to compare the time frequencies at which articles show with the top queries from the most shared articles on Facebook, Twitter, and email. A summary of the results show articles shared via Facebook appear more frequently than those shared via Twitter or email.

## Getting Started
### Required API
The following APIs are required to run the code on your local machine:

* Google Trends/PyTrends API
* NYTimes API
* Reddit API

### Required Python modules
Things that you need to install on to your local machine
```
PyTrends (Google Trends API Wrapper): 
pip install pytrends

PRAW (Python Reddit API Wrapper):
pip install praw 
```
### Further Setup

A Google API key is required to use PyTrends. A Reddit.com account, as well as a corresponding developer app key and secret key, is required to use PRAW.

## Running Tests
### Data Retrieval
Data was retrieved from the New York Times API for all three sharing channels (Facebook, Twitter, email). There were 35 news sections (e.g. Opinion, Obituaries, Travel, etc.) to choose from, and 8 of these were determined to be proper news articles for purposes of our analysis. Initially, Google Trends (via the Python wrapper PyTrends) was used to obtain results. To strengthen the case for supporting the hypothesis, the Reddit API (via the Python wrapped PRAW) was used as well.

### Google Trends/PyTrends
#### Finding the Data Trend
Pytrends, a Python wrapper for the Google Trends API, was used to run the top 5 queries in each New York Times sharing channel. The interval of time used was one year.

#### Comparing the Data Across Three Channels
The benchmark used to determine whether a search query was considered of significance was to see where its Google Trends trendline exceeds 50% of the maximum value. As the output produced by PyTrends was not easy to look at to determine the number of weeks where this benchmark was fulfilled, the Google Trends website was used to more precisely determine this was the case for each of the top queries. 

### Reddit 
#### Finding the Data Trend
PRAW, a Python wrapper for the Reddit API, was used to run the top 5 queries in each New York Times sharing channel. The interval of time used was chosen to be one year to be consistent with the approach taken with PyTrends.

#### Comparing the Data Across Three Channels 
The benchmark used to determine whether a search query was considered of significance was to see where its articles had more than the median number of upvotes on Reddit's r/news. The frequency of corresponding article appearance was calculated to be one year divided by the number of articles found this way, and the average of these frequencies was lowest among articles shared via Facebook, followed by articles shared via Twitter, and finally by articles shared via email. 

## Authors
* Hong Li 
* Niño Leonard J Yosinao
* Ahmad Bou Merhi
* Yanin Swangrujithum 

## Acknowledgements
* Thank you to the creators of PyTrends for their Python wrapper for the Google Trends API: https://github.com/GeneralMills/pytrends
* Thank you to the creators of PRAW for their Python wrapper for the Reddit API: https://github.com/praw-dev/praw

## Presentation Link
* https://docs.google.com/presentation/d/1bMl7znjuppp_4czhlwirky82LfQbNPjh36owapdiBFU/edit?ts=5b986bef#slide=id.p