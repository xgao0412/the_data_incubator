# The Data Incubator
The data incubator is a data camp that only chose the top 5% applicants 
as fellows.Through the program, I have learned hands-experience 
about webscraping, spark, SQL, neural network and machine learning. 
It really helped me to take my programming and machine learning 
capabilities to the next level. Each week I completed miniprojects on
diverse and up-to-date topics. Below is a description of introducing topics
and the tools used.

## The new york social graph
[New York Social Diary](http://www.newyorksocialdiary.com/) provides photos
of new york social elite. The caption for each photo forms a natural social graph 
Using this graph, we can get the most popular socialites, the most influential
people, and the most tightly couple pairs.

The data were parsed using BeautifulSoup by scraping html, I also used the spaCy's
entity recognition to get names. Finally, I ran the graph analysis using networkx.

## Yelp review ratings prediction
This project is using json data about each venue, for example, city,latitude/longitude,
,category,attributes. I built 4 models based on each data and a linear regression
model based on the outputs of the previous models.

Specifically, for each model I created my own classes to capture the data, transform them to a list of
dictionaries.This way sklearn dictvectorizer will come in handy. Then a pipeline is used
to train and predict.

I used FeatureUnion to include the four models output. when fit() is called, the featureunion will train
and predict. We can end up with 4 features and then put them into a linear regression model.

## Analyze wikipedia data using MRjob
This project is using MRjob Python package to perform Mapreduce jobs on Wikipedia data. The data was stored in HDFS
and parsed using lxml.etree. Then the top 100 most frequent words, link statistics, top linked by doublelinks are computed
using MRjob.
