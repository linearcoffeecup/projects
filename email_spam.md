# Email Spam

An email spam classifier was programmed using Python.  The classifier is binary: the email is spam or not, and the features are derived from the email databases using the hash function.  

## Logistic Regression

The logisitic regression algorithm is applied.  The underlying assumption is that the data may not be distributed Gaussian.  In this project, the probability was the sigmoid function, and the loss function was the negative log loss function.  The gradient of the loss function, and a learning rate (hyperparameter) were also programmed.  The program applied the gradient descent algorithm for the set of email features (X) and for the classification of spam or not (+1, -1) labels.  