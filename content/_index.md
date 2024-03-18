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
  - block: features
    content:
      title: Skills
      items:
        - name: Python
          icon: python
          icon_pack: fab
          description: 9/10
        - name: C++
          icon: code
          icon_pack: fas
          description: 8/10
        - name: SQL
          icon: bars
          icon_pack: fas
          description: 8/10
        - name: Machine Learning
          icon: robot
          icon_pack: fas
          description: 10/10
        - name: Computer Science
          icon: computer
          icon_pack: fas
          description: 9/10
        - name: Statistics
          icon: chart-simple
          icon_pack: fas
          description: 8/10
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
          company_logo:
          location: NY, NY
          date_start: '2023-03-15'
          date_end: '2024-03-15'
          description: |2-
            * Developed Large Language Model (LLM) solutions for labeling medical reports with labels along with explanations
            * Trained LLAMA-2 using LORA with distributed GPU training in PyTorch to improve Macro F1 score to 0.89

        - title: Research Internship
          company: University of Calgary, Mitacs Globalink 
          company_url: ''
          company_logo: 
          location: Calgary, Canada
          date_start: '2021-05-13'
          date_end: '2021-08-10'
          description: |2-
            *  Set up distributed training framework for UNet-based federated learning models in brain tumor segmentation
            * Achieved Dice Similarity Coefficient of 0.674 using variable local tuning of client parameters implemented in PyTorch

         
        - title: Machine Learning Intern
          company: Samsung Research Institute Bangalore
          company_url: ''
          company_logo: 
          location: Bangalore, India
          date_start: '2020-05-15'
          date_end: '2020-07-22'
          description: |2-
            * Implemented Autoencoder-based deep learning models in TensorFlow for denoising grainy, low-light videos
            * Achieved State of the Art SSIM of 0.89 and PSNR of 30.14 in high-quality video generation using perceptual loss

        - title: Software Development Intern
          company: IITK Summer of Code
          company_url: ''
          company_logo: 
          location: Kanpur, India
          date_start: '2018-05-15'
          date_end: '2018-07-22'
          description: |2-
            * Worked with a team of five members on developing a Web-App for taking attendance using facial recognition
            * Implemented real-time facial recognition using Microsoft Azure Face API and OpenCV
            * Developed a portal with a relational database for registration and viewing attendance using Django and added email support for notifications
    design:
      columns: '2'
  - block: accomplishments
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Accomplish&shy;ments'
      subtitle:
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: https://www.coursera.org
          date_end: ''
          date_start: '2021-01-25'
          description: ''
          organization: Coursera
          organization_url: https://www.coursera.org
          title: Neural Networks and Deep Learning
          url: ''
        - certificate_url: https://www.edx.org
          date_end: ''
          date_start: '2021-01-01'
          description: Formulated informed blockchain models, hypotheses, and use cases.
          organization: edX
          organization_url: https://www.edx.org
          title: Blockchain Fundamentals
          url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
        - certificate_url: https://www.datacamp.com
          date_end: '2020-12-21'
          date_start: '2020-07-01'
          description: ''
          organization: DataCamp
          organization_url: https://www.datacamp.com
          title: 'Object-Oriented Programming in R'
          url: ''
    design:
      columns: '2'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
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
        - name: Other
          tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: markdown
    content:
      title: Gallery
      subtitle: ''
      text: |-
        {{< gallery album="demo" >}}
    design:
      columns: '1'
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
  - block: collection
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  - block: tag_cloud
    content:
      title: Popular Topics
    design:
      columns: '2'
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
