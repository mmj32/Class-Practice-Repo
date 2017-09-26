Alicia Sigmon; als333@pitt.edu; 9/25/2017
Project Idea:

# Comparing English Dialects in the News

- I think it would be interesting to look into different dialects of English. Some examples of things I could do would be to compare the most common words or n-grams between the dialects, compare those with the top most common English words and n-grams, and create scripts that could make sentences in those dialects (like bible speak from computational lingustics), write scripts to be able to identify sentences as specific dialects (using test, training, and development splits), find what POS differ most between dialects, etc..
 - To do this, I could delve into the Leipzig Corpus: http://wortschatz.uni-leipzig.de/en/download/ 
 
 
## Canada vs. Australia vs. United Kingdom vs. New Zealand 

- I looked into the English corpora and found datasets of comparable size and year in countries whose first languages (I believe) would mostly be English; Australia, Canada, New Zealand, and United Kingdom. 


### Data: 

Size: 10K sentences - 1 million sentences
 - I am able to download different versions depending on what would be most appropriate for my project.

Format:
 - Includes sentences from the newspapers.
 - All data is from 2002 (15 years ago)
     - However, I believe the comparison would still stand as a valid project despite the langauge data being from the previous decade.
 - The .tar files include many extra cells, that contain data that is unlabeled. I would extract the sentences from the file and then do my own analysis on most frequent words and n-grams and more.

Citation:
 - If I use this data, I am required to cite the following paper:
 
D. Goldhahn, T. Eckart & U. Quasthoff: Building Large Monolingual Dictionaries at the Leipzig Corpora Collection: From 100 to 200 Languages.
In: Proceedings of the 8th International Language Ressources and Evaluation (LREC'12), 2012 


### Analysis:

Questions and Hypotheses:
 - What POS differences are most indicative of the dialects? Hypothesis (Guess..): 1. Noun, 2. Verb, 3. Adjective, 
 - News can be formal or informal: is this data too formal to be able to hear extreme dialectal differences?
      - Is there a noticeable dialect difference in the news between English speaking countries?
 - How do the top 20 words compare? Do different dialects of English favor distinct prepositions? Are any of the most common words indicative of the dialect?
 - How do these dialects compare with the Norvig top words?

Methods:
 - word tokenize
 - n-grams
 - POS tagging
 - writing a script like bible speak
 
 
### Presentation:

(I believe I previously discussed this aspect, so I am not sure if I correctly did the analysis portion above..)

 - I would like to present my data as a comparison between dialects. We can hear dialectal differences, but how distinct are the dialects really? In settings like the news, how distinguishable are dialects? As amount of dialect can differ from person to person, and there is no data on where the speakers grew up, is "Country" a good enough way to split speakers into groups for dialect comparison?
 - I'd like to create a script like bible speak to create sentences for news casts that can be recognized by its country of origin. 
 - I do not know if this data will work for these goals, but I could discover that by beginning to write a script and compare the data.