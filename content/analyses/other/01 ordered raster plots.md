---
title: Ordered raster plots
category: other
doctype: entry
entrynum: 1
---

### 1.1. Ordering by delta PC
[Figure 1.1](#f-1-1){:.animated} shows free play raster plots in which the subjects were ordered by their learning outcome (dPC) defined as the difference between average test PC and average training PC; both PC scores were calculated as the percentage of correct responses over the last 5 trials of the corresponding stage. The test stage for both groups was simply the last 5 trails of free play. While training PC was always calculated across 3 learnable tasks, the test PC was the average over the last 5 free play trials that the subject had actually played, and if she did not play at least 5 trials of one of the tasks, her PC test would be the average over the remaining 2 tasks.

{% include caption.html 
    obj='figure'
    ext='1'
    num=page.entrynum 
    label='Raster plots depicting free play trials (ordered by dPC)' %}
<div class='full-width'>
    <table class='rastergrid'>
        <tr>
            <td><a href='{{site.baseurl}}/img/dpc_raster_plots_2colors-0-0.svg'><img alt='dpc_raster_plot_free_uninformed' src='{{site.baseurl}}/img_compressed/dpc_raster_plots_2colors-0-0.svg'/></a></td>
            <td><a href='{{site.baseurl}}/img/dpc_raster_plots_2colors-0-1.svg'><img alt='dpc_raster_plot_free_informed' src='{{site.baseurl}}/img_compressed/dpc_raster_plots_2colors-0-1.svg'/></a></td>
        </tr>
        <tr>
            <td><a href='{{site.baseurl}}/img/dpc_raster_plots_2colors-1-0.svg'><img alt='dpc_raster_plot_strategic_uninformed' src='{{site.baseurl}}/img_compressed/dpc_raster_plots_2colors-1-0.svg'/></a></td>
            <td><a href='{{site.baseurl}}/img/dpc_raster_plots_2colors-1-1.svg'><img alt='dpc_raster_plot_strategic_informed' src='{{site.baseurl}}/img_compressed/dpc_raster_plots_2colors-1-1.svg'/></a></td>
        </tr>
        <tr>
            <td colspan="2" align='center'>
                <a class='switch'>colors 🎨</a>
            </td>
        </tr>
    </table>
</div>

#### Notes
- The *vertical* colorbar represents the ordering of participants by dPC and the mapping of colors to values of dPC can be seen in the horizontal colorbar below the figures.
- Only the average dPC across *learnable* tasks was used for ordering.
- In the S groups, there might be a correlation between dPC and the number trials played on the R task. It seems like the upper right corners of S/i- and S/i+ are denser with errors from the random task. So group S subjects with higher dPC (might have) played the random task more than others at a later stage of the experiment. Perhaps, those are the ones who indeed tried to maximize their learning by quickly figuring out the learnable tasks, after which they reasonably stuck with the unlearned and unlearnable R task.

### 1.2. Ordering by test PC
[Figure 1.2](#f-1-2){:.animated} shows the familiar raster plots where the subjects are ordered by test PC. 

{% include caption.html 
    obj='figure'
    ext='1'
    num=page.entrynum 
    label='Raster plots depicting free play trials (ordered by test PC)' %}
<div class='full-width'>
    <table class='rastergrid'>
        <tr>
            <td><a href='{{site.baseurl}}/img/pc_raster_plots_2colors-0-0.svg'><img alt='pc_raster_plot_free_uninformed' src='{{site.baseurl}}/img_compressed/pc_raster_plots_2colors-0-0.svg'/></a></td>
            <td><a href='{{site.baseurl}}/img/pc_raster_plots_2colors-0-1.svg'><img alt='pc_raster_plot_free_informed' src='{{site.baseurl}}/img_compressed/pc_raster_plots_2colors-0-1.svg'/></a></td>
        </tr>
        <tr>
            <td><a href='{{site.baseurl}}/img/pc_raster_plots_2colors-1-0.svg'><img alt='pc_raster_plot_strategic_uninformed' src='{{site.baseurl}}/img_compressed/pc_raster_plots_2colors-1-0.svg'/></a></td>
            <td><a href='{{site.baseurl}}/img/pc_raster_plots_2colors-1-1.svg'><img alt='pc_raster_plot_strategic_informed' src='{{site.baseurl}}/img_compressed/pc_raster_plots_2colors-1-1.svg'/></a></td>
        </tr>
        <tr>
            <td colspan="2" align='center'>
                <a class='switch'>colors 🎨</a>
            </td>
        </tr>
    </table>
</div>

#### Notes
- Similarly to above, there seems to be a positive correlation between the number of trials played on the R task and PC. There seems to be a lot more red (thus, errors on 1D and I1D) at the lower portions of the F groups' graphs. This trend seems present, albeit less strikingly, in the F groups (and relatively more so in the S/i+).

### 1.3. Discussion
I don't see an obvious connection between playing the R task (often and badly) and better average performance on test trials. What seems plausible is that, due to the fact that the plots show errors, it *seems* like better learners prefer the R task, whereas in fact they simply learn the easier tasks efficiently and don't commit as many errors as poor learners do. In that case, the raster plots show a very obvious thing: that good learners commit less errors on learnable tasks than bad learners.

These raster plots provide a hint on characterizing exploration strategies of different individuals. We can look at performance *around* the switch trials for each participant. A good learning strategy would be to learn a task and switch to the yet unlearned task. This means that on average, the performance right before each switch should be better than performance right after each switch. This might be a behavioral characteristic of efficient and poor learners, or learning-oriented and performance-oriented subjects.

