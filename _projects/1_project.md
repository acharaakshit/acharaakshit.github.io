---
layout: page
title: RMiniZinc
img: assets/img/rminizinc_logo.png
importance: 4
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

<div class="info-box">
 <h3><b>Abstract</b></h3>
<p>
Constraint optimization, or constraint programming, is the name given to identifying feasible solutions out of a very large set of candidates, where the problem can be modeled in terms of arbitrary constraints. <a href="https://www.minizinc.org/">MiniZinc</a> is a free and open-source constraint modeling language. Constraint satisfaction and discrete optimization problems can be formulated in a high-level modeling language. Models are compiled into an intermediate representation that is understood by a wide range of solvers. MiniZinc itself provides several solvers, for instance <a href="https://www.gecode.org/">GeCode</a>. R users can use the package to solve constraint programming problems without using MiniZinc directly, modify existing MiniZinc models and also create their own models. Please refer to the Github <a href="https://github.com/acharaakshit/RMiniZinc">repository</a> or the <a href="https://rviews.rstudio.com/2021/02/15/r-interface-for-minizinc/">blog</a> to get started. The package is available on <a href="https://cran.r-project.org/web/packages/rminizinc/index.html">CRAN</a>.
</p></div> 
<br>

<h3><center>Use-Case 1</center></h3>

The first use case is to take an existing MiniZinc model and use the RMiniZinc package to get the solutions through the MiniZinc interface that allows using multiple solvers. The users can in turn, use the solutions for the next step of their overall problem.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/rminizinc_m1.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The users can use a MiniZinc model and use the interface to compile it into FlatZinc and obtain the solutions using a suitable solver like GeCode. 
        </div>
    </div>
</div>

<h3><center>Use-Case 2</center></h3>
The second use case is to utilize the R equivalents of MiniZinc classes to construct a custom MiniZinc model in R and solve the model through the interface.

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0 text-center">
        <div class="img">
            {% include figure.html path="assets/img/rminizinc_m2.png" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="caption">
            The users can construct a MiniZinc model by using inbuilt modules, use the interface to compile it into FlatZinc and obtain the solutions using a suitable solver like GeCode. 
        </div>
    </div>
</div>
