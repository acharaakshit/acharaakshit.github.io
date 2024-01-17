---
layout: page
title: 3D MRI Segmentation
description: An interactive tool for MRIs with 3D Segmentation Overlay.
img: assets/img/pixel_classification.png
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
<p>An AI powered brain segmentation application that segments Gray Matter (GM), White Matter (WM), and Cerebro-Spinal Fluid (CSF) from the Neuro MR exams. The tool provides the users, a way to browse, upload and view patient MRI exams along with various viewer utilities of which semantic segmentation is an in-house developed module. The uploaded MRI exams are stored in a shared file system coupled with an indexed SQL database. There are backend services to aid with data storage, 3D segmentation and viewing the MRIs. All the services are dockerized containers and the overall architecture is platform agnostic.
</p></div>  
<br>
<h3>Functionalities</h3>

The workflows are automated. Once a user uploads a scan, it is validated, processed, stored and indexed. The segmentation module runs on the processed scans and the segmentation masks are stored in a shared file storage so that they can be rendered without any latency. Images can be re-oriented as sagittal/axial/coronal/oblique in the viewer. A detailed architecture is provided below:

 <div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/arch_final.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figure shows a detailed architecture of the web-based application.
        </div>
    </div>
</div>


<h3>Segmentation</h3>
The segmentation task is formulated as a pixel level classification task with 3 classes namely Gray Matter (GM), White Matter (WM), and Cerebro-Spinal Fluid (CSF). Remaining pixels are labeled as the background class. We solve this problem using a supervised pixel level classification approach utilizing UNet model with a pretrained ResNet50 backbone (encoder). The redundancy in in the input space is reduced by performing meaningful augmentations and training on the subset of the augmented data. A detailed flow of segmentation module is shown below:
 <div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/model_train.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The figure shows a model training and inference details for the segmentation task.
        </div>
    </div>
</div>
<br>
An overall dice score of 0.84 (mean overall all classes) is achieved on 82 unseen real-world 3D MRI scans.


<b>MRI exams and UI design are confidential property of GE and can not be shared publicly.</b>