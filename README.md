## About

This project was created in June 2021 as a part of the University of Warsaw class _CSR - non-financial reporting_.

The purpose of this project was to identify the areas of McDonald's activity which customers/employees complain about on Twitter.

Analysis was divided into 5 stages:
1) Connecting to Twitter API and downloading tweets about McDonald's with `Tweepy` - from **01/05/2021** to **20/05/2021**.
2) Creating dataframe with downloaded data by using `Pandas`. 
3) Cleaning data with regex: dropping duplicates, deleting URLs, unnecessary spaces, and user tags.
4) Performing Sentiment Analysis with `NLTK`'s lexicon VADER and extracting only the negative tweets by using the `.loc function`.
5) Building the LDA model to generate the most popular topics based on content of negative tweets about McDonald's.

## Findings

**Sentiment Analysis**

73.8% of the obtained tweets about McDonald's were positive and 26.2% of them were negative

![alt text](https://github.com/kmlbober/mcdonalds_content_analysis/blob/main/img/sentiment_analysis_result.png?raw=true)

**LDA**

|         | Word 0   | Word 1    | Word 2   | Word 3   | Word 4   | Word 5   |
|:--------|:---------|:----------|:---------|:---------|:---------|:---------|
| Topic 0 | drive    | time      | like     | thru     | girl     | parking  |
| Topic 1 | order    | fire      | cry      | meal     | said     | check    |
| Topic 2 | machine  | cream     | always   | broken   | know     | broke    |
| Topic 3 | food     | breakfast | sprite   | coffee   | fucking  | good     |
| Topic 4 | people   | wage      | worker   | hour     | employee | minimum  |
| Topic 5 | burger   | think     | fry      | going    | time     | king     |
| Topic 6 | work     | hate      | people   | year     | stop     | would    |
| Topic 7 | chicken  | sandwich  | boycott  | photo    | would    | like     |

The most complaints on social media were about:
* Topic 0: Drive-thru
* Topic 2: Broken cream machine
* Topic 3: Cancellation of all-day breakfast menu in USA
* Topic 4: Protests over low wages of McDonald's employees
* Topic 7: Customer boycott concerning McDonald’s partnership with Israel (Palestine support)

## To Do

* Changing comments language to English.