# Trump's Hate on Twitter

Analysing 34771 Tweets by Donald Trump from Mai 4 2009 to August 13 2019 using the Vader Sentiment Analyzer.

![Trump Hate](dt.png)
Source: [Gage Skidmore](https://www.flickr.com/photos/gageskidmore/32758233090)

## 0 Datas Sources

All 34,771 short messages published on the social network by the 45th US President Donald Trump between 4 May 2009 and 13 August 2019 were considered for the story: [«Trump Twitter Archive»](http://www.trumptwitterarchive.com).
The deleted tweets are also included. The approximately 2000 messages retweets were excluded. The cleaned data in .csv format [is hier](https://github.com/tamedia-ddj/trumphate/blob/master/trumptweets.csv).

## [1 Sentiment-Analysis](https://github.com/tamedia-ddj/trumphate/blob/master/1.%20Sentiment%20Analysis.ipynb)

The ["Vader Sentiment Analyzer"](https://github.com/cjhutto/vaderSentiment) was used to categorize the messages into positive, negative or neutral messages. This is an algorithm that has been openly published on the Internet by a group of researchers. It is specifically designed to categorize the tone of English language social media content.

Among other things, the algorithm uses a lexicon of words defined as either positive, neutral or negative. The analysis also takes into account punctuation or whether certain words are written in capital letters. The combination of all parameters results in a value between 1 and -1 per message. In the present analysis, everything with a value below -0.5 was classified as negative; everything between -0.5 and 0.5 as neutral; everything above 0.5 as positive. Using this system, 16181 was classified as neutral, 13720 as positive and 4870 as negative. For quality control purposes, 100 classified notifications were subsequently checked manually. In all cases, the classification was useful. More information about the method can be found [here](http://comp.social.gatech.edu/papers/icwsm14.vader.hutto.pdf), and [the actual code is stored here](https://github.com/cjhutto/vaderSentiment).

## [2 Name extraction](https://github.com/tamedia-ddj/trumphate/blob/master/2.%20Name%20Extraction.ipynb)

Zur Extrahierung der Namen wurde der auf die Programmiersprache Python basierte Werkzeugkasten [Natural Language Toolkit] (NTLK)](https://www.nltk.org) verwendet. Die in einem ersten Durchlauf ermittelten Namen wurden dann von Hand zusammengeführt. Zum Beispiel: «Crooked Hillary» und «Hillary Clinton» oder «Loser Obama» und «Barack Obama».

## 3 Artikel
[Published on Tages-Anzeiger.ch on 18. August 2019](https://www.tagesanzeiger.ch/ausland/Trumps-Hasstiraden-in-den-sozialen-Medien-nehmen-unaufhoerlich-zu/story/11406769) (paywalled)
![PDF Version of newspaper page](ta_20190817_0_0_12.pdf))
