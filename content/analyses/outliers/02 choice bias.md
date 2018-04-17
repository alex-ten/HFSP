---
title: Choice Bias
category: outliers
entrynum: 2
---

<a id="{{ page.entrynum }}"></a>
## {{ page.entrynum }}. {{ page.title }}

Another way to find outliers is to see whether the subjects were biased towards one of the two possible responses across tasks. For each task within a subject, a single choice bias score is the proportion of the number of choices of the more frequently chosen item. That is, a choice bias score of .8 on any given task means that the subject chose one food item 80% of the time on that task. [Figure 2](#f-2) shows the sample distribution of *mean choice biases* across subjects, where mean choice bias per subject is the average of choice biases across the four tasks.

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    label='Mean choice biases across four tasks' %}
[![allocation_variance_raw](/img/average_choice_bias_across_tasks_raw.jpg)](/img/average_choice_bias_across_tasks_raw.jpg)

#### Notes
- Relative frequency hisogram of means of choice bias:
    - Vertical red line is the sample average of the mean choice bias scores across all subjects in all groups.
    - Shaded regions represent standard deviations.
    - Food choices were invariable within tasks for a given subject.
    - A single choice bias score per task (within a subject) is calculated as  the proportion of choices of the  more frequently chosen food item. Since there are only two alternatives per task, the range for the score is [.5, 1.0].
    
Different cutoff values and the corresponding outliers are listed in [Table 2](#t-2). The criterion of > 3 s.d. selects most of the subjects that form the small “islands” about the large bulk of data.

{% include caption.html 
    obj='table'
    num=page.entrynum 
    label='Extreme sticker counts split by group and condition' %}
    
| Upper-bound cutoff | Outliers |
|:------------------:|:--------:|
|         .7         |    19    |
|         .8         |     2    |
|         .9         |     1    |
|       2 s.d.       |    18    |
|       3 s.d.       |     7    |
|       4 s.d.       |     2    |
|====================|==========|
|                    |          |
{: .apa : align='center' : id='t-1-1'}
