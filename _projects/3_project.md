---
layout: page
title: Depth based Classification
description: Tracking the respiratory patterns for adjustable X-Rays
img: assets/img/resp.png
importance: 3
category: work
---

The static X-Rays can damage healthy cancer cells on the edge of tumor along with the cancerous cells due to the contraction and expansion of lungs. This can be addressed by using a dynamically adjustable X-Ray projection that uses the depth information during respiration. The aim of this project was to create a respiratory monitoring system to detect the depth of lungs.
This was addressed as a classification problem taking as an input, the video frames captured by
the Microsoft Kinect RGB-Depth cameras. The prior research has shown these depth cameras to be
efficient in estimating the respiratory motion with minimal errors. The frames were manually
annotated into 3 categories namely, below average, average and above average respiration. The 
period of contraction and expansion is typically higher in above average respiration allowing 
for a larger time window to project the X-rays during the expansion to avoid harm to the healthy
cells. This time window is less in the average respiration and even lesser in the below average respiration. Therefore, the accuracy of projection needs to be high in these cases. Utilizing the
VGG-16 based classifier, pretrained on imagenet, the classification accuracy on the test data was found to be 86.5%.
<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/vgg_16.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            Network architecture
        </div>
    </div>
</div>

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/transfer-learning.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            Transfer Learning (utilizing imagenet)
        </div>
    </div>
</div>

The source code is available on <a href="https://github.com/acharaakshit/Tracking-of-Lung-cancer">Github</a>.