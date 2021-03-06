The aim of the project is to compare the difference between 2 known Natural Language Processing (NLP) models in regards to analyzing medical textual data. The 2 NLP models are: Word2vec and TF-IDF. The data are over 3,000 medical notes from visits to medical professionals.

For each one of the 2 NLP models there are 2 tasks, in the fields of unsupervised learning and supervised learning:
1. Unsupervised learning: Cluster the texts to clusters using K-means.
2. Supervised learning: Classify each text to the correct diagnosis. In the Word2vec model a RNN (Recurrent Neural Network) model preforms the classification and in the TF-IDF model a Random forest model does.

A database in MongoDB stores the texts and details about the final K-means clusters for each model.

Models deployed as a REST API with multiprocessing with Python and Flask. The API receives from a request an unknown medical text and returns one of the following:
1. Most common labels and closest sentences in the cluster assigned to the text according to the Word2vec & K-means model or the TF-IDF & K-means model.
2. Predicted diagnosis for the condition described in the text according to the Word2vec & RNN model or the TF-IDF & Random forest model.

Technologies used in the project: Python, PyTorch, Gensim, Scikit-learn, Flask, MongoDB.
