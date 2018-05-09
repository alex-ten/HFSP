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

#### Discussion
I don't see an obvious connection between playing the R task (often and badly) and better average performance on test trials. What seems plausible is that, due to the fact that the plots show errors, it *seems* like better learners prefer the R task, whereas in fact they simply learn the easier tasks efficiently and don't commit as many errors as poor learners do. In that case, the raster plots show a very obvious thing: that good learners commit less errors on learnable tasks than bad learners.

These raster plots provide a hint on characterizing exploration strategies of different individuals. We can look at performance *around* the switch trials for each participant. A good learning strategy would be to learn a task and switch to the yet unlearned task. This means that on average, the performance right before each switch should be better than performance right after each switch. This might be a behavioral characteristic of efficient and poor learners, or learning-oriented and performance-oriented subjects.

### 1.3. Is learning outcome related to task selection patterns?
[Figure 1.3](#f-1-3){:.animated} shows dPC as a function of the percentage of the total number of trials spent on each task for each group and [Table 1.3](#t-1-3){:.animated} lists summaries of the models associated with each task / group split.

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='3'
    label='dPC and task selection' %}
[![alt]({{site.baseurl}}/img_compressed/correlates_of_dpc.svg)]({{site.baseurl}}/img/correlates_of_dpc.svg)

{% include caption.html 
    obj='table' 
    num=page.entrynum
    ext='3'
    label='Models of average dPC as a function of task selection' %}
<table class="apa">
    <thead>
        <tr>
            <th></th>
            <th></th>
            <th colspan="4">F</th>
            <th colspan="4">S</th>
        </tr>
    </thead>
    <thead>
        <tr>
            <td></td>
            <td></td>
            <td><bold>1D</bold></td>
            <td><bold>I1D</bold></td>
            <td><bold>2D</bold></td>
            <td><bold>R</bold></td>
            <td><bold>1D</bold></td>
            <td><bold>I1D</bold></td>
            <td><bold>2D</bold></td>
            <td><bold>R</bold></td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span style="font-style:italic">R<sup>2</sup></span></td>
            <td></td>
            <td>.032</td>
            <td>.003</td>
            <td>.046</td>
            <td>.008</td>
            <td>.047</td>
            <td>.002</td>
            <td>.001</td>
            <td>.026</td>
        </tr>
        <tr>
            <td><span style="font-style:italic">adj. R<sup>2</sup></span></td>
            <td></td>
            <td>.026</td>
            <td>-.004</td>
            <td>.039</td>
            <td>.002</td>
            <td>.042</td>
            <td>-.004</td>
            <td>-.004</td>
            <td>.021</td>
        </tr>
        <tr>
            <td><span style="font-style:italic">F</span></td>
            <td></td>
            <td>5.013</td>
            <td>0.0455</td>
            <td>7.286</td>
            <td>1.267</td>
            <td>8.585</td>
            <td>0.352</td>
            <td>0.252</td>
            <td>4.722</td>
        </tr>
        <tr>
            <td><span style="font-style:italic">p</span></td>
            <td></td>
            <td>.027</td>
            <td>.501</td>
            <td>.008</td>
            <td>.262</td>
            <td>.004</td>
            <td>.554</td>
            <td>.616</td>
            <td>.031</td>
        </tr>
        <tr>
            <td><span style="font-style:italic">b<sub>0</sub></span></td>
            <td></td>
            <td>0.118</td>
            <td>0.092</td>
            <td>0.026</td>
            <td>0.060</td>
            <td>0.126</td>
            <td>0.095</td>
            <td>0.073</td>
            <td>0.031</td>
        </tr>
        <tr>
            <td></td>
            <td><span style="font-style:italic">t</span></td>
            <td>5.347</td>
            <td>4.035</td>
            <td>1.086</td>
            <td>2.618</td>
            <td>6.313</td>
            <td>4.151</td>
            <td>2.610</td>
            <td>1.077</td>
        </tr>
        <tr>
            <td></td>
            <td><span style="font-style:italic">CI</span></td>
            <td>[0.074, 0.0161]</td>
            <td>[0.047, 0.0136]</td>
            <td>[-0.021, 0.074]</td>
            <td>[0.015, 0.105]</td>
            <td>[0.087, 0.166]</td>
            <td>[0.050, 0.141]</td>
            <td>[0.018, 0.128]</td>
            <td>[-0.026, 0.087]</td>
        </tr>
        <tr>
            <td></td>
            <td><span style="font-style:italic">p</span></td>
            <td>.000</td>
            <td>.000</td>
            <td>.279</td>
            <td>.01</td>
            <td>.000</td>
            <td>.000</td>
            <td>.010</td>
            <td>0.283</td>
        </tr>
        <tr><td></td></tr>
        <tr>
            <td><span style="font-style:italic">b<sub>1</sub></span></td>
            <td></td>
            <td>-0.312</td>
            <td>-0.051</td>
            <td>0.234</td>
            <td>0.08</td>
            <td>-0.257</td>
            <td>-0.054</td>
            <td>0.047</td>
            <td>0.0139</td>
        </tr>
        <tr>
            <td></td>
            <td><span style="font-style:italic">t</span></td>
            <td>-2.239</td>
            <td>-0.674</td>
            <td>2.699</td>
            <td>1.126</td>
            <td>-2.930</td>
            <td>-0.593</td>
            <td>0.502</td>
            <td>2.173</td>
        </tr>
        <tr>
            <td></td>
            <td><span style="font-style:italic">CI</span></td>
            <td>[-2.249, -0.016]</td>
            <td>[-0.202, 0.099]</td>
            <td>[0.063, 0.405]</td>
            <td>[-0.060, 0.220]</td>
            <td>[-0.429, -0.084]</td>
            <td>[-0.232, 0.125]</td>
            <td>[-0.139, 0.234]</td>
            <td>[0.013, 0.265]</td>
        </tr>
        <tr>
            <td></td>
            <td><span style="font-style:italic">p</span></td>
            <td>.027</td>
            <td>.501</td>
            <td>.008</td>
            <td>.262</td>
            <td>.004</td>
            <td>.554</td>
            <td>.616</td>
            <td>0.031</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>>
            <td colspan='10'></td>
        </tr>
    </tfoot>
</table>

#### Notes
- Some of the models are significant, but neither one accounts for a lot of variance in dPC. Considering the fitted lines together with the scatter-plotted data, it doesn't seem worthy to try and interpret the specific models (they all seem equally bad).
- However, some general trends are interesting:
    - In both groups, there is a reversal of the slope from negative to positive as a function of task difficulty. So, subjects who played less of task 1D (or more of task R) had a slightly higher dPC.
    - Tasks 1D and R seem to be related: proportion of time spent on each task is similarly distributed in the F group, but changes for 1D and R tasks in the S group.