##Vectorization Methods for Text Preprocessing##

This project explores the various text vectorization options available in scikit-learn. Text vectorization is the process of converting text data into numerical representations which are necessary for many machine learning algorithms. The commonly used vectorization methods explored in this project are:

1. **Bag of Words**: Counts the frequency of each word in the dataset. Each document is represented as a vector of word frequencies.

2. **N-Grams**: Counts the frequency of each groups of N words, allowing for some context and word-order to be captured. N-gram vectorization can create a feature space that is prohibitively large.

3. **TF-IDF**: Term Frequency - Inverse Document Frequency measures the importance of a term in a document relative to the corpus. It combines term frequency with inverse document frequency, which is the logarithmically scaled inverse fraction of the documents that contain the word. In scikit-learn, TfidfTransformer will compute a normalized Term Frequency vector, which divides the counts by the total number of words in the document. If the flag use_idf=True, then Inverse Document Frequency will also be calculated.

4. One-hot encodings

With a large enough text corpus, more advanced vectorization methods can better capture semantic relationships without building out a computationally prohibitive feature space. Word embeddings such as Word2Vec and GloVe. In transformer-based models, positional encodings can be added to word embeddings to give the model information about word order. A positional encoding creates a vector with information about positions of words in a sentence and adds these vectors to the wrod embedding.

The use of these different methods can affect the performance of the NLP task. In this notebook, two different classifiers are trained using the three different vectorization options. Text data is taken from the newsgroups dataset, which can be found in scikit-learn at `sklearn.datasets.fetch_20newsgroups`.

This notebook is partially adapted from the scikit-learn Working with Text Data [tutorial](scikit-learn.org/stable/tutorial/text-analytics/working-with-text-data.html)

