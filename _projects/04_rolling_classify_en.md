---
layout: project
title: Rolling Stylometry
description: A stylometric method of supervised classification, in which a given text is chunked into equal-sized blocks and then assessed sequentially.
thumbnail: rolling_thumbnail.jpg
permalink: /projects/rolling_stylo/
ref: rolling_stylo
lang: en
---



<div>
    <img class="col three left" src="{{ site.baseurl }}/assets/img/rolling.jpg" alt="" title="<i>Queen Sopia’s Bible</i> examined using Rolling Stylometry (in NSC flavor), with the following parameters: 100 MFWs, window size of 5,000 words, sample overlap of 4,500 words."/>
</div>
<div class="col three caption">
    Fig. 1: <i>Queen Sopia’s Bible</i> examined using Rolling Stylometry (in SVM flavor), with the following parameters: 100 MFWs, window size of 5,000 words, sample overlap of 4,500 words.
</div>



The Rolling Stylometry method is designed to detect stylistic takeovers. To give an example: imagine a text that is supposedly written by more than author, and you want to pinpoint the stylistic change between the individual authorial “signals”. In the case of the earliest Polish translation of the Bible knowns as _Queen Sophia’s Bible_, one might be interested in tracing the five scribal hands evidenced in the manuscript – were they “just” the scribes, or were they also involved in actual translatorial? In Fig. 1 above, one can notice that indeed, the change of a scribe (vertical dashed lines) is usually correlated by stylistic change (different colors of the strip).

The general idea is fairly simple: a text to be analyzed (e.g., an anonymous text to be attributed) is chunked into equal-sized blocks (partially overlapping). Then, instead of attributing the text in its entirety, the goal is to perform an independent similarity test for each chunk, and to inspect the results as a sequence of ordered stylistic signals. Arguably, any classification method can be combined with this procedure. However, so far, the method implementation in _stylo_ includes support vector machines (SVM), nearest shrunken centroids (NSC), and Delta in its classical Burrowsian flavor.

An overview of the project is provided [here](https://computationalstylistics.github.io/projects/rolling-stylometry/), a more detailed description, supplemented by applicable/reusable snippets of code, can be found in [this blog post](https://computationalstylistics.github.io/blog/rolling_stylometry/). For a comprehensive explanation of the method’s theoretical assumptions, features, and implementation refer to the following paper:

> **Eder, M.** (2016). [Rolling stylometry](https://academic.oup.com/dsh/article/31/3/457/1745764). _Digital Scholarship in the Humanities_, **31**(3): 457–469, [[pre-print](https://github.com/computationalstylistics/preprints/blob/master/Eder_Rolling_stylometry_draft.pdf)].

