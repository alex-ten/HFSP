---
title: Oversticking
category: outliers
doctype: entry
entrynum: 1
---

<a id="{{ page.entrynum }}"></a>
## {{ page.entrynum }}. {{ page.title }}
### {{ page.entrynum }}.1. Extreme sticking
Simple search of subjects who showed *extreme sticking* (i.e. played only one task) during free exploration detected **48 outliers**
- All, but not only extreme stickers can be seen in the right tail of the histogram below ([Figure 1.2.1](#f-1-2-1)).
- Judging by the counts, extreme sticking might be associated with instruction (see [Table 1](#t-1)). Being informed reduces extreme sticking in the strategic group, but increases it in the free exploration group

{% include caption.html 
    obj='table'
    num=page.entrynum  
    label='Extreme sticker counts split by group and condition' %}

| Group / Condition | Extreme stickers |
|:-----------------:|:----------------:|
|        F/i+       |        13        |
|        F/i-       |        17        |
|        S/i+       |        12        |
|        S/i-       |         6        |
|===================|==================|
|                   |                  |
{: .apa : align='center' : id='t-1-1'}

### {{ page.entrynum }}.2. Allocation variance

To quantify oversticking we can measure the **allocation variance** of each subject by computing the standard deviation of the number of trials that each subject played on each task. [Figure 1.2.1](#f-1-2-1) shows the distribution of allocation variance scores across all participants.

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='2.1' 
    label='Task allocation variance' %}
[![allocation_variance_raw](/img/task_allocation_variance_raw.jpg)](/img/task_allocation_variance_raw.jpg)

#### Notes:
- Relative frequency histogram of task allocation variance (std):
    - Vertical red line is the sample average of the mean choice bias scores across all subjects in all groups
    - Shaded regions represent standard deviations
    - Only the data from  free exploration trials is shown
    - For each subject I counted the number of trials played on each task and then calculated the standard deviation score of these 4 tallies.
    - To put the x-axis in perspective:
        - an extreme sticking subject who played, for example, 300 to 320 trials will have a score between 129.9 and 138.6
    - Many subjects seem to have overstuck on one task a lot more than all others, as seen by the tall column of values above 100.

Filtering the subjects by allocation variance (cutoff = 100) detected **55 outliers**, so 8 additional overstickers on top of the 48 extreme stickers. This amounts to 13.75% of participants. [Figure 1.2.2](#f-1-2-2) shows the 250 trials of free exploration of each participant in the *stickers* and the *nonstickers* groups, respectively.  Interestingly, the stickers tended to stick to 1D or to R most of the time. Nonextreme stickers (those stickers who switched at least once) seem to switch only once and for a short period of time after which they go back without switching again. 

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='2.2' 
    label='Stickers vs. Nonstickers' %}
    
[![allocation_variance_raw](/img/stickers_nonstickers.jpg)](/img/stickers_nonstickers.jpg)