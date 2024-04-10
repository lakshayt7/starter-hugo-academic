---
title: Scalable Active Learning for NLP
summary: Active Learning algorithms are often not compatible with recent advances in NLP. This project is an attempt to develop a scalable active learning algorithm that works with transformer based models and can be used for natural language processing
tags:
  - Deep Learning
  - Natural Language Processing
date: '2024-03-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Diagram
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Follow
    url: https://github.com/lakshayt7/active-Learning-NLP/
url_code: 'https://github.com/lakshayt7/active-Learning-NLP/'
url_pdf: ''
url_slides: 'https://docs.google.com/presentation/d/1bcm87lluuded7d5EMpM0E0w6_YZB__bE867Hao7tCL8/edit#slide=id.g1ec5d21e5cc_0_6'
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:  ''
---

# Scalable Active Learning Algorithm for Large Datasets with Transformers

## Overview

Active learning algorithms traditionally struggle to scale with large datasets, posing a significant challenge in fields requiring analysis of millions of data points, such as medical data analysis. This project introduces a scalable active learning algorithm designed to efficiently handle large datasets and compatible with advanced neural network architectures like transformers.

## The Challenge with Active Learning

Active learning is a semi-supervised machine learning approach that iteratively selects a subset of data to be labeled for training. The goal is to achieve high accuracy while minimizing the labeling effort. However, most active learning techniques falter when faced with the scale of data generated today, especially in areas requiring detailed analysis like medical report evaluation.

## Solution: A Scalable Active Learning Algorithm

Leveraging the principles of the **k-centers algorithm** and insights from the **coreset approach**, this project develops a novel active learning framework capable of processing millions of data points.

### Understanding the k-centers Algorithm

The k-centers algorithm is a clustering method that aims to select `k` representatives from a dataset such that the maximum distance of any point to its nearest representative is minimized. This technique is particularly useful in active learning for selecting diverse and representative samples from large datasets.

### The Coreset Concept

A coreset is a compact summary of a dataset that preserves the essential properties relevant to a specific task, like clustering. The idea is to reduce the dataset size without significant loss of information, making algorithms more manageable and efficient.

## Implementation with Transformers

To adapt the k-centers algorithm for use with transformers, we utilize a pretrained BERT model fine-tuned on a dataset of 3.5 million medical reports. This allows for generating high-quality embeddings that capture the nuances of medical language.

### Selection Process

Utilizing the k-centers algorithm, the best embeddings are chosen to represent the dataset. These selected data points are then labeled by GPT-4 for multi-label pathology classification, making the process suitable for detailed analysis of medical reports.

### Training and Iteration

The data labeled by GPT-4 serves as training input for further refining the BERT model. This cycle repeats, enhancing the model's accuracy and efficiency, embodying the principles of active learning by iteratively improving with each labeled dataset.

### Optimization with FAISS

To overcome the computational challenges of the k-centers algorithm on a large scale, this project employs vectorization techniques through FAISS (Facebook AI Similarity Search). This accelerates the selection process, enabling our active learning algorithm to scale effectively with large datasets.

## Conclusion

This project's development of a scalable active learning algorithm marks a significant advancement in handling vast datasets with transformers, particularly in the critical field of medical report analysis. By integrating sophisticated clustering techniques with the latest in neural network architectures, we pave the way for more efficient and accurate machine learning models capable of dealing with the complexities of modern data landscapes.
