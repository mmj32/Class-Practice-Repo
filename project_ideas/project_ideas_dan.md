### Project Ideas:

#### 1. Scraping bookmarks from Chrome, automatically group bookmarks into folders and subfolders with topic modeling. In a more general sense, this will group a list of URLs into topics and subtopics.

*Data*:
- A list of URLs to articles
- Each page will need to be cleaned from the page source code into a nice block of text (HTML parser libraries exist, but inline javascript will need to be handled somehow). 

*Analysis*:
- Using a list of URLs, it's possible to extract some interesting linguistic insights to understand what the user is interested in. 
- Gensim for topic modeling, keras/sci-kit for any ML. 
- Can generate a summary about each article/URL about sentence length, TTR, and stuff as well as an actual summary of maybe 3-4 important sentences extracted from the article (textrank?).
- Some kind of ML may need to be employed to group things by their topics, because it's really hard to programmatically know that an article about apples and another about oranges should go a folder called "Fruit". Really unsure about a good approach for this.

*Presentation*
- Could turn into a python module or even a package
- Test on my own bookmarks, or some giant list of URLs and see how it turns out.

#### 2. Tackle something like Cornell's NLVR [challenge](http://lic.nlp.cornell.edu/nlvr/) and try to describe images with text
*Data*
- On GitHub [here](https://github.com/clic-lab/nlvr)
- Nicely formatted into test and train sets
- Has image data and associated JSON of a sentence describing the image and some other indicators.
- Not much cleaning to do here, mostly just understanding what the data contains
*Analysis*
- From what I understand, this involves some image processing paired with NLP to understand what is contained in these images. 
- Cornell describes the task as to determine whether a sentence is true or false about an image. 
    - "The data was collected through crowdsourcing, and requires reasoning about sets of objects, quantities, comparisons, and spatial relations"
- Would involve a lot of ML and combinations of multiple ML techniques (images and NLP) to teach the algorithm to "understand" the images.
- The sentences are all very basic, so stuff like lexical diversity and whatnot aren't super interesting here. Perhaps this isn't that interesting of a project linguistically.
*Presentation*
- End goal would be a writeup of results and the ML approach taken, and some analysis of how images can be described with sentences. 
