---
title: Performance and learnability ratings
category: descriptive
doctype: entry
entrynum: 1
---

To ascertain that the task works as intended we tested the performance during the training stage: the first 60 trials that each person received, in which they played with each family for 15 trials, receiving feedback on each trial. 

As intended, performance (PC):
- declines in order from 1D, I1D, 2D, R tasks
- is not affected by group or instruction (next slide, left column)

At the end of the training stage, each person provided a “learnability” rating for each task (which we call LRN) on a scale of 1 to 10 (lowest to highest learnability; see [Materials]({{site.baseurl}}{% link content/materials/index.md %}#2-self-reports){: .animated}).

The LRN ratings were:
- negatively correlated with PC for all tasks 
- not affected by group or instruction
- highest for the R task

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='1'
    label='Performance and Learnability ratings' %}
<table class='imagegrid'>
    <tr>
        <td>(a) PC across subjects for each task <br>split by group and condition</td>
        <td>(b) LRN across subjects for each task <br>split by group and condition</td>
    </tr>
    <tr>
        <td><a href="{{site.baseurl}}/img/pc_clean.svg"><img src="{{site.baseurl}}/img_compressed/pc_clean.svg" alt="pc_histogram" /></a></td>
        <td><a href="{{site.baseurl}}/img/lrn_clean.svg"><img src="{{site.baseurl}}/img_compressed/lrn_clean.svg" alt="lrn_histogram" /></a></td>
    </tr>
</table>

#### Notes
- The PC plots show the distribution of PC of 15 training trials over 11 bins. However, it seems more appropriate to bin the scores according to the number of trials, so that we can exactly see the frequency of each of the 16 possible values of our discrete random variable (i.e. 0/15, 1/15, ..., 15/15 correct trials).
    - [Figure 1.2](#f-1-2){: .animated} below shows the distributions of PC across subjects split by group and condition.
    
{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='2'
    label='PC across subjects for each task split by group and conditions (N bins = 16)' %}
<a href='{{site.baseurl}}/img/pc_clean-nbins16.svg'><img src='{{site.baseurl}}/img_compressed/pc_clean-nbins16.svg' alt='pc_hists_16_bins' style='width: 50%; height:auto; display: block; margin: 0 auto;/'></a>

#### Notes
- The stark bimodality seen in [Figure 1.1](#f-1-1){: .animated} disappears when we use (appropriately) more bins. Here, it seems that for each group / condition split, the mean gradually shifts toward lower values of PC as the task gets more difficult.
- These shape differences caused by a varying number of bins will be especially relevant in [section 3](#3){: .animated}