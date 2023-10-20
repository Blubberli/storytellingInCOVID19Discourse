##The COVID-19 storytelling discourse

The following repository contains the data for the paper "Stories and personal experiences in the COVID-19 Discourse".

###Test set of COVID-19 Discourse

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

###The storytelling discourse data

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