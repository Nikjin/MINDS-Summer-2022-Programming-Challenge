# MINDS-Summer-2022-Programming-Challenge

This project involves predicting sentiment of a few articles scraped from the internet. It started with scraping the website to extract the articles. I used the library called ‘Beautiful Soup’ to parse the website. I inspected and found the pattern to extract the links to recent articles on the [website](https://www.aljazeera.com/where/mozambique/). All the articles/links are in chronological order, i.e. the top-most link contains the recent/latest article. I extracted all the links in a list and then sliced the list to get 10 recent articles and then stored the data in a JSON file. The data was then altered and pre-processed to make an accessible dataset for the next steps.

In the next step, I performed sentiment analysis using two different methods:
  1. Pre-trained BERT Model
  2. TextBlob


Results for both the analyses differed from each other. BERT classified all the articles with negative sentiment. In the BERT prediction, we get 5 values ranging from 0 to 4. The more the value, the more the positive sentiment. I classified 0 and 1 as negative, 2 as neutral, and 3 and 4 as positive for our task. While for Textblob, there were float polarity/sentiment values ranging from [-1,1]. I classified 0 as neutral, negative and positive values as negative and positive sentiment, respectively. The prediction was not the same as BERT. TextBlob classified many articles with a positive sentiment.


After analyzing the results manually, I can conclude that BERT prediction was much better than TextBlob, as the latter predicted positive sentiment for articles with obvious negative/violent content.

## IDE Used
JuPyter Notebook

## Visualization

### Sentiment Analysis using Pre-trained BERT Model

![SA using BERT](https://github.com/Nikjin/MINDS-Summer-2022-Programming-Challenge/blob/main/SA%20using%20BERT.png)


### Sentiment Analysis using TextBlob

![TextBlob](https://github.com/Nikjin/MINDS-Summer-2022-Programming-Challenge/blob/main/SA%20using%20TextBlob.png)


