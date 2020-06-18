---
layout: post
title: "AWS - SageMaker: Sentiment Analysis"
date: 2020-06-10
---

### Summary

Using Amazon Sagemaker, build and deploy a simple PyTorch deep learning model for sentiment analysis in the cloud environment. This post outlines the steps necessary to perform the operation. Acutal execution can be done by copying the notebook from the repo(Add Github Repo).

### Outline

1. Data Aquisition - Retrieve, Processs and Upload
   - The downloaded data should be split into train & test sets
   - Python modules such as nltk is used to filter the significant words of each reviews.
   - These word groups are now feature engineered to word_dict vector where occurence of 5000 common words are monitored
   - These transformed dataset are uploaded into S3 storage for SageMaker access
2. Model Building - Build, Train and Deploy
   - PyTorch has built-in LSTM layers for NLP inference
   - LSTM: Hidden layers exist along with the outputs to serve as a memory-like cell that carries through each iteration
   - The model is trained and deployed using `sagemaker.pytorch`
   - The trained model is then deployed as an SageMaker instance
3. Model Access and Usage
   - Through the instance endpoints, we can access the deployed model for our own predictions

### Tools

- Python: Sklearn (XGBoost, lasso, ridge)

<span class="improved">Link</span> [Github Notebook](<https://github.com/maerory/AWS-SageMaker-practice/blob/master/Sentiment%20Inference%20(Pytorch-LSTM)/SageMaker%20Project.ipynb>)
