---
title: Assessing quality of predictors
category: open_loop
doctype: entry
entrynum: 3
---

### 3.1. Effects of variable inclusion on model performance

Next, I took a more systematic approach to examining the effects of individual predictors on model performance. A quick way to do this is to fit a linear regression model of all predictor variables on a dependent performance metric (e.g. AIC). If we regress binary variables (0 = excluded from model, 1 included in model) on AIC, we can interpret the resulting coefficients as linear effects of including them on the relative estimated Kullback-Leibler distance between the corresponding model and the true model of our data:

<pre class='codeblock'>
              Estimate Std. Error    t value   Pr(>|t|)
currentd    -1016.0107     0.2928 -3469.6567  0.000e+00
relt         -242.0646     0.2928  -826.6459  0.000e+00
time         -127.6029     0.2928  -435.7616  0.000e+00
pval          -92.8800     0.2928  -317.1833  0.000e+00
int           -22.2639     0.2928   -76.0308  0.000e+00
pc             -8.4321     0.3586   -23.5114 3.785e-122
sc             -8.4321     0.3586   -23.5114 3.785e-122
pct            -5.5794     0.2928   -19.0535  6.682e-81
scsq           -2.8838     0.2928    -9.8480  7.034e-23
prog           -2.2432     0.2928    -7.6606  1.855e-14
pcr            -1.7125     0.2928    -5.8481  4.975e-09
lrn            -1.1741     0.2928    -4.0095  6.087e-05
rule           -0.5935     0.2928    -2.0270  4.267e-02
comp            0.2775     0.2928     0.9476  3.433e-01
lrn2            0.5177     0.2928     1.7679  7.708e-02
tord            1.5058     0.2928     5.1423  2.715e-07
grp             1.9731     0.2928     6.7381  1.607e-11
trial           3.0304     0.2928    10.3489  4.265e-25
blkt            4.3069     0.2928    14.7079  5.907e-49
(Intercept)  5763.8200     0.6548  8802.4410  0.000e+00
</pre>

Since all predictor variables are binary, we can directly compare the coefficients. Predictors `currentd`, `relt`, `time`, `pval`, and `int` had the largest negative effects on AIC (i.e. decreased the distance to the true model the most). Although the best 10 AIC-ranked models were not the same as the best BIC-ranked models, the relative importance of the predictors was the same when the variable inclusion data was regressed on BIC:

<pre class='codeblock'>
               Estimate Std. Error    t value   Pr(>|t|)
currentd    -1010.35014     0.2928 -3450.3259  0.000e+00
relt         -236.40402     0.2928  -807.3151  0.000e+00
time         -121.94236     0.2928  -416.4308  0.000e+00
pval          -87.21938     0.2928  -297.8525  0.000e+00
int           -16.60331     0.2928   -56.7000  0.000e+00
pc             -2.77154     0.3586    -7.7279  1.096e-14
sc             -2.77154     0.3586    -7.7279  1.096e-14
pct             0.08119     0.2928     0.2773  7.816e-01
scsq            2.77682     0.2928     9.4828  2.489e-21
prog            3.41736     0.2928    11.6702  1.832e-31
pcr             3.94809     0.2928    13.4827  2.021e-41
lrn             4.48650     0.2928    15.3213  5.707e-53
rule            5.06704     0.2928    17.3038  4.661e-67
comp            5.93807     0.2928    20.2784  2.223e-91
lrn2            6.17827     0.2928    21.0987  9.281e-99
tord            7.16640     0.2928    24.4731 3.591e-132
grp            18.95485     0.2928    64.7304  0.000e+00
trial          20.01220     0.2928    68.3413  0.000e+00
blkt           21.28865     0.2928    72.7003  0.000e+00
(Intercept)  5780.80174     0.6548  8828.3754  0.000e+00
</pre>

As BIC is less tolerant to variables with a small effect, some of the variables that had a good (negative) effect on AIC did not reduce the BIC. Finally, it is interesting to look at how the variables contributed to model accuracy:

<pre class='codeblock'>
              Estimate Std. Error  t value   Pr(>|t|)
(Intercept)  0.3243399 0.00014017 2313.921  0.000e+00
currentd     0.0593033 0.00006268  946.067  0.000e+00
relt         0.0457215 0.00006268  729.396  0.000e+00
pval         0.0288917 0.00006268  460.911  0.000e+00
time         0.0246570 0.00006268  393.354  0.000e+00
pc           0.0041124 0.00007677   53.566  0.000e+00
sc           0.0041124 0.00007677   53.566  0.000e+00
int          0.0037452 0.00006268   59.748  0.000e+00
scsq         0.0022145 0.00006268   35.328 5.871e-273
grp          0.0020553 0.00006268   32.788 1.849e-235
trial        0.0013895 0.00006268   22.167 8.389e-109
rule         0.0011699 0.00006268   18.664  1.051e-77
prog         0.0010843 0.00006268   17.297  5.229e-67
pct          0.0009359 0.00006268   14.930  2.159e-50
lrn2         0.0008101 0.00006268   12.924  3.363e-38
comp         0.0003969 0.00006268    6.333  2.414e-10
tord         0.0003541 0.00006268    5.649  1.616e-08
blkt         0.0001163 0.00006268    1.855  6.357e-02
pcr          0.0001102 0.00006268    1.759  7.863e-02
lrn         -0.0002819 0.00006268   -4.497  6.896e-06
</pre>

### 3.2. Model weighting

The analyses in the previous section give us some idea about the relative importance of different variables, but tell us little about their particular effects on the dependent variable in question, the task choices. For that, we need to look at individual models. However, since we have taken an all-subset approach, we have many models, some of which are not much different from each other. This can be seen by examining the differences between the AIC score of each model and the minimum AIC score of the set:

$$ \Delta_i = AIC_i - AIC_{min} $$

Conventionally, a score less than 2 indicates a lack of sufficient differences between the models to select one over the other. In our set, there were 41 models at a distance less than 2 from the lowest-AIC model. Another useful measure that tells us of the relative quality of individual models is Akaike weight (<a href='{{base.url}}/pdfs/SymondsMoussalli_2011_ModelSelection.pdf' class='animated'>Symonds & Moussalli, 2011</a>):

$$ w_i = \frac{ \exp (-\frac{1}{2} \Delta_i)}{\sum_{r=1}^{R} \exp(-\frac{1}{2} \Delta_r)} $$

where $$ \exp (-\frac{1}{2} \Delta_i) $$ is proportional to the relative likelihood of model $$ i $$, and $$ R $$ is the number of models in the set. The closer a model is to the lowest-AIC model, the higher its weight, relative to all others. The problem in our case is a big amount of models, and thus, very low weights even for the best models:

<pre class='codeblock'>
rank         AIC      delta            w
   1   4348.7521 0.00000000 0.0034711807
   2   4349.0986 0.34651244 0.0029189926
   3   4349.2057 0.45361657 0.0027667864
   4   4349.3109 0.55886515 0.0026249510
   5   4349.5450 0.79297337 0.0023349912
   6   4349.7901 1.03798690 0.0020657665
...

</pre>

This can't be helped by restricting the set of models to those with lower AIC values (by AIC < 5,000 criterion). So, there is considerable uncertainty as to which model should be selected. Since AIC makes no assumptions about whether the true model is in the set of fitted models, and since (I think) it is safe to assume that in fact none of the models we have come up with is in fact the true model, we should use all of the evidence we have on our hands. That is, we can use Akaike weights of all models to weight the fitted parameters of the full model with all 19 variables (though not very elegant, can be appropriate in exploratory model selection exercises <a href='{{base.url}}/pdfs/SymondsMoussalli_2011_ModelSelection.pdf' class='animated'>Symonds & Moussalli, 2011</a>).

Concretely, we can add up Akaike weights across models that included each of the variables to obtain predictor weights:

<a href='{{site.baseurl}}/r/param_weights.svg'><img src='{{site.baseurl}}/r/param_weights.svg' alt='Akaike_param_weights'></a>

Fitting a full model was not possible due to very high correlation between `pc` and `sc`, so a model excluding `sc` was fitted as the full model. Here is the summary of this model:

<pre class='codeblock'>
Coefficients :
                    Estimate     Std. Error  z-value     Pr(>|z|)    
2:(intercept)   -0.037099997    0.217001019 -0.17097     0.864250    
3:(intercept)   -0.137904928    0.226420916 -0.60906     0.542482    
4:(intercept)   -0.336228004    0.235045680 -1.43048     0.152579    
currentd       -21.139031605 1699.998818113 -0.01243     0.990079    
tord            -0.018274009    0.022089252 -0.82728     0.408078    
pct              0.442487977    0.345457553  1.28088     0.200238    
pcr             -0.164640265    0.161930457 -1.01673     0.309280    
pc              -0.202412645    0.506988647 -0.39924     0.689713    
pval             3.191226202    0.713099546  4.47515 0.0000076358 ***
relt            -3.273171784    0.333599191 -9.81169   < 2.22e-16 ***
scsq            -0.768264568    0.569458767 -1.34911     0.177300    
lrn              0.116491164    0.078847232  1.47743     0.139561    
int              0.143778877    0.070103372  2.05096     0.040271 *  
comp             0.061745518    0.135710540  0.45498     0.649124    
time             0.869563665    0.079529359 10.93387   < 2.22e-16 ***
prog             0.165318302    0.120715421  1.36949     0.170847    
rule             0.132016048    0.127191668  1.03793     0.299303    
lrn2             0.096779392    0.072237927  1.33973     0.180333    
2:grp            0.028532379    0.140604217  0.20293     0.839192    
3:grp            0.137169437    0.141739888  0.96775     0.333167    
4:grp            0.013584480    0.143135945  0.09491     0.924389    
2:trial          0.000361129    0.001053761  0.34270     0.731820    
3:trial          0.000182237    0.001081334  0.16853     0.866167    
4:trial          0.001391273    0.001103615  1.26065     0.207435    
2:blkt           0.001137344    0.002855512  0.39830     0.690411    
3:blkt          -0.000273179    0.002826106 -0.09666     0.922994    
4:blkt           0.002336238    0.002962794  0.78853     0.430390    
</pre>

And here are the weighted coefficients:

<pre class='codeblock'>
1  2:(intercept)  -0.037099996980
2  3:(intercept)  -0.137904928051
3  4:(intercept)  -0.336228003637
4       currentd -21.139031604590
5           tord  -0.005854365322
6            pct   0.213721925746
7            pcr  -0.075054980709
8             pc  -0.049975019357
9           pval   3.191128367691
10          relt  -3.273171784355
11          scsq  -0.189682007027
12           lrn   0.072604351775
13           int   0.068320624565
14          comp   0.048465197772
15          time   0.260456813165
16          prog   0.165318302263
17          rule   0.088075559417
18          lrn2   0.043655535170
19         2:grp   0.015367266258
20         3:grp   0.073878146671
21         4:grp   0.007316471164
22       2:trial   0.000030178123
23       3:trial   0.000015228784
24       4:trial   0.000116263114
25        2:blkt   0.000266034654
26        3:blkt  -0.000063899030
27        4:blkt   0.000546466308
</pre>

<a href='{{site.baseurl}}/r/weighted_coeffs.svg'><img src='{{site.baseurl}}/r/weighted_coeffs.svg' alt='weighetd_coeffs'></a>

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