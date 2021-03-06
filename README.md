
# Overview
In this project I will fetch data about businesses from the yelp API within 15 miles of UMBC in attempt to find hidden patterns in the businesses surrounding the school.  The task at hand is to use the yelp API to gather data on the businesses around UMBC and then explore and perform machine learning on it to find hidden groups of businesses to help current and prospective business owners.

# Goals

The goal of this project is to understand and use unsupervised learning to discover hidden groups.  After completion of it I have a better understanding of unsupervised clustering apporaches and the best way to optimize their output.  After completion I have a better understanding of how endless the exploration process can be and ideas for where to start and what to look for in the data to provide the best analysis and answer to the question.

# Background and Field Research

UMBC and college campuses in general draw a lot of people to one area which presents a large opportunity for the surrounding businesses.  The type of people that gather at college campuses tend to me similar in certain ways, but very different in others.  For example, the bulk of the people there are most likely in the age range of 18-24, interested in going out around campus with friends, and in most cases not necessarily financially well off as they are paying tuition with minimal income.  On the other hand, the people who gather there may be from anywhere across the world; with different cultures, religions, and culinary practices.

With that, there may be a pattern in what types a businesses are most successful around a college campus.  Perhaps they tend to be cheaper places that fit all kinds of cultures.  The machine learning problem at hand here is: can we detect hidden groups or patterns in businesses of interest to college students, in particular shops and restaurants, within 15 miles of UMBC to see the diversity of them and determine if there are some that should that are redundant and should be gotten rid of and any opportunity for new restaurants and or shops that would fill the void of what is not already there?  For example, say I am looking to start a new business and I want to know if it has a good chance of being successful.  Perhaps there is a void in a certain location for a certain type of business that would be hugely successful if I start it.  In the scenario the stakeholder is the me as the prospective business owner.  And what the stakeholder is asking is what type of business could potentially fill a missing void and be successful as it would be in demand.  In a secondary scenario, there may be cases where some businesses are redundant and with too many of the same businesses, they don't have enough demand to do well.  In this case the stakeholder would be the current business owner struggling and helping him/her see that their business is redundant and potentially offering them help on how to potentially change to be more successful.

# Data Description
You may create a yelp account here: [Yelp Developer Page](https://www.yelp.com/developers).  And once an account is created, create an app.  Once the app is created, from the manage app page there will be a Client ID and API key.  Put the Client Id in a 'auth' section of the secret.cfg file, and the API key in the 'token' section of the same file - further described in the technical report.

I created a list of categories that I believed would be interesting to college students.  The reason I spent the time going through all these groups rather than just simply seraching for terms like 'food' or 'fun' is because of a limitation with the yelp API.  For any one particular query, a maximum of 1,000 businesses may be obtained with it (offset cannot be used above 1,000) and so with breaking the calls down to more specific categories, that minimizes the number of calls that return a number of businesses greater than 1,000 which results in more data for us both in numbers and of higher quality as less is missing.

Looping through and querying for each category, I ended up with 8752 rows of data with 17 columns.  The API docs are available here: [Yelp API Docs](https://www.yelp.com/developers/documentation/v3/business_search).

# Table of Contents

**Data Source:**
<br>
[Yelp Business Search](https://www.yelp.com/developers/documentation/v3/business_search)

**Python Notebooks:**
<br>
[Exploratory Data Analysis](https://github.com/zvance1/cluster-businesses/blob/master/notebooks/clean-and-explore.ipynb)
Note: Not all exploratory analysis made it into the final techincal report - only what I saw as most relevant.
<br>
[Technical Notebook](https://github.com/zvance1/cluster-businesses/blob/master/notebooks/technical-report.ipynb)

**Data Folder (all data in csv format, used in our final python notebooks):**
<br>
[Data](https://github.com/zvance1/cluster-businesses/tree/master/data)

**Data Visualizations Folder (all visualizations used in our final python notebook):**
<br>
[Data Visualizations](https://github.com/zvance1/cluster-businesses/tree/master/images)

**Python Folder (python technical report notebook, and a notebook that fetches the data, and another for the exploration):**
<br>
[Python Files and Notebooks](https://github.com/zvance1/cluster-businesses/tree/main/notebooks)


# Project Info
<pre>
Contributors : <a href=https://github.com/zvance1>Zach Vance</a>
</pre>

<pre>
Languages    : Python3
Tools/IDE    : Anaconda, Jupyter Notebook
Libraries    : pandas, tabulate, requests, configparser, json, csv
</pre>

<pre>
Duration     : November 2020
Last Update  : 11.15.2020
</pre>