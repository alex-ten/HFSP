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