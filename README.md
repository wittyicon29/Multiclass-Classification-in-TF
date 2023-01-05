# Multiclass-Classification-in-TF
Multiclass classification refers to classification tasks with more than two classes. For example, a model that predicts the type of animal in an image may have "dog," "cat," "rabbit," "bird," and "other" as classes. There are several ways to approach multiclass classification in TensorFlow. Here are a few options:

One-versus-all (OvA) classification: In OvA classification, you train K separate binary classifiers, one for each class, with all examples in a given class labeled as positive and all examples in the other classes labeled as negative. At prediction time, you compute the probability for each class by running the input data through each of the K classifiers and selecting the class with the highest probability.

One-versus-one (OvO) classification: In OvO classification, you train a binary classifier for each pair of classes. For example, if you have K classes, you would train K(K-1)/2 classifiers. At prediction time, you compute the probability for each class by running the input data through all of the classifiers and selecting the class that wins the most "battles."

Softmax regression: Softmax regression is a generalization of logistic regression that allows you to perform multiclass classification. In softmax regression, you predict the probability for each class by using the softmax function, which squashes the outputs of the K classifiers into a probability distribution.

Which approach you choose will depend on your specific use case and the requirements of your model. If you have a large number of classes, OvO classification can be computationally expensive because it requires training a large number of classifiers. On the other hand, OvO classification can often result in a more balanced model because each classifier is only trained on a small number of classes. Softmax regression is a good general-purpose approach, but it may not perform as well as OvO or OvA on some datasets.
The model is trained on the Sign MNIST dataset which contains 28x28 images of hands depicting the 26 letters of the english alphabet. The accuracy of the model is very low due to the EDA not being very thorough.
