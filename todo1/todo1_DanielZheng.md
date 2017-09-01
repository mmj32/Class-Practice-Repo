# To-do #1 for LING 1340


### Dataset 1
- Cornell Natural Language Visual Reasoning (NLVR) Corpus v1.0
- Paper [here](http://alanesuhr.com/suhr2017.pdf)
    - Authors: Alane Suhr, Mike Lewis, James Yeh, Yoav Artzi
- [download](https://github.com/clic-lab/nlvr)
- As far as I can tell, there isn't a license for the repository.
- Data
    - Total Size: 549M
    - Data is split into three folders:
        - **dev**
            - Assuming this is the development folder for additional data
        - **test**
            - Test set for classifier
        - **train**
            - Train set for classifier
    - Each folder contains an **images** folder and a **JSON** file
        - **images** contains images 
        - The JSON file looks to be in the [JSON Lines](http://jsonlines.org/) format. 
- This is a crowdsourced dataset of sentences made to describe synthetic images given certain constraints. Various classifiers (CNN, RNN, MLP, LSTM, etc) are tested in attempts to learn which image a given sentence describes.
        

Looking through `nlvr/train/train.json`:

```python
import json
import random
train_data = []
# open file
with open ('Cornell_NLVR_1.0/nlvr/train/train.json') as f:
    for line in f:
        train_data.append(json.loads(line))
        
```


```python
# listing keys in json objects
print(train_data[0].keys())
```

    [u'evals', u'structured_rep', u'label', u'identifier', u'sentence']



```python
# sampling 5 objects
for x in random.sample(train_data, 5):
    print(x)
```

    {u'evals': {u'r0': u'true'}, u'structured_rep': [[{u'color': u'#0099ff', u'x_loc': 72, u'y_loc': 7, u'type': u'triangle', u'size': 20}, {u'color': u'Black', u'x_loc': 39, u'y_loc': 18, u'type': u'circle', u'size': 10}, {u'color': u'Black', u'x_loc': 76, u'y_loc': 57, u'type': u'triangle', u'size': 10}, {u'color': u'#0099ff', u'x_loc': 70, u'y_loc': 70, u'type': u'triangle', u'size': 30}], [{u'color': u'Yellow', u'x_loc': 41, u'y_loc': 3, u'type': u'triangle', u'size': 10}], [{u'color': u'Black', u'x_loc': 22, u'y_loc': 73, u'type': u'square', u'size': 20}, {u'color': u'Black', u'x_loc': 81, u'y_loc': 9, u'type': u'triangle', u'size': 10}]], u'label': u'true', u'identifier': u'1198-0', u'sentence': u'There is no square closely touching the bottom of a box.'}
    {u'evals': {u'r2': u'true'}, u'structured_rep': [[{u'color': u'Black', u'x_loc': 0, u'y_loc': 47, u'type': u'triangle', u'size': 10}], [{u'color': u'Yellow', u'x_loc': 80, u'y_loc': 24, u'type': u'circle', u'size': 20}, {u'color': u'#0099ff', u'x_loc': 80, u'y_loc': 56, u'type': u'circle', u'size': 20}], [{u'color': u'#0099ff', u'x_loc': 17, u'y_loc': 45, u'type': u'triangle', u'size': 20}, {u'color': u'Black', u'x_loc': 18, u'y_loc': 83, u'type': u'triangle', u'size': 10}, {u'color': u'Black', u'x_loc': 48, u'y_loc': 70, u'type': u'circle', u'size': 30}, {u'color': u'Black', u'x_loc': 71, u'y_loc': 36, u'type': u'square', u'size': 20}]], u'label': u'true', u'identifier': u'129-1', u'sentence': u'There is 1 box with only 1 item'}
    {u'evals': {u'r5': u'false'}, u'structured_rep': [[{u'color': u'Black', u'x_loc': 40, u'y_loc': 80, u'type': u'square', u'size': 20}], [{u'color': u'Black', u'x_loc': 40, u'y_loc': 80, u'type': u'square', u'size': 20}], [{u'color': u'Yellow', u'x_loc': 40, u'y_loc': 80, u'type': u'square', u'size': 20}, {u'color': u'#0099ff', u'x_loc': 40, u'y_loc': 59, u'type': u'square', u'size': 20}, {u'color': u'#0099ff', u'x_loc': 40, u'y_loc': 38, u'type': u'square', u'size': 20}, {u'color': u'Yellow', u'x_loc': 40, u'y_loc': 17, u'type': u'square', u'size': 20}]], u'label': u'false', u'identifier': u'3419-3', u'sentence': u'There is no yellow block as the base of a tower.'}
    {u'evals': {u'r0': u'false'}, u'structured_rep': [[{u'color': u'Black', u'x_loc': 22, u'y_loc': 2, u'type': u'circle', u'size': 10}, {u'color': u'#0099ff', u'x_loc': 19, u'y_loc': 14, u'type': u'triangle', u'size': 20}], [{u'color': u'Yellow', u'x_loc': 21, u'y_loc': 17, u'type': u'square', u'size': 10}, {u'color': u'Black', u'x_loc': 46, u'y_loc': 70, u'type': u'square', u'size': 30}, {u'color': u'Black', u'x_loc': 53, u'y_loc': 11, u'type': u'square', u'size': 10}], [{u'color': u'#0099ff', u'x_loc': 4, u'y_loc': 45, u'type': u'circle', u'size': 30}, {u'color': u'#0099ff', u'x_loc': 57, u'y_loc': 6, u'type': u'square', u'size': 20}, {u'color': u'#0099ff', u'x_loc': 55, u'y_loc': 70, u'type': u'triangle', u'size': 30}]], u'label': u'false', u'identifier': u'2004-3', u'sentence': u'There are exactly two black objects touching the edge'}
    {u'evals': {u'r0': u'true'}, u'structured_rep': [[{u'color': u'#0099ff', u'x_loc': 70, u'y_loc': 38, u'type': u'triangle', u'size': 30}, {u'color': u'#0099ff', u'x_loc': 63, u'y_loc': 80, u'type': u'triangle', u'size': 20}], [{u'color': u'#0099ff', u'x_loc': 25, u'y_loc': 18, u'type': u'triangle', u'size': 30}, {u'color': u'Yellow', u'x_loc': 65, u'y_loc': 64, u'type': u'triangle', u'size': 30}, {u'color': u'Black', u'x_loc': 63, u'y_loc': 21, u'type': u'circle', u'size': 30}, {u'color': u'Yellow', u'x_loc': 0, u'y_loc': 70, u'type': u'square', u'size': 30}], [{u'color': u'Yellow', u'x_loc': 64, u'y_loc': 64, u'type': u'square', u'size': 30}, {u'color': u'#0099ff', u'x_loc': 51, u'y_loc': 23, u'type': u'square', u'size': 30}, {u'color': u'Yellow', u'x_loc': 10, u'y_loc': 13, u'type': u'triangle', u'size': 30}]], u'label': u'true', u'identifier': u'1912-1', u'sentence': u'there are exactly three yellow objects not touching the edge'}



```python

```

### Dataset 2
- WordNet-Morphosemantic Database
- Paper [here](https://wordnet.princeton.edu/wordnet/publications/jbj-jeju-fellbaum.pdf)
    - Authors: Jordan Boyd-Graber, Christiane Fellbaum, Daniel Osherson, Robert Schapire, Princeton University
- [Dataset link](http://wordnet.cs.princeton.edu/downloads.html)
- License: "Princeton University makes WordNet available to research and commercial users free of charge provided the terms of our [license](https://wordnet.princeton.edu/wordnet/license/) are followed, and proper reference is made to the project using an appropriate citation. Acknowledgement is both required for use of WordNet, and critical to future funding for project maintenance and enhancements. "
- This is a very interesting dataset. 
    - links among noun and verb "synsets", or sets of synonyms, contain words that share an underlying meaning. 
    - examples in this [readme](http://wordnetcode.princeton.edu/standoff-files/morphosemantic-links-README.txt)
- Data is given in the form of an Excel spreadsheet with 17739 rows. First four rows: 

**arg1 sensekey**|**arg1 offset**|**relation**|**arg2 sensekey**|**arg2 offset**|**arg1 gloss (abbreviated)**|**arg2 gloss (abbreviated)**
:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:
cannibalise%2:34:00::|201162291|agent|cannibal%1:18:00::|109891079|eat human flesh|a person who eats human flesh
cannibalize%2:34:00::|201162291|agent|cannibal%1:18:00::|109891079|eat human flesh|a person who eats human flesh
court-martial%2:41:01::|202499172|agent|court-martial%1:14:00::|108331525|subject to trial by court-martial|a military court to try members of the a...
equal%2:42:01::|202672187|agent|equal%1:18:00::|109626238|be equal to in quality or ability; "Noth...|a person who is of equal standing with a...




