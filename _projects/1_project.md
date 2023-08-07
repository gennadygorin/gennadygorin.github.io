---
layout: page
title: Theory 
description: Unifying sequencing analyses with foundational stochastic theory
img: assets/img/12.jpg
importance: 1
category: work
related_publications: gorin_studying_2023,gorin_length_2023,gorin_distinguishing_2023
---

Single-cell workflows have been evolving at tremendous pace — yet data interpretation has been lagging behind in important ways. Conventional analyses take inspiration from the computer science field, using methods from signal processing and graph theory. But gene expression violates many of these methods' assumptions: it is high-dimensional, discrete, and sparse. Even if the current methods work acceptably _some_ of the time, I strive to characterize their limits and failure modes to understand how to build on them.

The observed experimental readouts combine biological variability due to cell type heterogeneity, transcriptional bursting, and single-molecule stochasticity, as well as technical variability due to imperfect sequencing, batch effects, and many as of yet uncharacterized sources of variation. To appropriately attribute and exploit differences in expression, we need to understand the contributions of biological and technical effects.

My Ph.D. work has focused on developing a suite of interpretable, tractable models that combine the mechanisms of single-cell biology with the technology of single-cell RNA sequencing in a common stochastic framework. This approach brings the foundations of sequencing in line with theory developed for fluorescence transcriptomics, and confers two advantages.

First, the mechanistic approach uses more of the data and provides more information than the descriptive approach. For example, instead of talking about differences in average gene expression, we can directly attribute those differences to changes in specific transcriptional parameters. To that end, I have implemented the *Monod* software package and used it to characterize subtle differences in biophysical processes which would otherwise be undetectable.

Second, it provides a principled way to ask questions of standard workflows, clarify their performance, and build better tools. I have used this approach to characterize the limitations of standard methods. For example, dimensionality reduction methods make severe assumptions, leading them to discard biologically meaningful variability. RNA velocity uses the outputs of dimensionality reduction workflows to visualize its results, leading to potentially flawed conclusions.

<!-- 
Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %} -->
