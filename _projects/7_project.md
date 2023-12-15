---
layout: page
title: coredeep
description: Improving Crack Detection Algorithms Using Width Stochasticity
img: assets/img/coredeep_logo.png
importance: 3
category: work
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .info-box {
            border: 2px solid #3498db; /* Border color */
            padding: 20px; /* Padding inside the box */
            border-radius: 10px; /* Rounded corners */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Box shadow for a subtle lift */
            max-width: 800px; /* Maximum width of the box */
            text-align: center;
        }

        .info-box p {
            margin: 0; /* Remove default margin for better spacing */
        }
    </style>
</head>

In this discussion, we present an overview of the width stochasticity in cracks and how it can help in improving existing approaches significantly. The details are discussed in <a href="https://arxiv.org/abs/2209.04648">this article</a>.


 <div class="info-box">
 <h3><b>Background</b></h3>
        <p>Automatically detecting or segmenting cracks in images can help in reducing the cost of maintenance or operations. Detecting, measuring and quantifying cracks for distress analysis in challenging background scenarios is a difficult task as there is no clear boundary that separates cracks from the background. Therefore, the algorithms should be developed while considering the inherent challenges associated with data. Some of the perceptually noted challenges are color, intensity, depth, blur, motion-blur, orientation, different region of interest (ROI) for the defect, scale, illumination, complex and challenging background, etc. These variations occur across (crack inter class) and within images (crack intra-class variabilities). Overall, there is significant background (inter) and foreground (intra-class) variability. In this work, we have attempted to reduce the effect of these variations in challenging background scenarios using the proposed stochastic width (SW) approach.</p></div>  
<br>

 <h3><center><b>Stochastic Width</b></center></h3>

In this section, we will discuss the stochastic width approach and how it is applied on the input binary crack masks.

 <div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/coredeep_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figure shows <b>(a)</b> input image, <b>(b)</b> ground truth mask, <b>(c)</b> gt dilated with 3 x 3 kernel, <b>(d)</b> mask (c) dilated with 5 x 5 kernel and  <b>(e)</b> mask (d) dilated with 8 by 8 kernel (from left to right)
        </div>
    </div>
</div>

 <h3><center><b>Under Work!!!</b></center></h3>