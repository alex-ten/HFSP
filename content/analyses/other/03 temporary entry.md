---
title: Temporary entry
category: other
doctype: entry
entrynum: 3
---

### 3.1.  Self-challenge score
{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='1.1'
    label='Trials histogram' %}
[![alt]({{site.baseurl}}/img_compressed/sc_histogram.svg)]({{site.baseurl}}/img/sc_histogram.svg)

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='1.2'
    label='Trials histogram through time' %}
[![alt]({{site.baseurl}}/img_compressed/sc_histogram_through_time.svg)]({{site.baseurl}}/img/sc_histogram_through_time.svg)

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='1.3'
    label='Individuals histogram' %}
[![alt]({{site.baseurl}}/img_compressed/sc_histogram_subjs.svg)]({{site.baseurl}}/img/sc_histogram_subjs.svg)

### 3.2. Learners and learning points
{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='2.1'
    label='Learners' %}
{% include carousel2.html thumbnails='true' path='img/learners_bars.svg::img/learners_lines.svg' %}

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='2.2'
    label='Learning points' %}
[![alt]({{site.baseurl}}/img_compressed/learning_points.svg)]({{site.baseurl}}/img/learning_points.svg)


### Multimodel fitting
We can compare the weighted model against the full model in terms of the quality of their predictions. For that, we can look at the confusion matrices of the models. Before considering model predictions, note the slight imbalance in response frequencies:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-zv4m{border-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-lghr{border-color:#ffffff;text-align:center}
.tg .tg-aoco{border-color:#ffffff;text-align:right}
.tg .tg-19n4{font-weight:bold;border-color:#ffffff;text-align:center}
.tg .tg-h25s{font-weight:bold;border-color:#ffffff;text-align:right;vertical-align:top}
.tg .tg-ofj5{border-color:#ffffff;text-align:right;vertical-align:top}
</style>
<table class="tg" align='center'>
  <tr>
    <th class="tg-zv4m"></th>
    <th class="tg-lghr" colspan="4">Response frequencies</th>
  </tr>
  <tr>
    <td class="tg-zv4m"></td>
    <td class="tg-19n4">1D</td>
    <td class="tg-19n4">I1D</td>
    <td class="tg-19n4">2D</td>
    <td class="tg-19n4">R</td>
  </tr>
  <tr>
    <td class="tg-h25s">count</td>
    <td class="tg-aoco">464</td>
    <td class="tg-aoco">523</td>
    <td class="tg-aoco">547</td>
    <td class="tg-aoco">589</td>
  </tr>
  <tr>
    <td class="tg-h25s">%</td>
    <td class="tg-ofj5">21.9</td>
    <td class="tg-ofj5">24.6</td>
    <td class="tg-ofj5">25.7</td>
    <td class="tg-ofj5">27.8</td>
  </tr>
</table>

The overall accuracy of the full model (47.3%) was higher than that of the averaged model (44.0%) which is likely the result of the full model's overfitting:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-peng{font-weight:bold;background-color:#ffffff;border-color:#ffffff;text-align:right}
.tg .tg-oe15{background-color:#ffffff;border-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-01x7{background-color:#ffffff;border-color:#ffffff;text-align:right}
.tg .tg-wk8r{background-color:#ffffff;border-color:#ffffff;text-align:center;vertical-align:top}
.tg .tg-us2q{background-color:#ffffff;border-color:#ffffff;text-align:left}
.tg .tg-bqvo{background-color:#ffffff;border-color:#ffffff;text-align:center}
.tg .tg-ref9{font-weight:bold;background-color:#ffffff;border-color:#ffffff;text-align:right;vertical-align:top}
.tg .tg-c1kk{background-color:#ffffff;border-color:#ffffff;text-align:right;vertical-align:top}
</style>
<table class="tg" align='center'>
  <tr>
    <th class="tg-us2q"></th>
    <th class="tg-us2q"></th>
    <th class="tg-bqvo" colspan="9">Reference</th>
  </tr>
  <tr>
    <td class="tg-us2q"></td>
    <td class="tg-01x7"></td>
    <td class="tg-peng">1D</td>
    <td class="tg-peng">I1D</td>
    <td class="tg-peng">2D</td>
    <td class="tg-peng">R</td>
    <td class="tg-01x7"></td>
    <td class="tg-peng">1D</td>
    <td class="tg-peng">I1D</td>
    <td class="tg-peng">2D</td>
    <td class="tg-peng">R</td>
  </tr>
  <tr>
    <td class="tg-us2q" rowspan="4">Prediction</td>
    <td class="tg-peng">1D</td>
    <td class="tg-01x7">149</td>
    <td class="tg-01x7">54</td>
    <td class="tg-01x7">50</td>
    <td class="tg-01x7">49</td>
    <td class="tg-peng">1D</td>
    <td class="tg-01x7">230</td>
    <td class="tg-01x7">116</td>
    <td class="tg-01x7">126</td>
    <td class="tg-01x7">174</td>
  </tr>
  <tr>
    <td class="tg-peng">I1D</td>
    <td class="tg-01x7">101</td>
    <td class="tg-01x7">221</td>
    <td class="tg-01x7">95</td>
    <td class="tg-01x7">93</td>
    <td class="tg-peng">I1D</td>
    <td class="tg-01x7">105</td>
    <td class="tg-01x7">274</td>
    <td class="tg-01x7">115</td>
    <td class="tg-01x7">135</td>
  </tr>
  <tr>
    <td class="tg-peng">2D</td>
    <td class="tg-01x7">102</td>
    <td class="tg-01x7">117</td>
    <td class="tg-01x7">287</td>
    <td class="tg-01x7">99</td>
    <td class="tg-peng">2D</td>
    <td class="tg-01x7">89</td>
    <td class="tg-01x7">87</td>
    <td class="tg-01x7">256</td>
    <td class="tg-01x7">105</td>
  </tr>
  <tr>
    <td class="tg-ref9">R</td>
    <td class="tg-c1kk">112</td>
    <td class="tg-c1kk">131</td>
    <td class="tg-c1kk">115</td>
    <td class="tg-c1kk">348</td>
    <td class="tg-ref9">R</td>
    <td class="tg-c1kk">40</td>
    <td class="tg-c1kk">46</td>
    <td class="tg-c1kk">50</td>
    <td class="tg-c1kk">175</td>
  </tr>
  <tr>
    <td class="tg-oe15"></td>
    <td class="tg-wk8r" colspan="5">Full model</td>
    <td class="tg-wk8r" colspan="5">Averaged model</td>
  </tr>
</table>

Quite notably, there was a difference in the number of predictions made for 1D and R tasks between the models. The supposedly less overfitting averaged model seems to predict a lot less of R and a lot more of 1D compared to the full model, despite the actual prevalence of choices of R. 

We can also look at other confusion metrics:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-zh4n{font-weight:bold;border-color:#ffffff;text-align:right}
.tg .tg-km2t{font-weight:bold;border-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-zv4m{border-color:#ffffff;text-align:left;vertical-align:top}
.tg .tg-aoco{border-color:#ffffff;text-align:right}
.tg .tg-aw21{font-weight:bold;border-color:#ffffff;text-align:center;vertical-align:top}
.tg .tg-19n4{font-weight:bold;border-color:#ffffff;text-align:center}
.tg .tg-h25s{font-weight:bold;border-color:#ffffff;text-align:right;vertical-align:top}
.tg .tg-ofj5{border-color:#ffffff;text-align:right;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 586px" align='center'>
<colgroup>
<col style="width: 82px">
<col style="width: 47px">
<col style="width: 47px">
<col style="width: 47px">
<col style="width: 47px">
<col style="width: 48px">
<col style="width: 21px">
<col style="width: 58px">
<col style="width: 47px">
<col style="width: 47px">
<col style="width: 47px">
<col style="width: 48px">
</colgroup>
  <tr>
    <th class="tg-aw21" colspan="12">Confusion metrics</th>
  </tr>
  <tr>
    <td class="tg-km2t"></td>
    <td class="tg-19n4" colspan="5">Full model</td>
    <td class="tg-zv4m"></td>
    <td class="tg-aw21" colspan="5">Averaged model</td>
  </tr>
  <tr>
    <td class="tg-km2t"></td>
    <td class="tg-zh4n">1D</td>
    <td class="tg-zh4n">I1D</td>
    <td class="tg-zh4n">2D</td>
    <td class="tg-zh4n">R</td>
    <td class="tg-h25s">mean</td>
    <td class="tg-ofj5"></td>
    <td class="tg-h25s">1D</td>
    <td class="tg-h25s">I1D</td>
    <td class="tg-h25s">2D</td>
    <td class="tg-h25s">R</td>
    <td class="tg-h25s">mean</td>
  </tr>
  <tr>
    <td class="tg-h25s">Sensitivity</td>
    <td class="tg-aoco">0.321</td>
    <td class="tg-aoco">0.422</td>
    <td class="tg-aoco">0.524</td>
    <td class="tg-aoco">0.590</td>
    <td class="tg-ofj5">0.464</td>
    <td class="tg-ofj5"></td>
    <td class="tg-ofj5">0.495</td>
    <td class="tg-ofj5">0.524</td>
    <td class="tg-ofj5">0.468</td>
    <td class="tg-ofj5">0.297</td>
    <td class="tg-ofj5">0.446</td>
  </tr>
  <tr>
    <td class="tg-km2t">Precision</td>
    <td class="tg-ofj5">0.493</td>
    <td class="tg-ofj5">0.433</td>
    <td class="tg-ofj5">0.474</td>
    <td class="tg-ofj5">0.492</td>
    <td class="tg-ofj5">0.473</td>
    <td class="tg-ofj5"></td>
    <td class="tg-ofj5">0.356</td>
    <td class="tg-ofj5">0.435</td>
    <td class="tg-ofj5">0.476</td>
    <td class="tg-ofj5">0.562</td>
    <td class="tg-ofj5">0.457</td>
  </tr>
</table>

Sensitivity (also called recall) is the ratio of true positives and false negatives. That is, we divide the number of correct guesses by the number of misses for a given class. Intuitively, it tells us how many trials on which a certain task was preferred to other alternatives was correctly identified. The averaged model was more sensitive to easier tasks than the full model.


Finally, precision is the ratio of true positives and the sum of true and false positives. It gives us the amount of correct guesses out of all guesses for a given class. In other words, it tells us how many of model-predicted choices of a certain task were actually that task. So, on average the averaged model was more precise with the R task but less precise on the 1D task, compared to the full model.

Thus, the averaged model was better at identifying the correct choices of 1D than the full model (vice versa for R). However, the averaged model was at the same time less precise at identifying 1D, that is, more of its 1D guesses were wrong, compared to the full model (and vice versa for R).