---
title: Personalized and Controlled Image Generation using Diffusion models
summary: In this project, we combine three popular diffusion models into one model that can be used to generate personalized and controlled images. Pose data is used to add control and Dreambooth finetuning is used to personalize the model to new entities. Following this we introduce even more finegrained control using GliGen which connects bounding boxes, poses and new entities for superior control and personalization.
tags:
  - Deep Learning
  - Computer Vision
date: '2023-03-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Diagram
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Follow
    url: 
url_code: 'https://github.com/lakshayt7/CV_ControlImage'
url_pdf: 'https://lakshaytyagi.netlify.app/uploads/LLVM_report.pdf'
url_slides: 'https://docs.google.com/presentation/d/1i6baPgqF2AdrL912C31kI6OuOmhwUuk4RQaNseHSXVs/edit#slide=id.g1ed6e5985ce_0_11'
url_video: 'https://drive.google.com/file/d/1_NMjDR32ok6juF3xQDcHGodI86fW3fMB/view'

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:  'https://docs.google.com/presentation/d/1i6baPgqF2AdrL912C31kI6OuOmhwUuk4RQaNseHSXVs/edit#slide=id.g1ed6e5985ce_0_11'
---

# Exploring the Design Space of Diffusion Models for Human-Centered Image Generation

This project delves into the forefront of diffusion models, aiming to create controllable and personalizable methods for generating images centered around human needs and preferences. Text to Image Diffusion models are currently the state-of-the-art in terms of diversity, quality, and the level of control they offer over the generated outputs. In the realm of generative models, having precise control over what is produced is crucial, especially for applications in digital art and design.

Recent advancements, notably ControlNet and DreamBooth, have pushed the boundaries further in this respect. **ControlNet** is designed to input structural priors into the image generation process, such as pose, while **DreamBooth**'s finetuning process allows for the inclusion of custom objects into the model’s learned vocabulary. However, the potential of a unified approach that harnesses both these capabilities has been relatively unexplored until now.

## Our Approach

We propose a novel integration of the finetuning techniques of personalization approaches (DreamBooth) with the structural control provided by approaches like ControlNet. This combination highlights the importance of creating a synergy between:
- **Textual control**: The manipulation of image descriptions, word embeddings, etc., which are primarily targeted by personalization approaches.
- **Structural control**: The specification of pose, HED maps, etc., which are the focus of control approaches.

Such integration enables a higher degree of control in image generation by grounding the textual controls (identifying objects or persons) with structural controls (defining the pose or location of these objects/persons).

### Technical Innovations

To facilitate this enhanced control, we've extended ControlNet with an additional **SelfAttention layer**, allowing for effective grounding between textual and structural controls.

#### Key Contributions:

1. **Unified Finetuning Step**: Merging the separate finetuning processes required for personalization and structural control into a single, streamlined step.
2. **Text-grounded ControlNet**: A new architecture that can link structural cues, like poses, with textual queries (e.g., the name of an entity).

## Extended Possibilities

Our findings show that combining multiple ControlNets can offer more nuanced control, as demonstrated in our experiments where background and pose are integrated seamlessly. However, challenges in generalizing to new entities were observed, highlighting an area for improvement.

### Integrating with GliGen

We further refined our approach by integrating with GliGen, enhancing the model’s ability to faithfully follow text prompts by better associating structural control with textual descriptions. This integration not only improved the alignment between textual and structural controls but also allowed the generation of images featuring entities previously unknown to the model.

## Conclusion

This project represents a significant step forward in human-centered image generation, offering a glimpse into the potential of combining personalization with structural control for more tailored and expressive digital creations. Our developments pave the way for more intuitive and accessible generative models, promising a future where technology can more closely align with human creativity and imagination.
