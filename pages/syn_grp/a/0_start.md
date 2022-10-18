---
layout: Post
content-type: static
permalink: /syn_grp/a/start
title: SD Group A Start
---

# Start
**Synthetic Data Track, Session A**

In this session, you will be annotating clusters in synthetically generated images. The task simulates the challenges of annotating medical images but displaces the source of uncertainty solely to ambiguous objectness.
In the first half of the session, you will annotate 40 images with the **standard** annotation protocol. 
In the second half, you will annotate another 40 images with the **min-max** annotation protocol.

## [1] The Task
In this task, you will be presented with artificially synthesized images of 'blobs' or 'masses'. These blobs are meant to abstractly emulate the challenges of annotating medical images data.

**A blob is a densely connected collection of unified masses**. Your task is to annotate the large blob in the center of the image. The challenge is determining whether surrounding structures should be included in the boundary or not. This boundary discrimination / structure inclusion ambiguity is common in real-life medical image annotation problems. For instance, consider the following image:

![image](https://user-images.githubusercontent.com/73039742/196100476-6edaf92f-5331-4071-bfd2-5ce32a8367cf.png)

The following region marked in red is certainly part of the blob. It is relatively uniform and dense.

![image](https://user-images.githubusercontent.com/73039742/196100745-0ed0b2a9-323a-4de0-b9cc-8cce0eaf566f.png)

On the other hand, these other appendages may or may not be part of the blob.

![image](https://user-images.githubusercontent.com/73039742/196101143-b3bf886e-a645-4d04-9f50-9743b7c420cd.png)

Therefore, if one had to provide a single continuous annotation, all of the following would be valid. Ultimately, **which annotation is drawn depends on the annotator's conception of what "looks the most right"**.

![image](https://user-images.githubusercontent.com/73039742/196101483-a158dc86-15e2-42de-ac24-47bf5f5bb9dd.png)

As an annotator, you must use your intuition about objectness to determine the shape and size of the center blob. Imagine that the entities you see in the images are fluid particles in a two-dimensional space: intuit the physics of these particles. It is possible that particles can be very close together but not be the same object, but it is also possible that nearby particles are still separate despite close proximity. 

> **Tip 💡**. To determine if appendages are part of a blob, candidates, or definitely not part of the blob, zoom out a lot and take a quick glance. Zooming out helps you compare objectness against neighbors.

In your establishment of the separation between blobs, **be aggressive and intuitive**: take a brief overall look at the separation, and if they two masses do not look like they would be jointly connected particles, do not consider them as possibly connected. Don't overthink it!

## [2] Short Quiz
**Take this** [**short quiz**](https://docs.google.com/forms/d/e/1FAIpQLSc2iu8S33Uz5YzCGWmItfL5jWV1-h91Ol24dQYVdNavIQOFdg/viewform?usp=sf_link){:target="_blank"} to evaluate your understanding. If you make any mistakes, make sure you understand why!

## [3] Proceed

Next, you will proceed to annotating your first batch of 40 images. [Let's Go →](/muadocs/syn_grp/a/annotate)
