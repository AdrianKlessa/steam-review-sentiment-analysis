### Steam review sentiment analysis

This repository contains code for training multiple models for analysing the sentiment of Steam game reviews, predicting if they are positive or negative based on their text content alone.

Models trained & compared:

- FNN using pretrained FastText embeddings
- FNN using a TF-IDF vectorizer
- (Bidirectional) LSTM
- Pretrained Hugging Face pipeline (Transformer model)

F1 scores:

- FNN + TF-IDF: 0.90
- FNN + FastText: 0.82
- Bidirectional LSTM: 0.91
- Bert Base Multilingual Uncased Sentiment: 0.91 

Random note:

It appears that the LSTM picked up some of the more interesting quirks of the language used in Steam reviews. For example, ♥ is used to censor cursewords. Consequently, a review that consists solely of "♥♥♥♥" is considered a bad review, while "I ♥ this game" is positive. "F" is negative and "W" is positive.  

---

Dataset used:
    
    Antoni Sobkowicz. (2017). Steam Review Dataset (2017) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.1000885
    License
    
    CC BY NC 4.0