# Term Project Ideas

## 1. Time Magazine: Measuring Sentiment Related to Historical Figures
- SUMMARY: I was looking to use the TIME Magazine archive (from recent years) to
scan for proper nouns and also grab the text that surrounds specific proper nouns,
namely famous figures. After parsing out the data, it should show the sentiment
toward certain figures as being favorable or unfavorable.  

- DATA: The data would be sourced from the TIME archive. I would only use ones from the
past decade, to keep the corpus manageable. After scanning, I would maintain data structures
that map the name of a famous figure to sentences that refer specifically to them.
Additionally, each figure would receive a sentiment score. Additionally, there would
be additional fields where a particular figure would receive sentiment scores across
multiple years if they are mentioned multiple times across multiple issues.  

- ANALYSIS: I'm hoping to bring in other corpora using nltk to assist with the sentiment analysis. Additionally, I may have to manually take tallies of specific vocabulary as being particularly positive or negative to use. The end goal is to be able to produce output mapping the rise and fall of the sentiment for particular people across a number of years.

- PRESENTATION: I think the primary component of this would be the visuals since the analysis would look into the change of something over time.

## 2. Twitter Scraping
- SUMMARY: This idea was to try and learn how to scrape Twitter to develop a corpus, mapping the use of certain colloquialisms with specific popular hashtags. Additionally, I could try to look into the geography of certain hashtags to see in what places certain topics are trending.  

- DATA: I am not quite sure what the data would look like, other than it would map instances of the occurrence of particular hashtags, which are mapped to a number of instances where that hashtag is used. Additionally, the location of the tweet would be saved as well to be able to map.  

- ANALYSIS: I would likely use the Corpus of Contemporary American English to supplement the analysis. After parsing a tweet, I could count the number of proper English words versus slang, which can give insights into the formality of a hashtag.

- PRESENTATION: The focus of the presentation can show statistical summary data of particular hashtags. Additionally, visuals like maps could be created to show how certain words and hashtags are trending or popular.
