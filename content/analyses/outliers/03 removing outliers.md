---
title: Removing outliers
category: outliers
doctype: entry
entrynum: 3
---

Removing extreme stickers (no switches during free exploration), overstickers (with allocation variance score > 100) and choice-biased participants (choice bias > 2 s.d.) leaves out 70 outliers (48 by extreme sticking criterion, 55 by allocation variance, and 18 by side-bias).

That leaves us with 330 subjects: 75, 79, 84, and 92 in groups F/i-, F/i+, S/i- and S/i+, respectively.

{% include caption.html 
    obj='figure' 
    num=page.entrynum  
    label='Filtered data' %}
<table class='imagegrid'>
    <tr>
        <td>(a) Task allocation variance</td>
        <td>(b) Mean choice biases across four tasks</td>
    </tr>
    <tr>
        <td><a href="{{site.baseurl}}/img/task_allocation_variance_clean.svg"><img src="{{site.baseurl}}/img_compressed/task_allocation_variance_clean.svg" alt="allocation_variance_clean" /></a></td>
        <td><a href="{{site.baseurl}}/img/average_choice_bias_across_tasks_clean.svg"><img src="{{site.baseurl}}/img_compressed/average_choice_bias_across_tasks_clean.svg" alt="choice_bias_clean" /></a></td>
    </tr>
</table>