---
layout: page
title: truedeep
description: An approach to perform supervised crack detection using less data
img: assets/img/truedeep_logo.png
importance: 3
category: fun
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

In this discussion, we present an overview on the true image selection algorithms discussed in the <a href="https://authors.elsevier.com/a/1iDcb3PiGTPj8i">published article</a>.


 <div class="info-box">
 <h3><b>Background</b></h3>
        <p>There is significant amount of data consumption in the field on AI. Especially in the context of supervised deep learning algorithms, the
requirement of labeled data is a challenge in multiple domains. This requirement not only introduces high training and annotation costs but
also has a high environmental impact due to the carbon emissions associated with the training. One of the ways to address these issues is
reduction in the data consumption. In this discussion, will will explore the input data space.</p></div>  
<br>

<h3><center><b>Objective</b></center></h3>
Given a dataset, the goal is to select a representative subset which closely resembles the overall dataset distribution. In the context
of 2D vision based tasks, we refer to the corresponding approaches as true image selection algorithms.

<h6><b>Step 1:</b></h6> 

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/td_step1.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figures shows input images, feature extractor and the extracted feature vectors (from left to right)
        </div>
    </div>
</div>

We select a pre-trained model trained on a variety of images to use the feature representation of the input dataset images. The choice of model
depends on the use case.

<h6><b>Step 2:</b></h6> 
<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/td_step2.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figures shows feature vectors, PCA block and the corresponding low dimensional representations (from left to right)
        </div>
    </div>
</div>

We obtain a low dimensional representations of the feature vectors obtained from the step 1 using PCA.

<h6><b>Step 3:</b></h6>

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/td_step3.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figures shows all the points from the nth principal component in the format of <x,x>. Representative data samples
            are selected in such a way that is resembles the overall distribution. Blue coloured points are validation samples.
        </div>
    </div>
</div>

Firstly, a principal component is selected in the ascending order of priority. Once the principal component is fixed (say k), we compute the distance of each coordinate (corresponding to each image) from the mean coordinate and compute the root of squaue of each centered coordinate. These coordinates are then split into bins using the <a href="https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html">hist algorithms</a>.

<h6><b>Step 4:</b></h6> 

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/td_step4.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figure shows the algorithm for selection of images from each of the bins obtained from step 3. Initially, the parameters are defined and the selection percentage decreases as we iterate from the first to the last bin. All the images are combined after selection to form the representative dataset.
        </div>
    </div>
</div>


We select the representative images from the distribution in a specific dimension. It is to be noted that selecting samples/data points from multiple principal components combined doesn't aid in identifying separate images. For example, the images in one component might be far away but can be closer in another component. Therefore, we give priority of image selection in descending order of principal components. This means that the highest number of samples
can be selected from the first principal component followed by the other principal components.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/td_step4.gif" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figure shows all the points from the nth principal component in the format of <x,x>. Representative data samples
            are selected in such a way that is resembles the overall distribution. Blue coloured points are validation samples.
        </div>
    </div>
</div>

<h6>Step 5:</h6> Your representative dataset is ready. Enjoy!


<h2><center>Under Work!!!</center></h2>