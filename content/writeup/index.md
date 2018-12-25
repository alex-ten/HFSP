---
layout: default

---

{% include toc.html %}

<h2> 1. Overall task prevalence across groups and conditions shows conditional preference for R </h2>
The figure shows the proportions of trials on each of the four tasks in various partitions of the data.

<div class='caption' id='f-1'>
    <em>
        <b>Figure 1. Proportions of time spent on each task across different groups and conditions</b>
    </em>
</div>
<a href='{{site.baseurl}}/img/time_on_tasks.svg'><img alt='time_on_tasks' src='{{site.baseurl}}/img_compressed/time_on_tasks.svg' style="width: 40%; height:auto; display: block; margin: 0 auto;/"></a>
<hr>

<h2> 2. Task prevalence across time shows consistency in conditional preference for R </h2>
All figures below show more or less the same information -- task prevalence through time. Line plots show the proportions of people on each of the four tasks (I think splitting the groups by condition looks to chaotic if put in the same subplot, see Figure 1.2).

<div class='caption' id='f-2-1'>
    <em>
        <b>Figure 2.1. Line plots of task prevalence split by group</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/pselect_G_lines.svg'>
    <img src='{{site.baseurl}}/fimg/pselect_G_lines.svg' alt='task_prevalence_lines_G' style="width: 80%; height:auto; display: block; margin: 0 auto;/">
</a>
<hr>

<div class='caption' id='f-2-2'>
    <em>
        <b>Figure 2.2. Line plots of task prevalence split by group and condition</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/pselect_GC_lines.svg'>
    <img src='{{site.baseurl}}/fimg/pselect_GC_lines.svg' alt='task_prevalence_lines_GC' style="width: 80%; height:auto; display: block; margin: 0 auto;/">
</a>
<h4> Notes </h4>
Dashed lines represent the uninformed condition.
<hr>

<h2> 3. Individual-level selection rates show idiosyncratic preference for R across groups </h2>
Histograms below show the distribution of individuals in each group that played some X amount of time on a task, relative to total time spent on all tasks.

<div class='caption' id='f-3-1'>
    <em>
        <b>Figure 3.1. Line histograms of participants' trial allocation</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/selection_rates.svg'>
    <img src='{{site.baseurl}}/fimg/selection_rates.svg' alt='ind_selection_rates' style="width: 80%; height:auto; display: block; margin: 0 auto;/">
</a>
<hr>

<h2> 4. Judgments of learning potential appear related to objectively measured performance during familiarization </h2>

In this, as well as the next section, a Spearman's rank correlation coefficient was calculated for each participant to provide a measure of the relationship between their judgment of learning potential and their objective performance (or, in section 5, their positive change in objective performance). First, each participant's raw PC and LRN scores were converted to ranks. Ranks of the tied values were determined randomly. This tie-breaking approach may product false non-zero coefficients where there should be no correlation. Therefore, all cases with all-equal LRN or PC scores were assigned 0 correlation coefficients prior to the ranking procedure.

Each individual coefficient is highly unreliable, since only 4 observations (one for each task) are available per participant. However, noting that the correlation coefficient $$r$$ is a sample statistic, we can find an appropriate sampling distribution to evaluate our data against. For example, we can assume that each individual coefficient comes from sampling two independent (uncorrelated) variables, PC and LRN. If they are indeed independent, the sampling distribution of $$r$$ should be approximately normally distributed around 0. We can compare our sufficiently large groups to this abstract sampling distribution by applying an appropriate transformation, known as the [Fisher's z](http://onlinestatbook.com/2/sampling_distributions/samp_dist_r.html){:.animated}:

$$ z_F = \frac{1}{2} \log (\frac{1+r}{1-r}) $$

Variable $$z_F$$ is normally distributed with a standard error determined by sample size $$N$$:

$$ \sigma = \frac{1}{\sqrt{N - 3}} $$

Thus, assuming no correlation, we can calculate the probability of observing our data in samples of correlation coefficients:

<pre class='codeblock'>
    F / i+: r = -0.35, z = -3.07, p =  0.00
    F / i-: r = -0.35, z = -3.01, p =  0.00
    S / i+: r = -0.32, z = -2.97, p =  0.00
    S / i-: r = -0.30, z = -2.72, p =  0.00
</pre>

<div class='caption' id='f-4-1'>
    <em>
        <b>Figure 4.1. Distributions of individual-level Spearman's rank correlation coefficients between LRN and PC across groups and conditions (separate bar histograms)</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/corr_pc_lrn_bars.svg'>
    <img src='{{site.baseurl}}/fimg/corr_pc_lrn_bars.svg' alt='lrn_and_pc1' style="width: 70%; height:auto; display: block; margin: 0 auto;/">
</a>
<hr>

<div class='caption' id='f-4-2'>
    <em>
        <b>Figure 4.2. Distributions of individual-level Spearman's rank correlation coefficients between LRN and PC across groups and conditions (overlaid line histograms)</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/corr_pc_lrn_lines.svg'>
    <img src='{{site.baseurl}}/fimg/corr_pc_lrn_lines.svg' alt='lrn_and_pc2' style="width: 50%; height:auto; display: block; margin: 0 auto;/">
</a>
<hr>

The plots hint at a potential effect of group on correlation between LRN and PC. To test this, a 2-way ANOVA was conducted. The analysis found no significant main effects of neither group nor condition. It appears that the relationship between PC and LRN was homogeneous across groups. It is interesting nonetheless that there are 2 distinct clusters of people: those whose LRN ratings were correlation with their objective performance (the majority), and those whose ratings and performance were completely unrelated.


<h2> 5. Judgments of learning potential appear unrelated to change in objectively measured performance during familiarization </h2>

Change in performance is measured as the difference between hit rates during the last and the first five trials of training. Negative difference scores were assigned 0 values, corresponding to no positive change (no progress in performance). Using the same logic for testing the correlations as presented in section 4, the relationship between LRN and change in performance is not so obvious. Only in the free and uninformed group dPC reliably predicted LRN:

<pre class='codeblock'>
    F / i+: r = -0.10, z = -0.86, p =  0.19
    F / i-: r = -0.20, z = -1.70, p =  0.04
    S / i+: r = -0.10, z = -0.92, p =  0.18
    S / i-: r = -0.02, z = -0.21, p =  0.42
</pre>

<div class='caption' id='f-5-1'>
    <em>
        <b>Figure 5.1. Distributions of individual-level Spearman's rank correlation coefficients between LRN and dPC across groups and conditions (separate bar histograms)</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/corr_dpc_lrn_bars.svg'>
    <img src='{{site.baseurl}}/fimg/corr_dpc_lrn_bars.svg' alt='lrn_and_dpc1' style="width: 70%; height:auto; display: block; margin: 0 auto;/">
</a>
<hr>

<div class='caption' id='f-5-1'>
    <em>
        <b>Figure 5.2. Distributions of individual-level Spearman's rank correlation coefficients between LRN and dPC across groups and conditions (composite line line histogram)</b>
    </em>
</div>
<a href='{{site.baseurl}}/fimg/corr_dpc_lrn_lines.svg'>
    <img src='{{site.baseurl}}/fimg/corr_dpc_lrn_lines.svg' alt='lrn_and_dpc2' style="width: 50%; height:auto; display: block; margin: 0 auto;/">
</a>

Another 2-way ANOVA was conducted to spot any reliable differences in the relationship between performance improvement and learning potential. Again, there were no significant main effects and no interactions.