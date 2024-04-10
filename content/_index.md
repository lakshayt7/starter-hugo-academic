---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: about.avatar
    id: about
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      # Override your bio text from `authors/admin/_index.md`?
      text:
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
       
          
        - title: Research Assisstant
          company: NYU Langone
          company_url: ''
          company_logo: nyu
          location: NY, NY
          date_start: '2023-03-15'
          date_end: '2024-03-15'
          description: |2-
            * Developed Large Language Model (LLM) solutions for labeling medical reports with labels along with explanations
            * Trained LLAMA-2 using LORA with distributed GPU training in PyTorch to improve Macro F1 score to 0.89

        - title: Data Science Intern
          company: Bayer US LLC
          company_url: ''
          company_logo: bayer
          location: Whipanny, NJ
          date_start: '2023-06-12'
          date_end: '2024-09-01'
          description: |2-
            * Trained and deployed time series forecasting models for predicting dollar sales worth more than 100 million in DataBricks and SnowFlake
            * Developed hierarchical time series models with anomaly detection to model dependency between different categories and brands of products

        - title: Research Internship
          company: University of Calgary, Mitacs Globalink 
          company_url: ''
          company_logo: mitacs
          location: Calgary, Canada
          date_start: '2021-05-13'
          date_end: '2021-08-10'
          description: |2-
            *  Set up distributed training framework for UNet-based federated learning models in brain tumor segmentation
            * Achieved Dice Similarity Coefficient of 0.674 using variable local tuning of client parameters implemented in PyTorch

         
        - title: Machine Learning Intern
          company: Samsung Research Institute Bangalore
          company_url: ''
          company_logo: samsung
          location: Bangalore, India
          date_start: '2020-05-15'
          date_end: '2020-07-22'
          description: |2-
            * Implemented Autoencoder-based deep learning models in TensorFlow for denoising grainy, low-light videos
            * Achieved State of the Art SSIM of 0.89 and PSNR of 30.14 in high-quality video generation using perceptual loss

        - title: Software Development Intern
          company: IITK Summer of Code
          company_url: ''
          company_logo: indian-institute-of-technology-kanpur-iit-kanpur9273
          location: Kanpur, India
          date_start: '2018-05-15'
          date_end: '2018-07-22'
          description: |2-
            * Worked with a team of five members on developing a Web-App for taking attendance using facial recognition
            * Implemented real-time facial recognition using Microsoft Azure Face API and OpenCV
            * Developed a portal with a relational database for registration and viewing attendance using Django and added email support for notifications
    design:
      columns: '2'

  - block: collection
    id: featured
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card

    design:
      columns: '2'
      view: compact

  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Deep Learning
          tag: Deep Learning
        - name: Computer Vision
          tag: Computer Vision
        - name: Natural Language Processing
          tag: Natural Language Processing
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false


  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      # Contact (add or remove contact options as necessary)
      email: lt2504@nyu.edu
      phone: 5513447010
      autolink: true
      # Email form provider
    design:
      columns: '2'
---
