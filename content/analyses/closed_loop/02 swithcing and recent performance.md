---
title: Switching and recent performance
category: closed_loop
doctype: entry
entrynum: 2
---

[Figure 2.1](#f-2-1){: .animated} shows the relationship between switching and performance at a group level. The relationship is split by task, and different tasks are organized into rows. Within each task, there are two subplots that share an x-axis with each other. The x-axis represents the number of trials played on that task during the free play stage. The top subplot shows the probability of switching and the bottom one displays PC. Since this analysis is potentially revealing, I provide a detailed description of how the data going into this visualization was prepared [beneath](#description){: .animated} the figure. 

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='1'
    label='Group-level probability of switching as a function of performance <br>(left = F, right = S)' %}

[![switching_and_preformance]({{site.baseurl}}/img_compressed/switching_and_performance.svg)]({{site.baseurl}}/img/switching_and_performance.svg)

#### Notes
- the scale of and the position along the y-axis is different for each group / task split. 
- It seems that there is some correspondence between Pr(switch) and PC. Specifically, switching seems to be more likely when PC starts to plateau, which is a more prominent pattern for the F column. However, it might be the case that people just start switching after a certain period of time on a task (perhaps, due to boredom).

<a href='#description'></a>
#### Description

First, *outcome* (correct / incorrect) and *switch* (whether a new task was chosen for the next trial) data was split by group and task, resulting in two binary vectors for each split. These vectors were then sliced and stacked up in such a way that outcomes and switches of each subject occupied a separate row of its respective container array. Below is a simplified example of a single array containing the outcome data from 9 subjects (the switch array is processed identically, so that the corresponding rows represent the same individual). Note that the adjacent trials in a row do not necessarily correspond to adjacent trials during free play, because each row is a *concatenation* of all trials played on a given task by the subject.

<pre class='codeblock'>
[[0, 0, 1, 1, 1, 1, 0, 1, 0, 0, 1],
 [1, 0, 0, 1, 0],
 [1, 0, 0, 0, 0, 1],
 [1, 1, 1, 1, 0, 1, 0, 0, 0, 1, 1, 0, 0, 1],
 [1, 0, 1, 0, 1, 0, 0, 0, 0, 1, 0],
 [1, 1, 1, 0, 1, 0, 0, 1, 0, 1, 0, 1, 0, 0, 1, 1],
 [0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 0, 1, 0, 1],
 [0],
 [1, 1, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 1]]
</pre>

Since each row length is variable, only some of the data was selected and clipped to produce meaningful group-level statistics. The rows were first sorted by length. 

<pre class='codeblock'>
[[0],
 [1, 0, 0, 1, 0],
 [1, 0, 0, 0, 0, 1],
 [0, 0, 1, 1, 1, 1, 0, 1, 0, 0, 1],
 [1, 0, 1, 0, 1, 0, 0, 0, 0, 1, 0],  <------ Middle row (length = 11)
 [1, 1, 1, 1, 0, 1, 0, 0, 0, 1, 1, 0, 0, 1],
 [0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 0, 1, 0, 1],
 [1, 1, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 1],
 [1, 1, 1, 0, 1, 0, 0, 1, 0, 1, 0, 1, 0, 0, 1, 1]]
</pre>

Then, all rows shorter than the length of the middle row were thrown out, and the remaining rows were clipped by that length. What is left is a rectangular array that includes clipped data from at least half of the subjects.

<pre class='codeblock'>
[[0],
 [1, 0, 0, 1, 0],
 [1, 0, 0, 0, 0, 1],
 [0, 0, 1, 1, 1, 1, 0, 1, 0, 0, 1]
 ---------------------------------
               ^
 [1, 0, 1, 0, 1, 0, 0, 0, 0, 1, 0]   |,
 [1, 1, 1, 1, 0, 1, 0, 0, 0, 1, 1]   |, 0, 0, 1],
 [0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 0]  >|, 1, 0, 1],
 [1, 1, 1, 0, 0, 1, 0, 0, 1, 0, 0]   |, 0, 0, 0, 1],
 [1, 1, 1, 0, 1, 0, 0, 1, 0, 1, 0]   |, 1, 0, 0, 1, 1]]
</pre>

Each row of the outcome array was smoothed by a dynamic retrospective boxcar with a window size of 5. Concretely, each element in a row was replaced by the average across up to 4 preceding elements and itself. Each i-th element of the first 4 (starting from i = 0) was calculated as the average over the preceding i elements and itself. This corresponds to the assumption that all subjects considered the percentage of correct responses over up to 5 preceding trials (including the just played present trial), before deciding whether to switch on the next trial.

<pre class='codeblock'>
[1.  , 0.5 , 0.67, 0.5 , 0.6, 0.4, 0.4, 0.2, 0.2, 0.2, 0.2]
[1.  , 1.  , 1.  , 1.0 , 0.8, 0.8, 0.6, 0.4, 0.2, 0.4, 0.4]
[0.  , 0.5 , 0.33, 0.5 , 0.6, 0.6, 0.6, 0.8, 0.8, 0.6, 0.6]
[1.  , 1.  , 1.  , 0.75, 0.6, 0.6, 0.4, 0.2, 0.4, 0.4, 0.2]
[1.  , 1.  , 1.  , 0.75, 0.8, 0.6, 0.4, 0.4, 0.4, 0.4, 0.4]
</pre>

The mean vector across rows of this smoothed *outcome* array for each task is shown as a color-coded line in each task subplot. The mean vector across rows of the equivalently organized *switch* array is presented as a scatter plot. Finally, to prepare the last row of subplots, all arrays within a group were clipped by the "width" of the shortest array of their group and averaged across rows.

---

[Figure 2.2](#f-2-2){: .animated} shows the same relationship more directly by plotting the probability of switching against PC. 

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='2'
    label='Probability of switching plotted against PC <br>(left = F, right = S)' %}

[![switching_and_preformance_2]({{site.baseurl}}/img_compressed/switching_and_performance_2.svg)]({{site.baseurl}}/img/switching_and_performance_2.svg)

#### Notes
- There seems to be a positive relationship between the probability of switching and PC.
- However, the variance of Pr(switch) increases with higher levels of PC. In part, this seems to be an effect of sparsity of switches on any given trial. But it might also reflect the observation that higher levels of PC can either be rising or leveling off and Pr(switch) may change in relation to that, which these scatter plots cannot quite capture.