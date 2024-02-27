---
layout: page
title: SimPGen
description: Understanding performance and data from a model's perspective
img: assets/img/dtsim_logo.png
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
    
    table {
      font-family: Arial, sans-serif;
      border-collapse: collapse;
      width: 100%;
    }

    th, td {
      border: 1px solid #dddddd;
      text-align: left;
      padding: 8px;
    }


    </style>
</head>

<div class="info-box">
<h3><b>Background</b></h3>
<p>
Model performance on unseen data determines the strength of the solution used for automation. An understanding of model behaviour and the relationship
of data with generalizaion and performance can help in improving the autonomous solutions and designing the continual learning framework for the 
model. We explore the relation between model, data, performance and generalization by considering various tasks like semantic segmentation, scene
understanding and person re-identification. One of the proposed techniques is to compute a distance metric between two datasets and also between an image
and dataset. If the training data is taken into consideration, the distances of unseen images and datasets can be computed from the training data (referred
as primary dataset in the published article). In the further sections, we show the computation of these distances which can be used for experiments focused
on the relationship with model and its generalization (see article for more details). 

</p></div>  
<br>

We will discuss the distance computation approach proposed in the article. The idea is to obtain the feature representations of each image from the two datasets in consideration, namely primary and secondary. The feature representations are flattened and passed into a dimensionality 
reduction process to obtain low dimensional representations of each image from the two datasets. A distance matrix can be obtained by comparing each image from one dataset against that of all the images from the other dataset. The sum of all the distance of an image from the other dataset is referred as Idist (image-dataset distance) and the mean of Idist of all images in a dataset from another dataset is referred as Odist (dataset-dataset distance).

<h1>To be updated!</h1>