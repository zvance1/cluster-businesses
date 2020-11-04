
# Summary
In this project I will fetch data about businesses from the yelp API within 15 miles of UMBC in attempt to help UMBC see relevant information and stats to recruit the most talented students.  The task at hand is to use the yelp API to gather data on the businesses around UMBC and then explore it to find reasons for college students to attend UMBC based on that data.

# Goals

The goal of the data gathering part of this project is to successfully read and understand API docs to gather the cleanest and most informative data for our purpose.  After completion of it I have a better understanding of API usage and implementation and be able to translate that skill to using any API regardless of the limitations.  For the data exploration portion of this project the goal is to be able to explore the data to find information and stats that answer the question / address the problem.  After completion I have a better understanding of how endless the exploration process can be and ideas for where to start and what to look for in the data to provide the best analysis and answer to the question.

# Motivation and Background

The question/ problem at hand here is finding stats and information that will help UMBC in recruiting more students to apply and attend the school.  UMBC is our customer, and the more quality students they can get, the more they can grow as a school and therefore it is of the utmost importance for the school to be able to attract the most talented students.

I do some analysis on the data gathered to look for answers to questions that may help recruit some college students based on the businesses around UMBC.  Our target audience is students that would be coming to live on campus as any applicant close to UMBC with the option of commuting already knows what is around and what they enjoy around the Baltimore area.  So, the main essentials of what a student may look for in a school when leaving home is the restaurants and shops around campus to get an idea of the area and what it would be like to live there.

The process for answering this question is to explore stats/ information about the restaurants and shops around UMBC that are attractive to prospective students.  This is an initial attempt based on intuition and if there was more time to carry the project forward, more experimentation and research could be done on what students look for in local businesses around college and attack those categories in the exploration.  I did not find any blogs/tutorials/articles on this subject, the exploration was based on my own intuition about college students.

# Data Description
You may create a yelp account here: [Yelp Developer Page](https://www.yelp.com/developers).  And once an account is created, create an app.  Once the app is created, from the manage app page there will be a Client ID and API key.  Put the Client Id in a 'auth' section of the secret.cfg file, and the API key in the 'token' section of the same file - further described in the technical report.

I created a list of categories that I believed would be interesting to college students.  The reason I spent the time going through all these groups rather than just simply seraching for terms like 'food' or 'fun' is because of a limitation with the yelp API.  For any one particular query, a maximum of 1,000 businesses may be obtained with it (offset cannot be used above 1,000) and so with breaking the calls down to more specific categories, that minimizes the number of calls that return a number of businesses greater than 1,000 which results in more data for us both in numbers and of higher quality as less is missing.

Looping through and querying for each category, I ended up with 8752 rows of data with 17 columns.  The API docs are available here: [Yelp API Docs](https://www.yelp.com/developers/documentation/v3/business_search).

# Summary of Files

**Data Source:**
<br>
[Yelp Business Search](https://www.yelp.com/developers/documentation/v3/business_search)

**Python Notebooks:**
<br>
[Exploratory Data Analysis](https://github.com/zvance1/come-to-umbc/blob/master/notebooks/clean-and-explore.ipynb)
Note: Not all exploratory analysis made it into the final techincal report - only what I saw as most relevant.
<br>
[Technical Notebook](https://github.com/zvance1/come-to-umbc/blob/master/notebooks/technical-report.ipynb)

**Data Folder (all data in csv format, used in our final python notebooks):**
<br>
[Data](https://github.com/zvance1/come-to-umbc/tree/master/data)

**Data Visualizations Folder (all visualizations used in our final python notebook):**
<br>
[Data Visualizations](https://github.com/zvance1/come-to-umbc/tree/master/images)

**Python Folder (python technical report notebook, and a notebook that fetches the data, and another for the exploration):**
<br>
[Python Files and Notebooks](https://github.com/zvance1/come-to-umbc/tree/master/notebooks)


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
Duration     : September 2020
Last Update  : 10.08.2020
</pre>