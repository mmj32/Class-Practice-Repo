Robert Corbett, rwc27@pitt.edu
# Project Proposal

## First Proposal

### Summary
Collect comments from news sites with different political biases: right(fox news), alt-right(breitbart, drudge report),
liberal(Huffington Post, MSNBC) and impartial(AP, Reuters).  Attempt to find data points that
will allow me to develop an algorithm that is able to detect from which site (or bias)
future comments came from.  Then, use machine learning algorithms to find trends in data to make algorithm better.

### Data collection
I hope to write a script that allows me to find and strip comments from HTML files.  Then, seperate them into training,
testing and development classes.  

### Analysis
The data will be analyzed for data points like average comment, sentence and word length, commonly used words, and use of capitalization.
I will attempt to write a script, based on the findings, that is capable of sorting future comments based on which site they
came from.  Hopefully, my script can perform better than random sorting.
After we learn about machine learning techniques, I would like to use them to create another sorting algorithm.
