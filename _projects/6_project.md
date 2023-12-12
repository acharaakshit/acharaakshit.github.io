---
layout: page
title: truedeep
description: An approach to perform supervised crack detection using less data
img: assets/img/truedeep_logo.png
importance: 3
category: fun
---

In this discussion, we present an overview on the true image selection algorithms discussed in the <a href="https://authors.elsevier.com/a/1iDcb3PiGTPj8i">published article</a>.
<h3>Background:</h3>
There is significant amount of data consumption in the field on AI. Especially in the context of supervised deep learning algorithms, the
requirement of labeled data is a challenge in multiple domains. This requirement not only introduces high training and annotation costs but
also has a high environmental impact due to the carbon emissions associated with the training. One of the ways to address these issues is
reduction in the data consumption. In this discussion, will will explore the input data space.

<h3>Objective:</h3>
Given a dataset, the goal is to select a representative subset which closely resembles the overall dataset distribution. In the context
of 2D vision based tasks, we refer to the corresponding approaches as true image selection algorithms.

<h6>Step 1:</h6> 

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

<h6>Step 2:</h6> 
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

<h6>Step 3:</h6> 

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/td_step3.gif" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figures shows all the points from the nth principal component in the format of <x,x>. Representative data samples
            are selected in such a way that is resembles the overall distribution. Blue coloured points are validation samples.
        </div>
    </div>
</div>

We select the representative images from the distribution in a specific dimension. It is to be noted that selecting samples/data points from multiple principal components combined doesn't aid in identifying separate images. For example, the images in one component might be far away but can be closer in another component. Therefore, we give priority of image selection in descending order of principal components. This means that the highest number of samples
can be selected from the first principal component followed by the other principal components.


<h6>Step 4:</h6> Train your model using the representative samples and the corresponding labels.
<h6>Step 5:</h6> Enjoy!


<h2><center>Under Work!!!</center></h2>