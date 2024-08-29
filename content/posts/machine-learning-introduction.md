---
title: "Machine Learning Introduction"
date: 2024-04-09T13:28:26+05:30
description: ""
draft: false
subtitle: ""
header_img: "img/ml-banner.png"
images:
- img/ml-opengraph.png
toc: true
tags: ['Machine Learning', 'Python']
categories: []
series: []
comment: true
---

## Introduction

Machine learning is a fascinating field at the **intersection of computer science and statistics**, where computers are trained to learn from data and make decisions. 

In this introductory blog, we'll explore the basics of machine learning, its differences from deep learning and artificial intelligence, essential programming languages and libraries, and dive into some fundamental concepts and models.

## What is Machine Learning( ML )

Machine learning is a **subset of artificial intelligence** that focuses on the development of **algorithms that allow computers to learn from and make predictions or decisions based on data**. These algorithms iteratively learn patterns from data, enabling them to **improve their performance over time without being explicitly programmed**.

## How is ML different from Deep Learning ( DL )

Deep learning is a **subset of machine learning** that utilizes **neural networks** with many layers to learn complex patterns in large amounts of data. 

While deep learning is a powerful tool for tasks like image and speech recognition, machine learning encompasses a broader range of techniques, including decision trees, support vector machines, and clustering algorithms.

## How is ML different from Artificial Intelligence ( AI )

Artificial intelligence is a broad field focused on **creating machines or systems that can perform tasks that typically require human intelligence**. 

Machine learning is a subset of AI that focuses on algorithms that improve their performance over time through experience, while AI encompasses a wider range of approaches, including expert systems and natural language processing.

## Scope of ML

The scope of machine learning is vast, with applications spanning industries such as healthcare, finance, marketing, and more. **From predictive analytics to recommendation systems, machine learning techniques are being used to extract insights from data and drive decision-making in various domains.**

## How to start learning ML

To embark on your machine learning journey, begin by mastering foundational concepts and essential tools, paving the way for deeper exploration and practical application.

### Programming language - Python

Python is the **preferred programming language** of choice for machine learning for some of the giants in IT.
Python’s **built-in** libraries and** packages** provide base-level code so you don’t have to start writing from scratch. Machine learning requires continuous data processing and Python has in-built libraries and packages for almost every task. This **helps you reduce development time and improve productivity** when working with complex machine-learning applications. 

The best part of these libraries and packages is that there is zero learning curve, once you know the basics of Python programming, you can start using these libraries.

#### Python Libraries used in ML

These are a few of the basic libraries required to start with ML :

1. **NumPy**: For numerical computing and handling arrays.
2. **Pandas**: For data manipulation and analysis.
3. **Matplotlib and Seaborn**: For data visualization.
4. **Scikit-learn**: A comprehensive library for machine learning algorithms and tools.

### ML Basics

Machine learning basics encompass **essential concepts and techniques** for understanding how models learn from data, the machine learning lifecycle, various types of learning, and common evaluation metrics.

#### ML life cycle

The machine learning life cycle involves seven major steps : 

1. Gathering Data
2. Data preparation
3. Data Wrangling
4. Analyse Data
5. Train the model
6. Test the model
7. Deployment

#### Supervised learning vs Unsupervised learning vs Ensemble learning vs Reinforcement learning

| Type of Learning      | Definition                                                                                              | Example                                         |
|-----------------------|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Supervised Learning   | Supervised learning is a type of machine learning where the **model is trained on a labeled dataset**.      | Classification (e.g., spam email detection)     |
| Unsupervised Learning | Unsupervised learning is a type of machine learning where the **model is trained on an unlabeled dataset**.| Clustering (e.g., grouping customers)          |
| Ensemble Learning     | Ensemble learning **combines multiple models to improve performance**.                                      | Random Forest (e.g., combining decision trees)  |
| Reinforcement Learning| Reinforcement learning is a type of machine learning where an **agent learns to make decisions by interacting with an environment and receiving feedback in the form of rewards or penalties**.        | Training an AI to play video games              |


#### Overfitting vs Underfitting

Overfitting occurs when a **model learns to capture noise in the training data**, resulting in poor generalization to new, unseen data.

Underfitting happens when a **model is too simple to capture the underlying structure of the data**, leading to low performance on both the training and test datasets.

You can read about it in detail [here.](https://www.geeksforgeeks.org/underfitting-and-overfitting-in-machine-learning/)

#### Evaluation metrics

Evaluation metrics are used to **assess the performance of machine learning models** for example accuracy, Silhouette Score, etc.

### ML models

A machine learning model is a **program that can find patterns or make decisions from a previously unseen dataset**.

Further are some of the algorithms categorized based on the task they perform : 

#### Regression

Regression models are used to **predict continuous numerical values**. 
You can explore the following algorithms:

1. Simple linear regression
2. Multiple linear regression 
3. Polynomial regression

#### Classification

Classification models are used to **predict categorical outcomes**. 
You can explore the following algorithms:

1. Logistic regression
2. Naive Baye's classification
3. K-Nearest Neighbors classification
4. Decision tree algorithm
5. Random forest algorithm

#### Clustering 

Clustering algorithms are used to **group similar data points together**. 
You can explore the following algorithms:

1. K-means clustering
2. Hierarchical clustering
3. Density-based clustering algorithms.

### Flask

Flask is a lightweight **web framework for Python**, suitable for building web applications and APIs. You can learn how to **deploy machine learning models** using Flask, allowing users to **interact with your models through a web interface**.

You can start learning Flask from its easy-to-understand [documentation.](https://flask.palletsprojects.com/en/3.0.x/quickstart/)

## Project ideas for beginners

1. Sentiment Analysis on Movie Reviews
2. Customer Segmentation
3. Credit Card Fraud Detection
4. Spam Email Detection
5. Predicting Heart Disease

    and many more...

## Conclusion

In conclusion, machine learning is a powerful technology with the potential to transform businesses, industries, and society as a whole. By understanding its principles and techniques, you can harness the power of machine learning to solve complex problems, drive innovation, and make informed decisions in an increasingly data-driven world.

## References

1. [GeekforGeeks](https://www.geeksforgeeks.org/machine-learning/)
2. [Flask](https://flask.palletsprojects.com/en/3.0.x/quickstart/)
