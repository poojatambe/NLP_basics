# NLP_basics

## Text Preprocessing

Explore given text preprocessing concepts in ```text_preprocessing.ipynb```.


**Tokenization**

* Tokenization is a crucial process in natural language processing (NLP) where text is broken down into smaller units called tokens. 

* These tokens can be words, subwords, characters, or other meaningful elements depending on the tokenization strategy.

```
sentence tokenizer: 
 ['Tokenization is a fundamental step in preparing text data for machine learning models, particularly for tasks like text classification, language modeling, translation, and sentiment analysis.']
word tokenizer: 
 ['Tokenization', 'is', 'a', 'fundamental', 'step', 'in', 'preparing', 'text', 'data', 'for', 'machine', 'learning', 'models', ',', 'particularly', 'for', 'tasks', 'like', 'text', 'classification', ',', 'language', 'modeling', ',', 'translation', ',', 'and', 'sentiment', 'analysis', '.']
 ```

 **Stemming and Lemmatization**

 * Stemming is a text normalization technique in natural language processing (NLP) that reduces words to their root or base form, called the stem, by removing affixes (suffixes or prefixes). 

 * Lemmatization is a text normalization technique in natural language processing (NLP) that reduces a word to its lemma, which is its dictionary form or base meaning. 

* Unlike stemming, lemmatization considers the context and part of speech (POS) of a word to produce linguistically valid outputs.

```
Text : 

'Tokenization is a fundamental step in preparing text data for machine learning models, particularly for tasks like text classification, language modeling, translation, and sentiment analysis.'

Stemming:

['token fundament step prepar text data machin learn model , particular task like text classif , languag model , translat , sentiment analysi .']

Lemmatization:

['Tokenization fundamental step preparing text data machine learning model , particularly task like text classification , language modeling , translation , sentiment analysis .']
```

**Bag of Words**

* The Bag of Words (BoW) transforms text into a numerical format that machine learning models can process by considering the occurrence of words, without paying attention to grammar, word order, or context.

```
Features:  

['analysis' 'broken' 'called' 'characters' 'classification' 'crucial'
 'data' 'depending' 'element' 'fundamental' 'hese' 'language' 'learning'
 'like' 'machine' 'meaningful' 'modeling' 'models' 'natural' 'nlp'
 'okenization' 'particularly' 'preparing' 'process' 'processing'
 'sentiment' 'smaller' 'step' 'strategy' 'subwords' 'task' 'text' 'token'
 'tokenization' 'tokens' 'translation' 'unit' 'words']

Vocabulary: 

{'tokenization': 33, 'crucial': 5, 'process': 23, 'natural': 18, 'language': 11, 'processing': 24, 'nlp': 19, 'text': 31, 'broken': 1, 'smaller': 26, 'unit': 36, 'called': 2, 'tokens': 34, 'hese': 10, 'token': 32, 'words': 37, 'subwords': 29, 'characters': 3, 'meaningful': 15, 'element': 8, 'depending': 7, 'strategy': 28, 'okenization': 20, 'fundamental': 9, 'step': 27, 'preparing': 22, 'data': 6, 'machine': 14, 'learning': 12, 'models': 17, 'particularly': 21, 'task': 30, 'like': 13, 'classification': 4, 'modeling': 16, 'translation': 35, 'sentiment': 25, 'analysis': 0}

Bag of Words: 

 [[0 1 1 0 0 1 0 0 0 0 0 1 0 0 0 0 0 0 1 1 0 0 0 1 1 0 1 0 0 0 0 1 0 1 1 0
  1 0]
 [0 0 0 1 0 0 0 1 1 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 1 1 0 0 1 1 0 0
  0 1]
 [1 0 0 0 1 0 1 0 0 1 0 1 1 1 1 0 1 1 0 0 1 1 1 0 0 1 0 1 0 0 1 2 0 0 0 1
  0 0]]
```

**TF-IDF:**

* A refinement of BoW that accounts for the importance of words in the entire corpus.

```

TFIDF:

 [[0.         0.2919139  0.2919139  0.         0.         0.2919139
  0.         0.         0.         0.         0.         0.22200805
  0.         0.         0.         0.         0.         0.
  0.2919139  0.2919139  0.         0.         0.         0.2919139
  0.2919139  0.         0.2919139  0.         0.         0.
  0.         0.22200805 0.         0.22200805 0.2919139  0.
  0.2919139  0.        ]
 [0.         0.         0.         0.32311233 0.         0.
  0.         0.32311233 0.32311233 0.         0.32311233 0.
  0.         0.         0.         0.32311233 0.         0.
  0.         0.         0.         0.         0.         0.
  0.         0.         0.         0.         0.32311233 0.32311233
  0.         0.         0.32311233 0.24573525 0.         0.
  0.         0.32311233]
 [0.23007057 0.         0.         0.         0.23007057 0.
  0.23007057 0.         0.         0.23007057 0.         0.1749746
  0.23007057 0.23007057 0.23007057 0.         0.23007057 0.23007057
  0.         0.         0.23007057 0.23007057 0.23007057 0.
  0.         0.23007057 0.         0.23007057 0.         0.
  0.23007057 0.34994919 0.         0.         0.         0.23007057
  0.         0.        ]] (3, 38)


IDF: 

 [1.69314718 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718
 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718 1.28768207
 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718
 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718
 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718 1.69314718
 1.69314718 1.28768207 1.69314718 1.28768207 1.69314718 1.69314718
 1.69314718 1.69314718]
```