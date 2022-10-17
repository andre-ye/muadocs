---
layout: Post
content-type: static
permalink: /snr_grp/start
title: Senior Annotator Group Start
---

# Start 
**Senior Annotator Group**

In this session, you will be identifying the shape of pulmonary nodes captured on CT scans. 
In the first half of the session, you will annotate 40 images with the **standard** annotation protocol. 
In the second half, you will annotate another 40 images with the **min-max** annotation protocol.

Please read this page carefully: it provides important contextual information on pulmonary lung nodes.
After this page, you will begin annotating the first half of images.

## [1] The Lung

**The lung** is an important respiratory organ; inhaled air passes through the trachea and into the lungs through tabular branches (_bronchi_), which divide into successively more miniscule branchioles. The open space within the lung is the _cavity_, and the walls around it enclosing the lung are the _chest walls_.
 
![image](https://user-images.githubusercontent.com/73039742/196003077-2ffaa2b3-17f6-48ab-bec0-2fa48f644297.png)
<small>Diagram of a lung. Image from <a href="https://newportcts.com/thoracic-surgery/lung-cancer-surgery/lung-cancer/" target="_blank">Newport Cardiac & Thoraric Surgery</small>.

## [2] Pulmonary Nodes and Lung Cancer
 
**Pulmonary nodes**, or lung nodules, are abnormal growths which form on the lung. Pulmonary nodes can form from any number of causes, including the calcification of granuloma (clumps of cells) from inflamed lung tissue, fungal infections, and tumors. While most lung nodules are not cancerous, they can indicate the possibility of lung cancer. These nodes appear on imaging scans; the size and shape of the node is strongly correlated with this possibility.
  
![image](https://user-images.githubusercontent.com/73039742/196003521-d8fd8cac-a840-4ed3-8149-8b5bfc585225.png)
<small>An annotated example of a lung CT scan. Note that these are horizontally taken slices / cross-sections. Image modified from <a href="http://www.diagnijmegen.nl/index.php/Lung_Cancer" target="_blank">Diagnostic Image Analysis Group</a>.</small>

> "A spot on the lungs usually refers to a pulmonary nodule. This is a small, round growth on the lungs that shows up as a white spot on image scans. Typically, these nodules are smaller than three 3 centimeters (cm) in diameter. If your doctor sees a pulmonary nodule on a chest X-ray or CT scan, don’t panic. Pulmonary nodules are common, and most are benign or noncancerous. Nodules are found on up to half of all lung CT scans. When a pulmonary nodule is cancerous, the spot or growth is usually larger than 3 cm or has other characteristics like an irregular shape. ... The risk for cancer increases when... a nodule is large [or] the nodule appears to have lobes or a pointed surface."

> [Healthline](https://www.healthline.com/health/spot-on-the-lung){:target+"_blank"}

## [3] Pulmonary Node Identification
 
Computer vision models can automatically sweep through large amounts of lung scan data to identify and characterize pulmonary lungs, which can be considered in aggregate by a radiologist to make a judgement. Because the specific shape and size of a lung node is important to characterizing its likelihood of being cancerous, it is important that such computer vision models are trustworthy - when the model encounters an ambiguous context in which it simply cannot make a confident prediction, this lack of confidence is communicated. Current standard medical computer vision models lack strong uncertainty representation measures.
  
![image](https://user-images.githubusercontent.com/73039742/196003577-36cede03-d595-4b32-ac18-a82765359b76.png)
<small>An example of lung CT scans with lung nodes bounded by black boxes. From "Automated Lung Nodule Detection and Classification Using Deep Learning Combined with Multiple Strategies", Nasrullah et al.</small>
 
## [4] The LIDC Dataset

You will be annotating modified images from the Lung Image Database Consortium and Image Database Resource Initiative ([LIDC-IDRI](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3041807/){:target="_blank"}) dataset. This large-scale collaborative effort contains many Computed Tomagraphy (CT) scans of many different types of lung nodules. **You do not need to localize** (find) **where the lung nodes are**; rather, you will be presented with a subregion which is **guaranteed to contain a centered lung node**. Your responsibility is to annotate the border of the subregion. Rephrased, you already know that every lung contains a pulmonary nodule and that the relevant node is centered, but you must find its shape and size.
  
Four such samples are displayed below. Note that each contains a centered node, which can be identified as a bright gray-ish cluster extending into the cavity which may or may not be connected to a wall or a branch. The nodules vary widely in location, shape, and size.
  
![image](https://user-images.githubusercontent.com/73039742/196003914-94dba8ff-af48-4acd-8a4a-b0f946df0ca9.png)
 
You'll see that even professional radiologists asked to annotate the shape and size of nodules often disagree with each other. In the following series of examples, the left image contains 'wider context', the middle image shows the 'restricted window' (which you will be annotating), and the right image displays different annotations for the nodule.
 
![image](https://user-images.githubusercontent.com/73039742/196005058-868494c9-c1b8-477b-833c-67b2c23e18eb.png)
 
These disagreements result from differences in visual perception: some challenges include whether to include a darker region as part of the lung node, or how much of an auxiliary structure to include if the node is attached to a broader wall or branch (where does the node end and the structure begin?).

## [5] Short Quiz
**Take this short quiz** to evaluate your understanding. [Let's Go →](https://docs.google.com/forms/d/e/1FAIpQLSdJzcB5jnq8lk4uEcsd3FxMVo1syntPm-CTUKSDxfd4a57zqw/viewform?usp=sf_link){:target="_blank"}. If you make any mistakes, make sure you understand why!

## [6] Proceed
 
Next, you will proceed to annotating your first batch of 40 images. [Let's Go →](/muadocs/med_grp/a/annotate)

