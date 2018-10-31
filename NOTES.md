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