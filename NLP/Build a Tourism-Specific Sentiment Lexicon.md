#   Build a Tourism-Specific Sentiment Lexicon Via Word2Vec
Some data-driven sentiment lexicons have poor performance on sentiment polarity
classification due to lack of semantic information.  

## 1. Start words

First we need to have a small sentiment lexicon and then use the words to boost up.  Start words are selected from existing sentiment lexicons and each word is labeled with **a certain sentiment score.**



## 2. Sentiment Lexicon Building Mechanism  

Word2Vec can measure semantic similarity,
$$
SemanticSimilarity = \frac{w_1*w_2}{|w_1||w_2|}
$$


  