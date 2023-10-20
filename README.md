## The COVID-19 storytelling discourse

The following repository contains the data for the paper "Stories and personal experiences in the COVID-19 Discourse".

### Test set of COVID-19 Discourse

The manually annotated test set is available in ``data/test_set_covid19.csv``. The annotated layers describe the
following aspects (binary coded):
- ``STORY``: whether the span represents storytelling or not
- ``PERSONAL``: whether the span represents a personal (first-hand, protagonist is individual) or general story
- ``CLARIFICATION``: argumentative function of clarification
- ``BACKGROUND``: argumentative function establish background
- ``HARM``: argumentative function of disclosure of harm
- ``SOLUTION``: argumentative function of search for solution
- ``DIFFICULT``: whether annotators perceived the annotation of this item as difficult

Additionally the following information is provided:

- ``ID``: unique identifier of the span
- ``experience_text``: the span itself
- ``comment_body``: the whole comment from which the span was extracted
- ``comment_id``: unique identifier of the comment
- ``token_length``: number of tokens in the span
- ``corpus``: the subcorpus from which the span was extracted

### The storytelling discourse data

The automatically extracted discourse data is available in ``data/storytellingDiscourseCOVID19.csv``. The following information is
provided:
*minority/majority* indicates whether the span was annotated as the respective class or not by the majority of models. The minority indicates that at least
one model predicted the span as a positive. 

- ``ID``: unique identifier of the span
- ``experience_text``: the span itself
- ``comment_body``: the whole comment from which the span was extracted
- ``comment_id``: unique identifier of the comment
- ``token_length``: number of tokens in the span
- ``corpus``: the subcorpus from which the span was extracted
- ``STORY``: whether the span represents storytelling or not
- ``personal_minority/majority``: whether the span represents a personal (first-hand, protagonist is individual) or general story
- ``clarification_minority/majority``: argumentative function of clarification
- ``background_minority/majority``: argumentative function establish background
- ``harm_minority/majority``: argumentative function of disclosure of harm
- ``solution_minority/majority``: argumentative function of search for solution
- ``topic``: the assigned topic of the topic model
- ``comment_id``: unique identifier of the comment
- ``token_length``: number of tokens in the span
- ``BOW``: the most representative n-grams of the assigned topic
- ``General Topic``: the coarse-grained topic of the span

The additional extraction of storytelling spans and the classification layers were automatically assigned as described in the paper.
The topic was assigned by a topic model and each topic maps to a more coarse-grained topic based on the mapping manually created by the authors.
The mapping is available in ``data/topic_mapping.csv``. Topic labels and most representative tf-idf n-grams are available in
``data/topic_labels.csv`` and ``data/topic_ngrams.csv``.

The original / source data for the analysis of storytelling in the COVID19 discourse was extracted from the following sources (all publicly available):

*COVID-19 Vaccine News Discussions*
This dataset contains ~34k user comments from  the *r/Coronavirus* subreddit about COVID-19 vaccination news posted between November 2020 and January 2021.
The dataset is publicly available here: https://www.kaggle.com/datasets/xhlulu/covid19-vaccine-news-reddit-discussions

*Change My View (CMV) from the reddit-covid-dataset*
We extract the subreddit *r/CMV* from the Reddit covid dataset :
https://socialgrep.com/datasets/the-reddit-covid-dataset
It contains any covid-related posts until October 2021 and all corresponding comments. The CMV subreddit consists of ~35k user comments.

*COVID-19 Vaccine Perceptions on Reddit*
Contains ~267k user comments from 8,300 different subreddits that contain both COVID-19 and vaccine-related keywords. The comments have been posted between January and December 2020. 
The data is available here: https://osf.io/urp2a/
Cite the following publication if you use the dataset.

Navin Kumar, Isabel Corpus, Meher Hans, Nikhil Harle, Nan Yang, Curtis McDonald, Shinpei Nakamura Sakai, Kamila Janmohamed, Keyu Chen, Frederick L. Altice, Weiming Tang,
Jason L. Schwartz, S. Mo Jones-Jang, Koustuv Saha, Shahan Ali Memon, Chris T. Bauch, Munmun De Choudhury, Orestis Papakyriakopoulos, Joseph D. Tucker, Abhay Goyal, Aman Tyagi, Kaveh Khoshnood, and Saad Omer.
2022. *COVID-19 vaccine perceptions in the initial phases of US vaccine roll-out: an observational study on reddit.* BMC Public Health, 22(1).
