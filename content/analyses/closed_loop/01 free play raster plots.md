---
title: Free play raster plots
category: closed_loop
doctype: entry
entrynum: 1
---

Perhaps, visualizations in this section are not readily interpretable, but being the most literal representation of the raw, free play data available, they might inspire some ideas. Below, [Figure 1.1](#f-1-1){:.animated} shows free play raster plots, one for each group / condition split. Each row is a separate subject in that group. The x-axis represents consequtive trials of free play, vertical marks represent *errors* and black diamonds represent switch trials (i.e. trials after which a subject switched to a different task). 

Additionally, subjects in each group / condition split were sorted by the number of switches and appear in that order on the plots (ascending order from top to bottom). Also, you can use the button at the bottom-right corner of the figure to view the same plots with an alternative coloring scheme, such that each task has a more a distinct color, but I find those too chaotic to look at.

{% include caption.html 
    obj='figure'
    ext='1'
    num=page.entrynum 
    label='Raster plots depicting free play trials' %}

<div class='full-width'>
    <table class='rastergrid'>
        <tr>
            <td><a href='{{site.baseurl}}/img/raster_plots_2colors-0-0.svg'><img alt='raster_plot_free_uninformed' src='{{site.baseurl}}/img_compressed/raster_plots_2colors-0-0.svg'/></a></td>
            <td><a href='{{site.baseurl}}/img/raster_plots_2colors-0-1.svg'><img alt='raster_plot_free_informed' src='{{site.baseurl}}/img_compressed/raster_plots_2colors-0-1.svg'/></a></td>
        </tr>
        <tr>
            <td><a href='{{site.baseurl}}/img/raster_plots_2colors-1-0.svg'><img alt='raster_plot_strategic_uninformed' src='{{site.baseurl}}/img_compressed/raster_plots_2colors-1-0.svg'/></a></td>
            <td><a href='{{site.baseurl}}/img/raster_plots_2colors-1-1.svg'><img alt='raster_plot_strategic_informed' src='{{site.baseurl}}/img_compressed/raster_plots_2colors-1-1.svg'/></a></td>
        </tr>
        <tr>
            <td colspan="2" align='center'>
                <a class='switch'>colors 🎨</a>
            </td>
        </tr>
    </table>
</div>

#### Notes:
- Unsurprisingly, trial sequences of 2D and R tasks seem to be more dense (with errors) than sequences of 1D and I1D.
- Some participants (especially in the F/i+ group) tend to stick to one of the easy tasks (particularly, 1D) despite committing very few errors
- S groups in each condition appear relatively denser and bluer. Somewhat counter-intuitively,  S/i+ subjects seem to have persisted with the R task despite making many errors. I would expect informed, strategically exploring participants to abandon the R task as soon as they identify it as unsolvable, which should be suggested by the chance-level amount of errors. Reflecting on that, I don't think sticking necessarily means less exploration in this context. One can explore the depth of one family instead of the range of different families. And in fact, that would be in line with the instruction to "" when the learnable tasks are learned.
- Even after [filtering by oversticking]({{site.baseurl}}/content/analyses/outliers/index.html#1){:.animated}, a few subjects (like at the top of F/i+ and S/i- plots) still look like outliers.

To verify that impression that the S group spent more time on more difficult tasks we plot the box-and-whiskers distributions of the total number of trials spent on each task by subjects in each of the groups (see [Figure 1.2](#f-1-2){:.animated})

{% include caption.html 
    obj='figure'
    ext='2'
    num=page.entrynum 
    label='Time spent on each task' %}
[![Time spent on each task]({{site.baseurl}}/img_compressed/time_spent_boxplots.svg)]({{site.baseurl}}/img/time_spent_boxplots.svg)

#### Notes:
- Whiskers correspond to minimum and maximum values.
- More clearly we can see that the explicit instruction to maximize learning is associated with sticking to unsolvable task, mostly at the expense of spending time on the easiest task.