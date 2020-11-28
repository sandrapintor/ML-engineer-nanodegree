## Machine Learning Engineer Nanodegree

# Project 2: Deploy a Plagiarism Detector

**Project Overview**

This project aims to develop and deploy a plagiarism detector that examines a text file and performs binary classification; labeling that file as either plagiarized or not, depending on how similar the text file is to a provided source text.

This project is broken down into three main notebooks:

1. **Notebook 1: Data Exploration**
   
    * Load in the corpus of plagiarism text data.
    * Explore the existing data features and the data distribution.


2. **Notebook 2: Feature Engineering**
   
    * Clean and preprocess the text data.
    * Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
    * Select "good" features, by analyzing the correlations between different features.
    * Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.


3. **Notebook 3: Train and Deploy Model in SageMaker**
    * Upload train/test feature data to S3.
    * Define a binary classification model and a training script.
    * Train model and deploy it using SageMaker.
    * Evaluate deployed classifier.

## Data

The [dataset](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html) used in this project consists of a corpus of plagiarised short answers (200-300 words) to Computer Science questions. This dataset contains multiple `.txt` files. Each text file contains an answer to one short question; these questions are labeled as tasks A-E.

The corpus includes 100 documents:
* 95 answers [which represent four levels of plagiarism: "Near copy" (`cut`), "Light revision" (`light`), "Heavy revision" (`heavy`), "Non-plagiarism" (`non`)]
* 5 Wikipedia source articles (category: `orig`)

**Reference**
>Clough, P., & Stevenson, M. (2011). Developing a corpus of plagiarised short answers. *Language Resources and Evaluation*, *45*(1), pp. 5-24. http://dx.doi.org/10.1007/s10579-009-9112-1

## Repo structure
This repo includes partially-run notebooks submitted for Udacity review. All code cells are executed and display outputs, except cells which the output contained AWS account identifying information.

This repo concerning project 2 includes the following files:

* [`1_Data_Exploration.ipynb`](1_Data_Exploration.ipynb)
* [`2_Plagiarism_Feature_Engineering.ipynb`](2_Plagiarism_Feature_Engineering.ipynb)
* [`3_Training_a_Model.ipynb`](3_Training_a_Model.ipynb)
* [`problem_unittests.py`](problem_unittests.py)
* [`helpers.py`](helpers.py)
* complete training directory ([`source_sklearn`](./source_sklearn/train.py))