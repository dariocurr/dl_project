# Experiment on Breast Cancer Classification

## About

[Deep learning application](/project.ipynb) developed using Python and [Keras](https://keras.io/)
with the aim of diagnosing breast cancer

## Description

Based on the results and the network presented in this
[paper](https://arxiv.org/abs/1811.04241), I conducted an experiment on breast
cancer classification.<br> I trained different _KNN_ classifiers and deep models
using the _BreakHis_ dataset.

To achieve this, I used well-known deep-learning frameworks for
[_python_](https://www.python.org/) such as:

-   [TensorFlow](https://www.tensorflow.org/)
-   [Keras](https://www.tensorflow.org/api_docs/python/tf/keras)
-   [scikit-learn](https://scikit-learn.org/)

The goal of this work is to compare the performance of 4 different deep models
that should perform well with images:<br> BreastNet, VGG16, VGG19,
Inception-ResNet.<br> In details, the _Inception-ResNet_ shares some
observations made to build the network _IRRCNN_ presented by the main paper.
While in the last three cases the neural network implementation is directly
provided by _Keras_, the former was presented in 2019, through the following
[paper](https://www.sciencedirect.com/science/article/pii/S0378437119319995),
and was implemented in _python_ by the same researchers (see
[_breastnet.py_](https://github.com/dariocurr/dl_project/blob/main/breastnet.py)).<br>

Because of the small number of images contained in the dataset (7909 images), I
used data augmentation, that is a regularization method, before feeding the
networks.<br> Also, as optimizer I used _SGD_ with 0.9 _momentum_ and _decay_,
since from the papers I read it seems to be a well-performing optimizer and kind
of a standard for this type of data.

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

## How to run

In order to replicate and to extend this experiment you need to:

1. download the
   [_BreakHis_ dataset](https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/)
2. extract it in a folder named `data`
3. build the `dev container` using the [Docker](https://www.docker.com/)
   extension of [VScode](https://code.visualstudio.com/)
4. run the [notebook](/project.ipynb)
