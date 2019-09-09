# Quora-text-classification kernel
Kernel for [Quora Insincere Questions Classification](https://www.kaggle.com/c/quora-insincere-questions-classification) Kaggle competition.
## Competition description
 A key challenge is to weed out insincere questions -- those founded upon false premises, or that intend to make a statement rather than look for helpful answers.
 An insincere question is defined as a question intended to make a statement rather than look for helpful answers. 
 
 Besides dataset there are also 4 word embedding provided, such as:
 * [GoogleNews-vectors-negative300](https://code.google.com/archive/p/word2vec/) 
 * [glove.840B.300d](https://nlp.stanford.edu/projects/glove/)
 * [paragram_300_sl999](https://cogcomp.org/page/resource_view/106) 
 * [wiki-news-300d-1M](https://fasttext.cc/docs/en/english-vectors.html) 
 
 Full description and the dataset itself can be found [here](https://www.kaggle.com/c/quora-insincere-questions-classification/data).
 
 ## Model description 
 All original texts are normalized to cover more words by embeddings. Two embedding matrices have been used. Glove, and paragram. 
 The mean of the two is used as the final embedding matrix.
 
 Model architecture is a Binary LSTM with an attention layer and an additional fully connected layer. Also using CLR and a capsule Layer. Blended together in concatentation.
