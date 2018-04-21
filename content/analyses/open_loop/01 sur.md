---
title: Seemingly unrelated regressions
category: open_loop
doctype: entry
entrynum: 1
---

This is the expected result based on the initial analysis:
The colors are the task (1D, I1D, etc). Groups 1 and 2 are free play, 3 and 4 are strategic
- Betas for PC are positive for groups 1 and 2 and negative for groups 3 and 4
- Betas for LRN are the other way around
- Betas for Change in PC are 0 (or perhaps slightly negative)
It is possible that the regression will crash is PC and LRN are too strongly correlated. In this case we will drop one of them.
This will allow us to say which ones of the trends we see are significant.

{% 
    include caption.html 
    obj='figure' 
    num=page.entrynum 
    label='Plot of SUR coefficients' 
%}
[![training_learning_performance]({{site.baseurl}}/img_compressed/sur.png)]({{site.baseurl}}/img/sur.png)