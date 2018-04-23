---
title: Splitting participants by performance and learning
category: descriptive
doctype: entry
entrynum: 3
---

[Figure 3.1](#f-3-1) shows how the subjects from each of the groups performed on each of the learnable tasks during the training stage (PC training), on the test (PC testing) or during the last 15 trials of free play (group F), as well as how well they learned (dPC). The last row shows the distributions over the entire data collapsed across groups and tasks.

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='1'
    label='PC and learning for each task split by group [N bins = 11]<br>(left = PC training, middle = PC test, right = dPC)' %}
[![train_test_delta_PC]({{site.baseurl}}/img_compressed/train_test_delta_hists_10_10.svg)]({{site.baseurl}}/img/train_test_delta_hists_10_10.svg)

#### Notes
- Both PC training and PC test *appear* bimodal.
- **However**, since the number of trials is fixed at 15, it is might be more appropriate to use 15 + 1 bins for our PC histograms, so that we can see the distribution of all and only possible PC values. The figure below ([Figure 3.2](#f-3-2)), shows the same data, but with a more appropriate number of bins (each of width 1/15).
    - Now, bimodality is much more subtle and doesn't quite show when all data is combined

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='2'
    label='PC and learning for each task split by group [N bins = 15 + 1]<br>(left = PC training, middle = PC test, right = dPC)' %}
[![train_test_delta_PC]({{site.baseurl}}/img_compressed/train_test_delta_hists_15_15.svg)]({{site.baseurl}}/img/train_test_delta_hists_15_15.svg)
