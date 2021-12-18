# Summary

This project built a Naive Bayes Optimization classifier.  It was designed to predict if a name was a boy's name or a girl's name.  

The project steps were to create a feature vector from a database of names.  The labels were boy (1) or girl (-1).  The feature vectors were created using a hashing function, and from a select set of letter blocks the name features were identified with a 1 or 0 to indicate whether the feature existed or not.

Following the well-known Naive Bayes conditional prbability equation, the code was written using numpy to learn from the training set and labels.  The model was tested on a test set.  The probability that the name was a boy's name and the probability that is was a girl's name was compared, and the greater probability determined the prediction.  Finally, it was noted that the model's performance could change depending on how well the hashing function performed in creating the feature vectors.
