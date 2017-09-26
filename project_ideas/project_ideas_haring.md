##### Paige Haring, peh40@pitt.edu
##### 9/25/17
##### Project Ideas



### Working Title 1
Gendered Name-calling in the 2016 US Election


### Data
1) https://github.com/brendanmmcmanus/trump_speeches

Transcriptions of all of Hillary Clinton and Donald Trump's speeches from the beginning of the 2016 election to the end from Brendan McManus's GitHub. My dataset is a corpus of 130 transcriptions of speeches given by both candidates throughout the election as text files. These text files include some in-text annotations like the name of who was speaking as follows: [Speaker] and other annotations like [laughter]. I would have to decide how to/if I should remove this extra information. Additionally, I have found several other corpora that could be useful as well.

2) https://mega.nz/#F!uIwHnK4I!z0gBGy1E93Gs7sg_uO26vw

This is a collection of all of Hillary Cinton and Donald Trump's tweets from the end of the election period and onwards. The goal of the creator of this corpus was to use this data for author identification of tweets.) This might not end up being relevant. I haven't looked to in depth at this dataset yet, but I'm including it here so I dont' forget about it. 

3) http://www.presidency.ucsb.edu/debates.php

The transcripts of all of the debates that occured during this election can be found at this site. They are provided by The American Presidency Project at UC Santa Barbara. The data from this site has been scraped for Trump, and formatted to only include times he was speaking here:
https://github.com/alexmill/trump_transcripts
I can scrape the site myself for Hillary's debates, or reformat the Trump ones that already exist. I'm not exactly sure which of these data sets I'll use yet, but they could all be helpful.

### Analysis
My end goal is to use this data to assess and pick out namecalling or gendered referring expressions in political speech. It would be interesting to look for repetition in the speeches and the simplicity of the speeches. I did a report in a different class about the 2016 presidential debates last year and looked at data from debates during the French presidential election with the first female candidate to make it to the debate round. That study looked at interruptions and gendered referring expressions. Now I have the skills to do that analysis myself on the US election. I plan for some part of this project to involve manual annotation of the debates for referring expressions. It would be interesting to compare my findings to the findings in that paper about the French election.

### Presentation
I plan to present the paper I was referring to above as part of my presentation to discuss some of the effects of gendered referring expressions as a method of gaining power.

### Working Title 2
TED Talks Classifier

### Data
https://www.datazar.com/file/f056e5bd0-c097-4177-a77d-6e71ef4dc66d

This is a dataset of 2000 TED Talks including the following information for each talk:
- id
- speaker
- headline
- url
- description
- transcription url
- month filmed
- year filmed
- event
- duration
- date published
- tags

It seems really clean already, but it seems like I would have to go to each URL on my own and scrape it for the transcription.

### Analysis
I think it would be cool to take advantage of the tags column in the data, especially because TED Talks are on a lot of diverse topics, and use it to build a topic classifier. You would feed it a document, and it could (hopefully) return tags to tell you what the the document was about. I would train a classifier with the transcripts and tags, but I don't know how well that would work with only 2000 talks to use to train.

### Presentation
Hopefully as part of my presentation I would be able to demonstrate how my classifier works for the class and then have people come up to try it.