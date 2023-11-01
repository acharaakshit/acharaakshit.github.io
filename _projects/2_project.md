---
layout: page
title: SHM
description: Time-series analysis of structural sensor data
img: assets/img/shm_pfolio.png
importance: 2
category: work
---

A tool providing Machine Learning and Signal Processing based algorithms 
for observation of a system over time using periodically sampled dynamic 
response measurements from an array of sensors. The damage senstitive 
features are extracted from these measurements and statistically analysed.
The source code is available on <a href="https://github.com/acharaakshit/Structural-Health-Monitoring">Github</a>.

<style>
    body {
        font-family: Arial, sans-serif;
        margin: 20px;
    }

    h3 {
        text-align: center;
    }

    table {
        width: 80%;
        margin: 0 auto;
        border-collapse: collapse;
    }

    th, td {
        padding: 8px;
        border: 1px solid #ddd;
        text-align: left;
    }
</style>

<h3>Signal Processing and Smoothing Methods</h3>

<table>
    <tr>
        <th>Signal Processing Methods</th>
    </tr>
    <tr>
        <td>
            <ul>
                <li>Custom Recursive Cooley FFT</li>
                <li>Cooley Tukey FFT (from numpy fft library)</li>
                <li>Haar Wavelet-based Transforms</li>
                <li>Signal Reconstruction and Denoising using DWT and IDWT</li>
            </ul>
        </td>
    </tr>
    <tr>
        <th>Methods of Smoothing</th>
    </tr>
    <tr>
        <td>
            <ul>
                <li>Moving Average</li>
                <li>Exponential Smoothing</li>
                <li>Trend Exponential Smoothing</li>
                <li>Trend and Seasonal Exponential Smoothing</li>
                <li>ARMA (AutoRegressive Moving Average)</li>
                <li>ARIMA (AutoRegressive Integrated Moving Average)</li>
            </ul>
        </td>
    </tr>
</table>

<br/><br/>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/bexp.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Basic Exponential Smoothing
</div>
<br/><br/>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/bma.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Moving Average Smoothing
</div>