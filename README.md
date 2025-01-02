This project aims to create a model able to predict whether or not proteins will interact or not based on their sequences.

A kaggle dataset containing around 70,000 protein pairs, was used as the data set. [https://www.kaggle.com/datasets/spandansureja/ppi-dataset](url)

A feature generator function was used to create composition features of the protein sequences.  The featues generated are numerical encodings of the different groupings of amino acids (i.e. if a protein has 4 lysine resiudes and 6 histidine residues, then it would get a basic residues count of 10).

Exploratory data analysis was performed on the feature generated dataframe.

A z-test was performed on the distribution of the different features, indicating that the sulfur content and aromatic content were the most statistically significant of the features generated (not p<0.05 however).

A random forest model was able to achieve an F1 score of .97 with the training data.

This model is hopeful for being used in antibody binding prediction if the epitope is an amino acid sequence.  Other future work might include using LSTM to feed the sequences and see if that is able to create a high scoring model.
