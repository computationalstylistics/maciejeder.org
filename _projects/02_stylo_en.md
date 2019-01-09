---
layout: project
title: Stylo
description: Software to perform various analyses in the field of computational stylistics, authorship attribution, etc.
thumbnail: clustering_thumbnail.jpg
permalink: /projects/stylo/
ref: stylo
lang: en
---

<div>
    <img class="col three left" src="{{ site.baseurl }}/assets/img/clustering.jpg" alt="" title="Cluster Analysis of 66 English novels from Jane Austen to Joseph Conrad: produced using the package ‘stylo’"/>
</div>
<div class="col three caption">
    Fig. 1: Cluster Analysis of 66 English novels from Jane Austen to Joseph Conrad: produced using the package ‘stylo’.
</div>

Hidden from academic impact estimators and other bibliometric indexes, my software is
downloaded and probably used much more often than my papers are read. It applies, I believe, to the package “stylo” at the first place.

Software “Stylometry with R” (or simply “stylo”) is a flexible R package for the highlevel analysis of writing style in stylometry. Stylometry (computational stylistics) is concerned with the quantitative study of writing style, e.g. authorship verification, an application which has considerable potential in forensic contexts, as well as historical research. Because “stylo” provides an attractive graphical user interface for high-level exploratory analyses, it is especially suited for an audience of novices, without programming skills (e.g. from Digital Humanities). More experienced users can benefit from implementation of a series of standard pipelines for text processing, as well as a number of similarity metrics.

The most commonly-known and widely used functionalities of “stylo” include:
* Hierarchical Cluster Analysis, an example of which is shown in Fig. 1 above
* Principal Components Analysis
* Multidimensional Scaling
* [Bootstrap Consensus Networks]({{ site.baseurl }}/projects/networks/)
* Burrows’s Delta
* Support Vector Machines
* Nearest Shrunken Centroids
* [Rolling Stylometry]({{ site.baseurl }}/projects/rolling_stylo/)


**Authors:** Maciej Eder<sup>*</sup>, Mike Kestemont, Jan Rybicki, Steffen Pielstrom

**License:** [GPL-3](https://opensource.org/licenses/GPL-3.0)

Current officially released version of the package: 
[![CRAN Version](http://www.r-pkg.org/badges/version/stylo)](https://CRAN.R-project.org/package=stylo)

For instructions on installation and usage, please visit the [GitHub repository](https://github.com/computationalstylistics/stylo). Please also check the [teaching subpage]({{ site.baseurl }}/teaching/) on the current website, where some updates will be posted.







