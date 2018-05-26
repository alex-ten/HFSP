---
title: What happens around switches?
category: other
doctype: entry
entrynum: 2
---

It is interesting to see what people do just before and right after switching to a new task. [Figure 2.1](#f-2-1){:.animated} shows the probability of error around switch trials. The figure contains 2 versions. 

To make the first version (a), I first removed all subjects who had at least one streak length shorter than 5. I then computed the probability of error on each of the 5 trials before and after switching for each subject, getting an averaged vector for each subject. Next, I averaged each trial across subjects and plotted these averages for each group. Error bars represent 1 SEM.

Getting rid of outliers by minimum streak length resulted in the removal of 85 subjects, leaving 114 and 131 subjects in F and S groups, respectively. In contrast to this conservative filtering, I have replotted the same information, but this time filtering out bad switch trials only (instead of throwing out the entire subject's data). The results are in the sub-figure (b).

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    label='Errors before and after switching' %}
{% include carousel2.html thumbnails='true' path='img/errors_around_switch_v2.svg::img/errors_around_switch_v1.svg' %}

#### Notes
- Quite surprisingly, the first couple of trials right before the switch are associated with higher probability of errors.
- Switching in F and S groups seems to be preceded by different error trajectories. Subjects in the S group play at a constant error rate and switch after more errors, while subjects in S group seem to improve their performance before starting to commit more errors and switching.
- Performance right after switching seems to be identical for the two groups.

For each subject I also calculated the average pre-switch and post-switch error rate across all of his or her (good) switches. The difference between the average pre-switch and post-switch error rates reflects the tendency to switch to the task on which the subject performs better or worse. E.g. if the subject commits more errors right after switching than immediately before, his or her difference score will be negative, reflecting challenging oneself more. [Table 2](#f-2){:.animated} shows group means of these difference scores (again, for each of the filtering approaches).

{% include caption.html 
    obj='table'
    num=page.entrynum 
    label='Average difference between pre- and post-switch error rates' %}
    
|   | (a) filtering subjects | (b) filtering switch trials  |
|:-:|:----------------------:|:----------------------------:|
| F |      0.008 (0.183)     |         -0.011 (0.187)       |
| S |     -0.041 (0.155)     |         -0.033 (0.164)       |
|============================|==============================|
|                            |                              |
{: .apa : align='center' : id='t-2'}

It seems like there is pattern. Free-exploration group seems to stay on the same level of challenge, but the S group appears to challenge itself. Filtering strategy matters. A simple independent-samples, two-tailed *t*-test shows a significant difference (&#945;=.05) between sample means when we remove subjects (*t* = 2.263, *p* = 0.02451), but not when we remove trials (*t* = 1.109, *p* = 0.26803).
