---
layout: Post
content-type: static
permalink: /med_grp/start/a/start
title: MD Group A Start
---

# Start
## Medical Data Annotator Group Track, Session A

In this session, you will be identifying the shape of pulmonary nodes captured on CT scans. 
In the first half of the session, you will annotate 40 images with the **min-max** annotation protocol. 
In the second half, you will annotate another 40 images with the **standard** annotation protocol.

Please read this page carefully: it provides important contextual information on pulmonary lung nodes.
After this page, you will begin the first half.

**The lung** is an important respiratory organ; inhaled air passes through the trachea and into the lungs through tabular branches (_bronchi_), which divide into successively more miniscule branchioles. The open space within the lung is the _cavity_, and the walls around it enclosing the lung are the _chest walls_.

![image](https://user-images.githubusercontent.com/73039742/196003077-2ffaa2b3-17f6-48ab-bec0-2fa48f644297.png)
<small>Diagram of a lung. Image from <a href="https://newportcts.com/thoracic-surgery/lung-cancer-surgery/lung-cancer/" target="_blank">Newport Cardiac & Thoraric Surgery</small>.

**Pulmonary nodes**, or lung nodules, are abnormal growths which form on the lung. Pulmonary nodes can form from any number of causes, including the calcification of granuloma (clumps of cells) from inflamed lung tissue, fungal infections, and tumors. While most lung nodules are not cancerous, they can indicate the possibility of lung cancer. These nodes appear on imaging scans; the size and shape of the node is strongly correlated with this possibility.
  
![image](https://user-images.githubusercontent.com/73039742/196003521-d8fd8cac-a840-4ed3-8149-8b5bfc585225.png)
<small>An annotated example of a lung CT scan. Note that these are horizontally taken slices / cross-sections. Image modified from <a href="http://www.diagnijmegen.nl/index.php/Lung_Cancer" target="_blank">Diagnostic Image Analysis Group</a>.</small>

> "A spot on the lungs usually refers to a pulmonary nodule. This is a small, round growth on the lungs that shows up as a white spot on image scans. Typically, these nodules are smaller than three 3 centimeters (cm) in diameter. If your doctor sees a pulmonary nodule on a chest X-ray or CT scan, don’t panic. Pulmonary nodules are common, and most are benign or noncancerous. Nodules are found on up to half of all lung CT scans. When a pulmonary nodule is cancerous, the spot or growth is usually larger than 3 cm or has other characteristics like an irregular shape. ... The risk for cancer increases when... a nodule is large [or] the nodule appears to have lobes or a pointed surface."

> - [Healthline](https://www.healthline.com/health/spot-on-the-lung){:target+"_blank"}

Computer vision models can automatically sweep through large amounts of lung scan data to identify and characterize pulmonary lungs, which can be considered in aggregate by a radiologist to make a judgement. Because the specific shape and size of a lung node is important to characterizing its likelihood of being cancerous, it is important that such computer vision models are trustworthy - when the model encounters an ambiguous context in which it simply cannot make a confident prediction, this lack of confidence is communicated. Current standard medical computer vision models lack strong uncertainty representation measures.
  
![image](https://user-images.githubusercontent.com/73039742/196003577-36cede03-d595-4b32-ac18-a82765359b76.png)
<small>An example of lung CT scans with lung nodes bounded by black boxes. From "Automated Lung Nodule Detection and Classification Using Deep Learning Combined with Multiple Strategies", Nasrullah et al.</small>

You will be annotating modified images from the Lung Image Database Consortium and Image Database Resource Initiative ([LIDC-IDRI](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3041807/){:target="_blank"}) dataset. This large-scale collaborative effort contains many Computed Tomagraphy (CT) scans of many different types of lung nodules. **You do not need to localize** (find) **where the lung nodes are**; rather, you will be presented with a subregion which is **guaranteed to contain a centered lung node**. Your responsibility is to annotate the border of the subregion. Rephrased, you already know that every lung contains a pulmonary nodule and that the relevant node is centered, but you must find its shape and size.
  
Four such samples are displayed below. Note that each contains a centered node, which can be identified as a bright gray-ish cluster extending into the cavity which may or may not be connected to a wall or a branch. The nodules vary widely in location, shape, and size.
  
![image](https://user-images.githubusercontent.com/73039742/196003914-94dba8ff-af48-4acd-8a4a-b0f946df0ca9.png)

**Take this short quiz to evaluate your understanding.**

Next, you will proceed to annotating your first batch of 40 images. [Let's Go →](/muadocs/med_grp/a/1_annotate_standard.md)

