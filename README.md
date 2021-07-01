# Experiment on Breast Cancer Classification

## About

Deep learning application developed using *python* and *Keras* with the aim of diagnosing breast cancer

## Description

Based on the results and the network presented in this [paper](https://arxiv.org/abs/1811.04241), I conducted an experiment on breast cancer classification.<br>
I trained different *KNN* classifiers and deep models using the *BreakHis* dataset.

To achieve this, I used well-known deep-learning frameworks for [*python*](https://www.python.org/) such as:

- [TensorFlow](https://www.tensorflow.org/)
- [Keras](https://www.tensorflow.org/api_docs/python/tf/keras)
- [scikit-learn](https://scikit-learn.org/)

The goal of this work is to compare the performance of 4 different deep models that should perform well with images:<br> BreastNet, VGG16, VGG19, Inception-ResNet.<br>
In details, the *Inception-ResNet* shares some observations made to build the network *IRRCNN* presented by the main paper.
While in the last three cases the neural network implementation is directly provided by *Keras*, the former was presented in 2019, through the following [paper](https://www.sciencedirect.com/science/article/pii/S0378437119319995), and was implemented in *python* by the same researchers (see [*breastnet.py*](https://github.com/dariocurr/dl_project/blob/main/breastnet.py)).<br>

Because of the small number of images contained in the dataset (7909 images), I used data augmentation, that is a regularization method, before feeding the networks.<br>
Also, as optimizer I used *SGD* with 0.9 *momentum* and *decay*, since from the papers I read it seems to be a well-performing optimizer and kind of a standard for this type of data. 

<br>

NB: in order to replicate this experiment you need to download the [*BreakHis* dataset](https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/), extract it in a folder named *data*.

<br>

<br>

Sections:

1. Preprocessing


2. KNN classification


3. Data augmentation


4. Deep models

    1. Hyperparameters
    2. [BreastNet](https://www.sciencedirect.com/science/article/pii/S0378437119319995)
    3. [VGG16](https://arxiv.org/abs/1409.1556)
    4. [VGG19](https://arxiv.org/abs/1409.1556)
    5. [Inception-ResNet](https://arxiv.org/abs/1602.07261)


5. Comparison of results


6. Conclusion and further experiments
