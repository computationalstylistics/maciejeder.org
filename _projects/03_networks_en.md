---
layout: project
title: Bootstrap Consensus Networks
description: A stylometric method to visualize similarities between texts in the form of a network.
thumbnail: network_thumbnail.jpg
permalink: /projects/networks/
ref: networks
lang: en
---


<div>
    <img class="col three left" src="{{ site.baseurl }}/assets/img/network.jpg" alt="" title="Bootstrap consensus network of 124 ancient Greek texts (prose, poetry, drama)"/>
</div>
<div class="col three caption">
    Fig. 1: Bootstrap consensus network of 124 ancient Greek texts (prose, poetry, drama).
</div>



Stylometry – to give as concise a definition as possible – is about comparing countable language features in written texts, in order to find groups of similar works. No matter if such a setup is involved to determine the authorship of an anonymous text, or to tell apart different literary genres, the general goal is quite the same: one is interested in linking similar texts so that they form distinct groups.

There are many methods to solve the above task, including Hierarchical Cluster Analysis, or Multidimensional Scaling. The current project was aimed at overcoming their limitations, with a little help of network analysis methodology. The underlying idea was as follows: let the algorithm establish for every single node a strong connection to its nearest neighbor (i.e. the most similar text) and two weaker connections to the 1st and the 2nd runner-up. Consequently, the final network will contain a number of weighted links, some of them being thicker (close similarities), some other revealing weaker connections between samples. The second algorithm performs a large number of tests for similarity with different number of features analyzed (e.g. 100, 200, 300, ..., 1,000 MFWs). Finally, all the connections produced in particular “snapshots” are added, resulting in a consensus network. 

A detailed overview of the project is provided [in this post](https://computationalstylistics.github.io/projects/bootstrap-networks/).  For a comprehensive explanation of the method’s theoretical assumptions, features, and implementation refer to the following paper:

> **Eder, M.** (2017). [Visualization in stylometry: cluster analysis using networks](http://dsh.oxfordjournals.org/content/early/2015/12/02/llc.fqv061). _Digital Scholarship in the Humanities_, **32**(1): 50–64, [[pre-print](https://github.com/computationalstylistics/preprints/blob/master/m-eder_visualization_in_stylometry.pdf)].
