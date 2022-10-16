---
layout: Post
content-type: static
permalink: /about
title: About
---

# Study Motivation and Information

Medical imaging is essential to timely and accurate medical diagnosis and prognosis. A wide number of noninvasive or minimally invasive imaging methods - such as X-rays, Medical Resonance Imaging (MRI) scans, and Computed Tomography (CT) scans - can capture the internal state of bodily systems along a large range of scales. Moreover, imaging techniques such as electron microscopy are also of significance to non-medical biological studies. 

Often, it is inefficient, time-consuming, or laborious for humans to manually identify features of interest, such as lesions, particular cell types, and other biological structures or aberrations in these scans. This is especially the case for high-resolution three-dimensional scans and features of interest which are very small in size compared to the field captured by the image(s). For this reason, there has long been interest in applying computer vision to medical imaging. 

Deep learning models have somewhat recently been applied to more challenging medical imaging problems which previous 'manual' computer vision approaches struggle on, including semantic segmentation. The standard objective of semantic segmentation is to associate each pixel in an input image with a class. Semantic segmentation is often used to automatically detect and `draw'/`outline' features of interest by classifying each pixel of the image as belonging to a feature of interest or not. Such deep learning models have applications in the automated detection and precise localization of cells, lesions, tumors, and other specific biological structures.

However, often medical images are inherently ambiguous. To address contextual ambiguity, it is standard for one image to be annotated by several annotators, then compared and discussed until a single unanimous annotation is obtained through deliberation. This high-labor process is inefficient and inconsistent. Alternatively, computational computer vision methods may be used to compute the median of annotations, but this has its own problems. Uncertainty cannot be wholly resolved into certainty, and therefore it can also be difficult for the model to associate ambiguous images with the annotation collectively chosen by the human annotators after aggregation. 

Establishing detailed annotation rules in an attempt to minimize disagreement also may not suffice in high-variation contexts, where rules fail to illustrate standards or protocols in novel situations. 

As such, there is a large body of work which attempts to allow models to abstractly learn uncertainty from the dataset. Why not, however, directly mark uncertainty into the image? This is easily understandable, accessible, not restricted by dataset size and variability restrictions, and so on. It opens up the ways in which we can use uncertainty.

To summarize - many segmentation tasks in medicine and biology can be automated. However, there are several challenges throughout the segmentation modeling process:
- Annotators often disagree with each other, which leads to…
  - …greater time spent reviewing and discussing disagreements.
  - …a greater number of annotators or skill level needed to reconcile disagreements.
  - …possibly uninformative or inaccurate annotations which do not reflect the complete context.
- Models trained on aggregated labels in high-disagreement contexts may develop un-robust representations and hit performance ceilings due to the inherent difficulty of modeling the average/median aggregated annotation (arbitrariness). (This assertion has strong precedent in literature around space).
- Even assuming a model can predict a standard annotation, the result may not be useful or fully accurate in a contextual sense. That is, in ambiguous contexts, the ‘correct answer’ is not a single possibility but rather the space of possibilities.

**Research Questions.**

- **RQ 1.** Representative/informative capacity.
  - **RQ 1a.** Can a single annotator using the min/max procedure capture the range of disagreement of multiple annotators using the standard procedure?
  - **RQ 1b.** Does using the min/max procedure as opposed to the standard procedure reduce disagreement between annotations for a single image?
- **RQ 2.** User interaction.
  - **RQ 2a**. Is the min/max procedure usable to the user (relative to the standard procedure)?
	- **RQ 2b**. Is the min/max procedure efficient to use? More specifically, does it require minimally more labor and time to use the min/max as opposed to the standard procedure?
- **RQ 3.** Applicability to modeling.
  - **RQ 3a.** Does a deep computer vision model trained on automatically derived min/max labels produce usable and robust predictions, compared to models trained on data annotated with the standard-procedure? Moreover, can we derive standard predictions from min/max-style predictions to establish a relationship in information content?
  - **RQ 3b.** Does a deep computer vision model trained on min/max annotated labels produce usable and robust predictions, compared to models trained on the same data annotated with the standard-procedure?
