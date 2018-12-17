## Template .md for analysis entry

---
title:
category:
doctype:
entrynum:
---

## Template for figure

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    label='caption content' %}
[![alt]({{site.baseurl}}/img_compressed/file.name)]({{site.baseurl}}/img/file.name)

### 1.3. What might the learning outcome be related to?
[Figure 1.3](#f-1-3){:.animated} shows dPC as a function of the percentage of the total number of trials spent on each task for each group and [Table 1.3](#t-1-3){:.animated} lists the summaries of models associated with each task / group split.

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
    
#### dPC and free play PC

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='4'
    label='dPC and task selection' %}
[![alt]({{site.baseurl}}/img_compressed/dpc_pc_by_task.svg)]({{site.baseurl}}/img/dpc_pc_by_task.svg)


<p>
    We could render the LaTeX document here with a link to the actual document and collaboration platform.
</p>

Here's an example of MathJax Jekyll integration:

<pre class='codeblock'>
{§ raw §}
  $$a^2 + b^2 = c^2$$
{§ endraw §}
</pre>

which is rendered like this:

{% raw %}
  $$a^2 + b^2 = c^2$$
{% endraw %}

<!--
# Baseline challenge predictions
accuracy = 0.327315914489311
{% endraw %}
</pre>
-->


#### Base rate
We should be able to safely assume that the expected prior probability of food preferences is uniform (i.e. $$p(h)=0.5$$). This should especially apply in the beginning of the experiment if no a priori expectations about the relative frequency of encountering monsters with a certain food preference are held. Whether and how the prior is updated as a function of experience has an effect on how subsequent uncertainty is computed. We could additionally assume that the empirical base rate information is neglected throughout the experiment (i.e. remains uninformative, at 0.5) regardless of the actual evidence. Perhaps participants do not pay attention to the base rate at all. In some of the tasks (I1D, and R) the true base rate was in fact 0.5, but note that in 1D and 2D task, the true prior under uniform sampling of individual monsters was not flat, due to uneven split of the feature space (2:4 and 16:20, respectively, see the [description of problem space]({{site.baseurl}}/content/writeup/index.html#1.1._The_problem_space){:.animated}). Another possibility is to start with a prior of 0.5, but then update the actual frequencies of observed food preferences. Furthermore, there are several possibilities of how these observations may be stored. For example, positive or negative feedback may have an effect on how the base rates are updated.

#### Evidence
When prediction is the goal, it is common to ignore the evidence term in the denominator, since it is constant across different hypotheses. Thus, in any given situation when multiple hypotheses (categories, answers) are considered, the one that has the highest relative score is the most likely to be correct. For that reason, the posterior is often written as being proportional to the numerator of the Bayes rule:

$$ p(h \vert \textbf{d}) \propto {p(h)p(\textbf{d} \vert h)} $$

All that is needed here in order to come up with relatively more or less probable answers is the base rate $$p(h)$$ and likelihood $$ p(\textbf{d} \vert h) $$. However, we are not merely interested in the *argmax* of the product of prior and likelihood, because we want to know the conditional entropy of a monster family which requires the absolute posterior probability

#### Likelihood
Suppose the perceptual system is able to derive a set of distinct features (e.g. eyes, star, tentacles, etc.) from raw visual input and represent them as abstract variables (e.g. having some size, relative position, etc.). Then the $$N$$-dimensional space $$\mathcal{D}$$ can represent the latent feature space of either discretely or continuously varying dimension variables. Assuming [conditional independence](https://en.wikipedia.org/wiki/Conditional_independence){:.animated} of features given a food preference, the likelihood that a particular monster has a particular food preference is the product of probabilities (possibly estimated from the observed frequencies) positive examples:

$$p(\textbf{d} \equiv (d_1, d_2, ... , d_m) \vert h) = \prod_{i=1}^{m}p(d_i \vert h)$$

Incorporating this simplification are known as the *naive* Bayes approach, since it assumes that features appear independently regardless of the underlying category ({% include citation.html link='pdfs/Lewis1998.pdf' cite='Lewis, 1998'%}). There are a couple of issues with this. First, the 2D task was constructed in such a way that the features would not be conditionally independent. That is, while dimension $$d_i$$ does not predict dimension $$d_j$$ unconditionally, if given the knowledge of food preference, the two dimensions become mutually constrained. Second, naive Bayes 


---

Assuming random and independent sampling of monster features from that space, and (2) conditional independence of features on food preferences (see below), the likelihood of hypothesis $$h$$ can be calculated heuristically as a function of its size ({% include citation.html link='pdfs/Tenenbaum1999.pdf' cite='Tenenbaum, 1999'%}):

$$p(\textbf{d} \equiv (d_1, d_2, ... , d_m) \vert h) =  = \frac{1}{|h|^N}$$

Uncertainty depends on the size of the hypothesis space, which depends not only on the size of the rectangles in known dimensions, but their dimensionality as well. All else being equal, a higher-dimensional cube is always larger than its lower-dimensional projection. So initially, when the there are more potential dimensions that might influence food choices, uncertainty is very high. but Assuming the participants assume a uniform distribution of these features 

---

Suppose the participant observes $$n$$ positive examples $$D_A = \{ \textbf{d}^{(1)}, \textbf{d}^{(2)}, ..., \textbf{d}^{(n)}\}$$ of monsters that prefer food A.

The assumption of conditional independence has implications for the computation of likelihoods for monster families with multidimensional variability. It is met in I1D, as we can reason that knowing the conditional event (food preference $$h$$) adds no information about the occurrence of some feature $$d_i$$ if we know that $$d_j$$ occurred (knowing whether a short bear is also tall is not clarified by knowing its food preference):

$$ p(d_i, d_j \vert h) = p(d_i \vert h)p(d_j \vert h)$$

The same assumption is not met in the 2D case, since knowing the food preference allows us to gain additional information about $$d_i$$ given $$d_j$$ (knowing whether a short bear is also tall can be  clarified by knowing its food preference):

$$ p(d_i, d_j \vert h) \neq p(d_i \vert h)p(d_j \vert h)$$



<!--
A more concrete example might be helpful. Suppose a subject say two monsters with somewhat large eyes ($$x_1=4$$ and $$$x_2=5$$) and both of them preferred food A. Then, the probability that a new monster with large eyes (say, $$y=6$$) will also be high:

$$ p(y prefers A \vert {x_1=4, x_2=5}) = \sum_{r \in \mathcal{D}}p(y \in C \vert r)p(r \vert X)$$


After seeing just one positive (or negative) example of food-A-loving monster, what possible other monsters might a participant think would prefer (or dislike) the same food? Presumably, the ones that are similar to that single example (as per instructions). But with very little experience, it is impossible to know what to base the similarity on (is it eye size, the number of eyes, their position, or something else entirely?). Reliable induction requires a sample of several examples.

Now suppose a few other examples have been seen observed. This similarly sparse experience is often enough to support induction in humans. In our monster task, it might be sufficient to observe a handful of monsters to establish the relevant dimensions of variability over which the classification rule might be defined.-->



----


<h2>1. Task description</h2>
<p>
    The active sampling task was designed to explore how adult human subjects organize their exploratory behavior in a relatively unconstrained setting. In this setting, the subjects were first familiarized with four classes (families) of stimuli (monsters) by guessing the subcategory (food preference) of each individual stimulus from each class and receiving immediate feedback on their responses. Specifically, each subject went through 4 blocks of 15 familiarization trials (one block per family) trying to figure out what food each individual monster preferred. </p>
<p>
    After familiarization, participants rated each family on the scale of Learnability (LRN) and proceeded to the next stage of free exploration. During free exploration, the subjects were required to perform at least 250 trials of the same food-guessing task. However, now they could willfully change which monster family to play on the next trial.</p>

<h3>1.1. The problem space</h3>
<p>
    There were 2 unique food items per family. Individual monsters varied both within and across families. Monsters from different families varied grossly in their overall appearance (e.g. pink bunnies, orange squids, blue bears), while monsters from the same family differed more subtly, in up to 2 features of variation unique to their family (e.g. a bunny with long ears and big belly star and a bunny with shorter ears and small belly star).</p>
<p>
    In addition to the obvious variability in appearance between monster families, there was a subtler variability in the complexity of food preference classification. For example, in one condition, the monsters varied along a single dimension (e.g. height) which reliably predicted food preference (1D condition). In other conditions, monsters varied along 2 dimensions. In condition I1D (ignore 1 dimension), only one dimension was diagnostic of food preference, while the other was not, i.e. it corresponded with food preference 50% of time on average. In condition 2D, it was a certain <i>combination</i> of those dimensions that predicted food preferences. Finally, there was a random (R) condition in which each individual monster was randomly assigned a food preference on each trial. By design, learning to reliably predict food preferences of monsters by looking at their appearance was impossible in that condition.</p>
<p>
    The precise category structure of each of the learnable conditions is illustrated below. The features varied discretely over 6 possible values. For a given subject, the conditions were constant across monster families (e.g. blue bears were always 1D, while pink bunnies were always I1D). However, the mapping of conditions onto monster families differed between participants.</p>

<pre class='codeblock'>
Condition 1D:
                          A  A  B  B  B  B
                          ----------------
                          1  2  3  4  5  6
                                 D1
Condition I1D:
                       6| A  A  A  B  B  B
                       5| A  A  A  B  B  B
                       4| A  A  A  B  B  B
                    D2 3| A  A  A  B  B  B
                       2| A  A  A  B  B  B
                       1| A  A  A  B  B  B
                         -----------------
                          1  2  3  4  5  6
                                 D1
Condition 2D:
                       6| B  B  B  B  B  B
                       5| B  B  B  B  B  B
                       4| A  A  A  A  B  B
                    D2 3| A  A  A  A  B  B
                       2| A  A  A  A  B  B
                       1| A  A  A  A  B  B
                         -----------------
                          1  2  3  4  5  6
                                 D1
</pre>


<h2>2. Findings</h2>
<h3>2.1. Sanity checks</h3>
<p>
    Before anything else, we wanted to verify that our manipulation of task difficulty worked as intended. To do that, we looked at a simple performance metric, the percentage of correct responses (<b>percent correct or PC</b>), at different points of time. <a href='#f-2-1' class='animated'>Figure 2.1</a> shows that the difficulty manipulation was meaningful in the sense that participants performed best on 1D, slightly worse on I1D, and worse still on 2D on training (leftmost column of plots).</p>

<div class='caption' id='f-2-1'>
    <em>
        <b>Figure 2.1.</b> PC across subjects for each task split by group and conditions (N bins = 16)
    </em>
</div>
<a href='{{site.baseurl}}/img/train_test_delta_hists_15_15_.svg'>
    <img src='{{site.baseurl}}/img_compressed/train_test_delta_hists_15_15_.svg' alt='train_test_delta_hists_15_15'>
</a>

<p>
    We also defined a test stage (here the last 15 trials of free play <a id='backto1' href='#fn1' class='animated'>[1]</a>) over which PC was measured (plots in the middle column). The difference between a participant's test-stage PC and training-stage PC provided an objective measure of performance improvement, delta PC (dPC). From <a href='#f-2-1' class='animated'>Figure 2.1</a> we can see that most people had positive dPC scores on 1D, meaning that the vast majority of people managed to improve on this task. As expected, more people improved less or even performed worse on I1D, as seen from a shallower and more laterally spread distribution of dPC on that task. This tendency was more prominent for 2D, with now a considerable portion of people falling below or close to 0.</p>

<p>
    There seems to be no differences in dPC between the two instructions groups (freely exploring vs. strategic, or F vs. S). This is rather interesting, given, as we show further, that different exploration strategies employed by the S and F groups.</p>


<h3>2.2. Task selection during free play </h3>
<p>
    One interesting finding was that despite the lack of differences in dPC between groups, their behavior during free play was quite distinct. For example, average PC per trial of free play increased steadily over this period for the F but not the S group (<a href='#f-2-2-1' class='animated'>Figure 2.2.1</a>)</p>

<div class='caption' id='f-2-2-1'>
    <em>
        <b>Figure 2.2.1.</b> Average PC per trial during free play
    </em>
</div>
<a href='{{site.baseurl}}/img/smoothed_pc.svg'>
    <img src='{{site.baseurl}}/img_compressed/smoothed_pc.svg' alt='smoothed_pc'>
</a>

<p>
    We investigated the pattern above further and found that it was due to F group's preference for easier tasks (especially 1D) and S group's preference of harder tasks (especially R). Examine <a href='#f-2-2-2' class='animated'>Figure 2.2.2</a>. The dotted selection curves indicate that consistently over the entire free play period, there was a higher proportion of people in the F group who played 1D than in the S group, and vice versa for the R task. Similar observations can be made for large of portions of the free-play period regarding I1D and 2D. Namely, consistently higher proportion of people played I1D in the F compared to S group (approximately trials 75 to 210, and vice versa for trials 140 onwards for 2D task).</p>


<div class='caption' id='f-2-2-2'>
    <em>
        <b>Figure 2.2.2.</b> Average PC per trial and proportion of players on task during free play
    </em>
</div>
<a href='{{site.baseurl}}/img/smoothed_pc_free2.svg'>
    <img src='{{site.baseurl}}/img_compressed/smoothed_pc_free2.svg' alt='smoothed_pc_free2'>
</a>

<p>
    These patterns seem to be expressed at the individual level, as shown in the histograms in <a href='#f-2-2-3' class='animated'>Figure 2.2.3</a>. Notice the group differences in 1D and R. There were more individuals in the F group than in the S group who played 1D 30% to 80% of their total free-play time. And similarly, there where more of those played the R task 30% to 90% of the time in the S group compared to the F group. Moreover, there were fewer people in the F group who spent little time on 1D, and there were fewer people in the S group who spent little time on R. Importantly, the histograms also show that in both groups, the amount of time people spend on each task ranges widely from 0% to 90%. If we consider the free exploration group to be a baseline, it seems that an instruction to learn as much as possible and anticipation of a test lead some people to play the easy 1D task less and the impossible R task more. </p>

<div class='caption' id='f-2-2-3'>
    <em>
        <b>Figure 2.2.3.</b> Amount of time spent on each task during free play
    </em>
</div>
<a href='{{site.baseurl}}/img/histograms_of_time_spent_on_each_task.svg'>
    <img src='{{site.baseurl}}/img_compressed/histograms_of_time_spent_on_each_task.svg' alt='histograms_of_time_spent_on_each_task' style='width: 50%; height:auto; display: block; margin: 0 auto;/'>
</a>


<h3 id='s2.3'>2.3. A measure of self-challenge</h3>
<p>
    More people in the S group seem to challenge themselves (compared to the F group) by playing less of 1D and more of R. To characterize this more precisely, we operationalized the concept of self-challenge by introducing an interpretable baseline representing an appropriate level of self-challenge for learning the experiment's problem space efficiently.</p>

<p>
    The baseline challenge level is based on a simple principle: given some prior record of performance on a number of tasks (e.g. performance from familiarization stage), an appropriate level of challenge is provided by the easiest task that has not yet been learned. Choosing anything harder than this baseline is considered overchallenging, and choosing anything easier is underchallenging. Maintaining this baseline level of self-challenge is an efficient strategy for time-constrained exploration in a partially known problem space. It avoids wasting time on learned problems by signaling underchallenging choices. It also avoids being stuck with the impossible problem by driving people to towards the easiest unlearned tasks.</p>

<p>
    The baseline level of challenge can be computed at any trial. It is determined by two factors: the difficulty of the tasks, and whether or not the tasks are learned. At any given point in time, subjective task difficulty and the extend to which the task is learned can be approximated by the observed PC. Specifically, the easiest task is simply the one with the highest PC, the next easiest is the one with the next highest PC and so on. To determine whether a task is learned we need to make several assumptions. First we assume that when a task is completely unknown, the probability of guessing food preference correctly is .5 (since there are two food choices available). We can call this probability our null hypothesis (no learning has occurred) and use it as a single parameter of the binomial probability mass function to get the probability of the alternative hypothesis:

    {% raw %}
        $$Pr_{H_1}(n, k) = \binom{n}{k} \frac{1}{2^n}$$
    {% endraw %}

    where <i>n</i> is the number of trials played so far, and <i>k</i> is the number of correct responses. The quantity <i>Pr<sub>H<sub>1</sub></sub></i>, which we call <i>p</i>-value, tells us how likely we are to observe <i>k</i> hits in <i>n</i> trials if all responses were entirely random guesses. The minimum <i>p</i>-values corresponded to subjective reports (see <a href='{{site.baseurl}}/content/materials/index.html#2-self-reports' class='animated'>Materials</a>) of the existence of a rule governing food preferences:</p>

<div class='caption' id='f-2-3-1'>
    <em>
        <b>Figure 2.3.1.</b> p-values correspond to subjective ratings of the existence of a rule
    </em>
</div>
<a href='{{site.baseurl}}/img/pval_cor_rule.svg'>
    <img src='{{site.baseurl}}/img_compressed/pval_cor_rule.svg' alt='pval_cor_rule'
         style='width: 60%; height:auto; display: block; margin: 0 auto;/'>
</a>

<p>
    People who failed to learn a rule had much higher minimum <i>p</i>-values compared to those who reported to have learned a rule. This was true for the learnable tasks, but not for the R task. Interestingly, the difference in <i>p</i>-values between rule-absent (≤5) and rule-present (>5) ratings decreased as a function of task difficulty. People needed higher <i>p</i>-values to give low scores for 1D and I1D compared to 2D. At the same time, higher <i>p</i>-values were associated with rule-present scores for more difficult tasks. So, for harder tasks, <i>p</i>-value based performance was not as good an indicator of a rule as it was for simpler tasks. </p>

<p>
    The <i>p</i>-values can be used to define other measures of learning. We can select a threshold, e.g. 0.01 to tell us whether a certain PC over a certain number of trials counts as learning. In other words, we can consider a task "learned" when the probability that the observed PC on that task came from random guessing is less than 1%. The use of <i>p</i>-values and a threshold also allowed us to define a <b>learning point</b> as the first trial on which learning as we define it has occurred.</p>

<p>
    To verify that our threshold-based learning criterion works as intended, we looked at the amount of people who learned each task (<a href='#f-2-3-2' class='animated'>Figure 2.3.2.a </a>) as well as the average time of (the first) learning points for each task (<a href='#f-2-3-2' class='animated'>Figure 2.3.2.b</a>).</p>


<div class='caption' id='f-2-3-2'>
    <em><b>Figure 2.3.2.</b></em>
</div>
<table>
    <tr>
        <td align='center'>
            (a)<br>Proportions of learners in each group by task
        </td>
        <td align='center'>
            (b)<br>Average time of the first learning point (by learnable task)
        </td>
    </tr>
    <tr>
        <td>
            <a href='{{site.baseurl}}/img/learners_bars.svg'>
                <img src='{{site.baseurl}}/img_compressed/learners_bars.svg' alt='learners_bars'>
            </a>
        </td>
        <td>
            <a href='{{site.baseurl}}/img/learning_points.svg'>
                <img src='{{site.baseurl}}/img_compressed/learning_points.svg' alt='learning_points'>
            </a>
        </td>
    </tr>
</table>

<p>
    As you may have noticed in <a href='#f-2-3-1' class='animated'>Figure 2.3.1</a>, under 10% of people in both F and S groups learned the unlearnable task. Indeed, our definition of learning makes this paradox possible (although unlikely), but note also that the subjects did not know in advance which task was unlearnable, so having certain experiences with the R task could make an impression that the task could be and/or was learned. More importantly, we see the expected, difficulty-based decline in the the number of learners. Overall, it appears that the S group learned more, especially the hardest learnable 2D task. Subfigure (b) shows the average time (averaged across subjects) of the first learning point. Here, the F group shows the anticipated pattern where 1D is learned first, followed by I1D, followed by 2D. Compared to group F, people in the S group appear to have learned 1D later. It also seems like they sacrificed the play time for 1D in favor of exploring more difficult tasks. These group differences in learning outcomes appear to be related to the measure of self-challenge discussed next.</p>

<p>
    Having defined an operational criterion for learning, we proceeded to examine the levels of self-challenge relative to the baseline. Concretely, this <b>self-challenge index (SC)</b> corresponds to the difference between PC of the appropriately challenging task and PC of the task that was actually chosen. This score can be calculated on the level of trials, individuals, groups and so on. <a href='#f-2-3-3' class='animated'>Figure 2.3.3</a> shows the relationships between individual-level SC (averaged across trials) and the selection rate of each task. Data points were split by group and regression lines were fit for each split. Correlation coefficients and significance levels are also shown for pooled data.</p>

<div class='caption' id='f-2-3-3'>
    <em>
        <b>Figure 2.3.3.</b> Relationship between task selection rates and self-challenging
    </em>
</div>
<a href='{{site.baseurl}}/img/sc_cor_sr.svg'>
    <img src='{{site.baseurl}}/img_compressed/sc_cor_sr.svg' alt='sc_correlations_sr' style='width: 60%; height:auto; display: block; margin: 0 auto;/'>
</a>

<p>
    Nearly all correlations were highly significant. SC and selection rates of 1D and I1D were strongly negatively correlated, while the correlation between SC and R was strongly positively correlated. Interestingly, selection rate of 2D and SC were positively related in the F group only. Therefore, relatively overchallenging exploration in the S stemmed primarily from playing the R task more. This is rather surprising, given the observed differences between the groups on the 2D task:</p>

    <ul>
        <li>
            Group S did slightly better on the 2D task during testing (see <a href='#f-2-1' class='animated'>Figure 2.1</a>) </li>
        <li>
            Group S seemed to have played this task slightly more (<a href='#f-2-2-2' class='animated'>Figure 2.2.2</a> and <a href='#f-2-2-3' class='animated'>Figure 2.2.3</a>)</li>
        <li>
            More people in group S learned the 2D task (<a href='#f-2-3-2' class='animated'>Figure 2.3.2</a>) </li>
    </ul>

<p>
    The lack of a relationship between the selection rate of 2D and SC suggest that participants in group S played this task without over- or underchallenging themselves, which could explain why learning 2D in that group tended to be slightly better (see <a href='#f-2-3-2' class='animated'>Figure 2.3.2</a>).</p>



<p>
    Next, <a href='#f-2-3-4' class='animated'>Figure 2.3.4</a> shows the distributions of the SC scores for individual trials, splitting them by group. It is important to note that following the baseline level of self-challenge sometimes implies that one should switch from the current task (whether because staying is under- or overchallenging) and sometimes that one should keep playing the current task (because it is the easiest task that hasn't yet been learned). Accordingly, we distinguish between switch and stay predictions and show them in the subpanels of <a href='#f-2-3-4' class='animated'>Figure 2.3.4</a></p>.

<div class='caption' id='f-2-3-4'>
    <em>
        <b>Figure 2.3.4.</b> Distributions of SC scores at the trial level
    </em>
</div>
<a href='{{site.baseurl}}/img/sc_histogram.svg'>
    <img src='{{site.baseurl}}/img_compressed/sc_histogram.svg' alt='sc_histogram' style='width: 60%; height:auto; display: block; margin: 0 auto;/'>
</a>

<p>
    The figure shows that there were more instances of overchallenging in the S group compared to the F group. We can also see that when people need to stay on the current task in order to maintain the baseline level of self-challenge they almost always do. However, when the baseline-challenge strategy requires switching, behavior is more diverse: there are many instances of underchallenging (indicating a bias to stick to the current task, even if performance is very consistently high) and overchallenging. Nevertheless, there is a distinct mode for the baseline level choices in both groups, showing that in many instances people did switch appropriately. Importantly, the S groups seems to underchallenge less and overchallenge more (relative to the baseline) compared to the F group, which is again consistent with task selection observations in <a href='#2.2._Task_selection_during_free_play_' class='animated'>Section 2.2</a>. Note however, that these plots may obscure temporal patterns of SC (see below). </p>

<p>
    We also looked at how SC behaved at a group level over time. We first split all SC scores by group and within each group split them further by the number of tasks learned (learning breadth; <a href='#f-2-3-5' class='animated'>Figure 2.3.5</a>). That gave us 4 subgroups within each instruction group. Both instruction and learning breadth seem to have had an effect on the temporal trajectory of SC. </p>

<!--
<div class='caption' id='f-2-3-4'>
    <em> <b>Figure 2.3.4.</b>
        <br> (a) Group-level SC over time split by breadth of learning
    </em>
</div>
<a href='{{site.baseurl}}/img/sc_and_breadth_hardest.svg'>
    <img src='{{site.baseurl}}/img_compressed/sc_and_breadth_hardest.svg' alt='sc_and_breadth_hardest'>
</a>
-->
<div class='caption' id='f-2-3-5'>
    <em>
        <b>Figure 2.3.5.</b> Group-level SC over time split by number of tasks learned
    </em>
</div>
<a href='{{site.baseurl}}/img/sc_and_breadth_numtasks.svg'>
    <img src='{{site.baseurl}}/img_compressed/sc_and_breadth_numtasks.svg' alt='sc_and_breadth_numtasks' style='width: 60%; height:auto; display: block; margin: 0 auto;/'>
</a>

<p>
    SC declined slowly over time across the board, except for the subgroup who haven't learned a single task (these are likely to be the people who over-played the R task, which hindered their progress on the other tasks). The observed gradual decrease might reflect a ceiling effect of our guessing game <a id='backto2' href='#fn2' class='animated'>[2]</a>. Specifically, note how the worst learners (1-task learners) in both groups underchallenged less than the best learners (3-tasks learners). This difference is because unless one commits to the R task after learning all learnable tasks, they will most likely underchallenge. So good learners who learn all tasks early, but don't stick to the R task afterwards, will underchallenge.</p>

<p>
    Another striking difference between the groups is the variance of SC in the beginning of free play. In the freely exploring group, better learners start with baseline-challenge choices, while the worse learners overchallenge. The strategic group's instructions seem to have lead to a less diverse set of behaviors: good and bad learners alike start by overchallenging. Thus, in the most unconstrained setting of our study, the best learners happened to be the ones who followed the baseline strategy (until there was nothing else to learn), while worse learners were the ones who failed to maintain the appropriate level of challenge. However, when instructed to learn as much as possible about the problem space and informed about an upcoming test, most people started by playing tasks on which their performance was low. It appears that eventually (approximately by trial 50) some of these people realized their overchallenging behavior and switched to a more manageable task.</p>


<p>
    The pattern above suggests that exploration was more structured initially but became less coherent over time. So, earlier stages of free play could tell us more about exploration than later periods. Indeed, we can see a dramatic differences in the distributions of SC scores at the trial level for earlier trials (<a href='#f-2-3-6' class='animated'>Figure 2.3.6</a>) compared to all trials (<a href='#f-2-3-3' class='animated'>Figure 2.3.3</a>):</p>

<div class='caption' id='f-2-3-3'>
    <em>
        <b>Figure 2.3.6.</b> Distributions of SC scores at the trial level (first 100 trials only)
    </em>
</div>
<a href='{{site.baseurl}}/img/sc_histogram_first100.svg'>
    <img src='{{site.baseurl}}/img_compressed/sc_histogram_first100.svg' alt='sc_histogram_first100' style='width: 60%; height:auto; display: block; margin: 0 auto;/'>
</a>

<p>
    Isolating the first 100 trials reveals that our baseline-based model predicted switching on a higher proportion of trials (82%, compared to 75% when we looked at all trials). However, we can also see that most of these higher or lower than baseline challenge choices were close to the baseline, as indicated by high relative frequencies of SC scores close to 0. By ignoring the later trials of free play we especially decreased the relative frequency of underchallenging instances.</p>











<hr/>

<b>Footnotes</b>
<ol style='list-style-position:outside;'>
    <li id='fn1'>
        Elsewhere, the test stage was defined as a the last 5 trials of free play in order to include more data points. Because of the unconstrained nature of the free-play stage, not all subjects played all tasks, and the bigger the window of last <i>n</i> trials is used to calculate test PC, the more participants are excluded for not having a sufficient number of minimum trials played. <a href='#backto1' class='animated'>[back]</a>
    </li>
    <li id='fn2'>
        But note the the inclusion of the R task does allow a subject to stay constantly around 0 (provided that the subject never learns it) <a href='#backto2' class='animated'>[back]</a>
    </li>
</ol>
