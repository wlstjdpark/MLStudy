# MLStudy

###### Summaries and References of ["Hands-On Machine Learning with Scikit-Learn and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems"](https://github.com/ageron/handson-ml) Book

## The Book

<img align="right" src="http://akamaicovers.oreilly.com/images/0636920052289/cat.gif">

Through a series of recent breakthroughs, deep learning has boosted the entire field of machine learning. Now, even programmers who know close to nothing about this technology can use simple, efficient tools to implement programs capable of learning from data. This practical book shows you how.

By using concrete examples, minimal theory, and two production-ready Python frameworks—scikit-learn and TensorFlow—author Aurélien Géron helps you gain an intuitive understanding of the concepts and tools for building intelligent systems. You’ll learn a range of techniques, starting with simple linear regression and progressing to deep neural networks. With exercises in each chapter to help you apply what you’ve learned, all you need is programming experience to get started.

- Explore the machine learning landscape, particularly neural nets
- Use scikit-learn to track an example machine-learning project end-to-end
- Explore several training models, including support vector machines, decision trees, random forests, and ensemble methods
- Use the TensorFlow library to build and train neural nets
- Dive into neural net architectures, including convolutional nets, recurrent nets, and deep reinforcement learning
- Learn techniques for training and scaling deep neural nets
- Apply practical code examples without acquiring excessive machine learning theory or algorithm details

## Prerequisites

- Python – you don't need to be an expert python programmer, but you do need to know the basics. If you don't, the official Python tutorial is a good place to start.
- Scientific Python – We will be using a few popular python libraries, in particular NumPy, matplotlib and pandas. If you are not familiar with these libraries, you should probably start by going through the tutorials in the Tools section (especially NumPy).
- Math – We will also use some notions of Linear Algebra, Calculus, Statistics and Probability theory. You should be able to follow along if you learned these in the past as it won't be very advanced, but if you don't know about these topics or you need a refresher then go through the appropriate introduction in the Math section.

## Install

### Install packages from Windows (64-bit)

1. Install [Python 3.6.2](https://www.python.org/ftp/python/3.6.2/python-3.6.2-amd64-webinstall.exe)

2. Visit [Unofficial Windows Binaries for Python Extension Packages](http://www.lfd.uci.edu/~gohlke/pythonlibs/)

3. Install [Numpy+MKL](http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy) package
    - When install, use instruction ```pip install [.whl file]```

5. Install [Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/en-us/download/details.aspx?id=53587)

6. Install [SciPy](http://www.lfd.uci.edu/~gohlke/pythonlibs/#scipy) package

7. Install [scikit-learn](http://www.lfd.uci.edu/~gohlke/pythonlibs/#scikit-learn), [matplotlib](http://www.lfd.uci.edu/~gohlke/pythonlibs/#matplotlib), and [pandas](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pandas) packages

## Contents

- Mathematics for Machine Learning
- [Chapter 1: The Machine Learning Landscape](https://github.com/utilForever/MLStudy/blob/master/Chapter%201%20-%20The%20Machine%20Learning%20Landscape.md)
    - What Is Machine Learning?
    - Why Use Machine Learning?
    - Types of Machine Learning Systems
    - Main Challenges of Machine Learning
    - Testing and Validating
    - Exercises
- Chapter 2: End-to-End Machine Learning Project
    - Working with Real Data
    - Look at the Big Picture
    - Get the Data
    - Discover and Visualize the Data to Gain Insights
    - Prepare the Data for Machine Learning Algorithms
    - Select and Train a Model
    - Fine-Tune Your Model
    - Launch, Monitor, and Maintain Your System
    - Try It Out!
    - Exercises
- Chapter 3: Classification
    - MNIST
    - Training a Binary Classifier
    - Performance Measures
    - Multiclass Classification
    - Error Analysis
    - Multilabel Classification
    - Multioutput Classification
    - Exercises
- Chapter 4: Training Models
    - Linear Regression
    - Gradient Descent
    - Polynomial Regression
    - Learning Curves
    - Regularized Linear Models
    - Logistic Regression
    - Exercises
- Chapter 5: Support Vector Machines
    - Linear SVM Classification
    - Nonlinear SVM Classification
    - SVM Regression
    - Under the Hood
    - Exercises
- Chapter 6: Decision Trees
    - Training and Visualizing a Decision Tree
    - Making Predictions
    - Estimating Class Probabilities
    - The CART Training Algorithm
    - Computational Complexity
    - Gini Impurity or Entropy?
    - Regularization Hyperparameters
    - Regression
    - Instability
    - Exercises
- Chapter 7: Ensemble Learning and Random Forests
    - Voting Classifiers
    - Bagging and Pasting
    - Random Patches and Random Subspaces
    - Random Forests
    - Boosting
    - Stacking
    - Exercises
- Chapter 8: Dimensionality Reduction
    - The Curse of Dimensionality
    - Main Approaches for Dimensionality Reduction
    - PCA
    - Kernel PCA
    - LLE
    - Other Dimensionality Reduction Techniques
    - Exercises
- Chapter 9: Up and Running with TensorFlow
    - Installation
    - Creating Your First Graph and Running It in a Session
    - Managing Graphs
    - Lifecycle of a Node Value
    - Linear Regression with TensorFlow
    - Implementing Gradient Descent
    - Feeding Data to the Training Algorithm
    - Saving and Restoring Models
    - Visualizing the Graph and Training Curves Using TensorBoard
    - Name Scopes
    - Modularity
    - Sharing Variables
    - Exercises
- Chapter 10: Introduction to Artificial Neural Networks
    - From Biological to Artificial Neurons
    - Training an MLP with TensorFlow’s High-Level API
    - Training a DNN Using Plain TensorFlow
    - Fine-Tuning Neural Network Hyperparameters
    - Exercises
- Chapter 11: Training Deep Neural Nets
    - Vanishing/Exploding Gradients Problems
    - Reusing Pretrained Layers
    - Faster Optimizers
    - Avoiding Overfitting Through Regularization
    - Practical Guidelines
    - Exercises
- Chapter 12: Distributing TensorFlow Across Devices and Servers
    - Multiple Devices on a Single Machine
    - Multiple Devices Across Multiple Servers
    - Parallelizing Neural Networks on a TensorFlow Cluster
    - Exercises
- Chapter 13: Convolutional Neural Networks
    - The Architecture of the Visual Cortex
    - Convolutional Layer
    - Pooling Layer
    - CNN Architectures
    - Exercises
- Chapter 14: Recurrent Neural Networks
    - Recurrent Neurons
    - Basic RNNs in TensorFlow
    - Training RNNs
    - Deep RNNs
    - LSTM Cell
    - GRU Cell
    - Natural Language Processing
    - Exercises
- Chapter 15: Autoencoders
    - Efficient Data Representations
    - Performing PCA with an Undercomplete Linear Autoencoder
    - Stacked Autoencoders
    - Unsupervised Pretraining Using Stacked Autoencoders
    - Denoising Autoencoders
    - Sparse Autoencoders
    - Variational Autoencoders
    - Other Autoencoders
    - Exercises
- Chapter 16: Reinforcement Learning
    - Learning to Optimize Rewards
    - Policy Search
    - Introduction to OpenAI Gym
    - Neural Network Policies
    - Evaluating Actions: The Credit Assignment Problem
    - Policy Gradients
    - Markov Decision Processes
    - Temporal Difference Learning and Q-Learning
    - Learning to Play Ms. Pac-Man Using Deep Q-Learning
    - Exercises

## License

<img align="right" src="http://opensource.org/trademarks/opensource/OSI-Approved-License-100x137.png">

The class is licensed under the [MIT License](http://opensource.org/licenses/MIT):

Copyright &copy; 2017 [Chris Ohk](http://www.github.com/utilForever).

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
