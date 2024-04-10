---
title: Efficient vectorized GPT document comparison 
summary: Context length of GPT model prevents the passing of two large documents directly to the API. Furthermore, reducing the number of calls and the tokens per call can save money. In this small project, I use semantic similarity to reduce the number of calls and tokens per call.
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
    url: https://github.com/lakshayt7/Efficient-GPT-comp
url_code: 'https://github.com/lakshayt7/Efficient-GPT-comp'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:  ''
---

# Text Comparison Solution Using AI and NLP Techniques

## Key Considerations

### General/Hands-off Approach

To minimize manual intervention and ensure a general applicability across various domains, our solution leverages ChatGPT for summarizing and comparing texts. This automated approach reduces the need for detailed oversight and makes the process more user-friendly.

### Scalable/Cost-effective

Our design focuses on scalability and cost-efficiency. By employing semantic search and term search, we efficiently locate relevant sections within the documents. This strategy significantly reduces the computational complexity from quadratic comparisons and minimizes the usage of API calls, leading to a more scalable and cost-effective solution.

## Solution Outline

### General/Hands-off

- **Summarization and Comparison:** Utilize ChatGPT for an automated process of summarizing and comparing two pieces of text, enabling a hands-off approach for users.

### Scalable/Cost-effective

- **Semantic and Term Search:** Leverage both semantic search and term search techniques to find pertinent sections across documents. This approach not only enhances scalability by avoiding exhaustive sentence-by-sentence comparisons but also optimizes the cost by reducing the number of required ChatGPT API calls and token consumption.

## Pipeline Details

1. **RAG-like Search:** Implement a Retrieval-Augmented Generation (RAG)-like search using the key considerations highlighted in the first document to identify similar text within the second document. The embedding comparison is optimized and vectorized using FAISS. The search employs the following models to generate embeddings, which are then compared using cosine similarity:
   - **TF-IDF (Term Frequency-Inverse Document Frequency):** A statistical measure used to evaluate the importance of a word in a document relative to a collection of documents or corpus.
   - **Sentence Embedding (BERT):** Utilizes a BERT (Bidirectional Encoder Representations from Transformers) model, specially pre-trained for generating sentence embeddings. This method effectively captures the semantic meaning of sentences.

2. **Comparison via GPT-4 with Chain-Of-Thought Prompting:** Once similar texts are identified, they are passed to GPT-4 alongside a Chain-Of-Thought prompt. This step facilitates a deep and nuanced comparison between the relevant sections of the two documents, leveraging GPT-4's advanced language comprehension capabilities.


