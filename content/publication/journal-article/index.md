---
title: 'Adapative federated learning'

authors:
- Anup Tuladhar
- admin
- Raissa Souza
- Nils D. Forkert 
author_notes:
- ""
- ""
- ""
- ""
date: "2022-05-03T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2022-07-15T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "International MICCAI Brainlesion Workshop"
publication_short: "MICCAI"

abstract: The potential for deep learning to improve medical image analysis is often stymied by the difficulty in acquiring and collecting sufficient data to train models. One major barrier to data acquisition is the private and sensitive nature of the data in question, as concerns about patient privacy, among others, make data sharing between institutions difficult. Distributed learning avoids the need to share data centrally by training models locally. One approach to distributed learning is federated learning, where models are trained in parallel at local institutions and aggregated together into a global model. The 2021 Federated Tumor Segmentation (FeTS) challenge focuses on federated learning for brain tumor segmentation using magnetic resonance imaging scans collected from a real-world federation of collaborating institutions. We developed a federated training algorithm that uses a combination of variable local epochs in each federated round, a decaying learning rate, and an ensemble weight aggregation function. When testing on unseen validation data our model trained with federated learning achieves very similar performance (average DSC score of 0.674) to a central model trained on pooled data (average DSC score 0.685). When our federated learning algorithm was evaluated on unseen training and testing data, it achieved similar performances on the FeTS challenge leaderboards 1 and 2 (average DSC scores of 0.623 and 0.608, respectively). This federated learning algorithm offers an approach to training deep learning learning models without the need to share private and sensitive patient data.

# Summary. An optional shortened abstract.
summary: Federated learning algorithms for brain tumor segmentation

tags: []

featured: true

# links:
# - name: ""
#   url: ""
url_pdf: 'https://link.springer.com/chapter/10.1007/978-3-031-09002-8_35'
url_code: 'https://github.com/lakshayt7/MIPLAB_FETS/'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.

---