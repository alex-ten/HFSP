---
title: Descriptive stats
category: open_loop
doctype: entry
entrynum: 2
---

Below you can see several histograms of the recorded variables:

<a href='{{site.baseurl}}/r/hist_loglikelihood.svg'><img src='{{site.baseurl}}/r/hist_loglikelihood.svg' alt='hist_AIC'></a>
<a href='{{site.baseurl}}/r/hist_accuracy.svg'><img src='{{site.baseurl}}/r/hist_accuracy.svg' alt='hist_AIC'></a>
<a href='{{site.baseurl}}/r/hist_AIC.svg'><img src='{{site.baseurl}}/r/hist_AIC.svg' alt='hist_AIC'></a>
<a href='{{site.baseurl}}/r/hist_BIC.svg'><img src='{{site.baseurl}}/r/hist_BIC.svg' alt='hist_AIC'></a>

There are several clusters of models with better and worse performances. Each cluster likely corresponds to a single predictor whereas variability within a cluster is due to joint effects with other variables. The models with AIC < 5,000 were the same as the ones with BIC < 5,000. Thus, I separated the better performing models (based on AIC < 5,000) to get a closer look at the distributions of performance metrics. There were 196,608 such models:

<a href='{{site.baseurl}}/r/hist_loglikelihood_best.svg'><img src='{{site.baseurl}}/r/hist_loglikelihood_best.svg' alt='hist_AIC'></a>
<a href='{{site.baseurl}}/r/hist_accuracy_best.svg'><img src='{{site.baseurl}}/r/hist_accuracy_best.svg' alt='hist_AIC'></a>
<a href='{{site.baseurl}}/r/hist_AIC_best.svg'><img src='{{site.baseurl}}/r/hist_AIC_best.svg' alt='hist_AIC_best'></a>
<a href='{{site.baseurl}}/r/hist_BIC_best.svg'><img src='{{site.baseurl}}/r/hist_BIC_best.svg' alt='hist_AIC_best'></a>

Below are the top 10 models with lowest AIC (`1` on the righ-hand side of `|` of a formula means that no individual-specific variables were included):

<pre class='codeblock'>
                                                                           form nvars    loglik  accuracy      AIC      BIC
             nxt ~ currentd + pval + relt + scsq + int + time + prog + lrn2 | 1     8 -2163.376 0.4686764 4348.752 4411.019
       nxt ~ currentd + pcr + pval + relt + scsq + int + time + prog + lrn2 | 1     9 -2162.549 0.4677343 4349.099 4417.026
                    nxt ~ currentd + pval + relt + scsq + int + time + prog | 1     7 -2164.603 0.4658502 4349.206 4405.812
              nxt ~ currentd + pcr + pval + relt + scsq + int + time + prog | 1     8 -2163.655 0.4691474 4349.311 4411.577
  nxt ~ currentd + pct + pcr + pval + relt + scsq + lrn + int + time + prog | 1    10 -2161.773 0.4705605 4349.545 4423.133
       nxt ~ currentd + pval + relt + scsq + lrn + int + time + prog + lrn2 | 1     9 -2162.895 0.4724447 4349.790 4417.717
 nxt ~ currentd + pct + pcr + pval + relt + scsq + int + time + prog + lrn2 | 1    10 -2161.906 0.4710316 4349.811 4423.399
              nxt ~ currentd + pval + relt + scsq + lrn + int + time + prog | 1     8 -2163.921 0.4715026 4349.841 4412.108
        nxt ~ currentd + pct + pval + relt + scsq + lrn + int + time + prog | 1     9 -2162.949 0.4691474 4349.898 4417.825
       nxt ~ currentd + pct + pval + relt + scsq + int + time + prog + lrn2 | 1     9 -2162.955 0.4715026 4349.910 4417.837
</pre>

lowest BIC:

<pre class='codeblock'>
                                                 form nvars    loglik  accuracy      AIC      BIC
              nxt ~ currentd + pval + relt + time | 1     4 -2171.261 0.4682054 4356.522 4396.146
        nxt ~ currentd + pval + relt + int + time | 1     5 -2168.375 0.4667923 4352.750 4398.034
       nxt ~ currentd + pval + relt + time + prog | 1     5 -2168.839 0.4663212 4353.678 4398.963
       nxt ~ currentd + pval + relt + scsq + time | 1     5 -2169.515 0.4625530 4355.031 4400.316
       nxt ~ currentd + pval + relt + time + rule | 1     5 -2170.002 0.4620820 4356.005 4401.289
       nxt ~ currentd + pval + relt + time + lrn2 | 1     5 -2170.048 0.4705605 4356.096 4401.380
 nxt ~ currentd + pval + relt + int + time + prog | 1     6 -2166.327 0.4616109 4350.654 4401.599
        nxt ~ currentd + pval + relt + lrn + time | 1     5 -2170.541 0.4696185 4357.081 4402.366
 nxt ~ currentd + pval + relt + scsq + int + time | 1     6 -2166.782 0.4719736 4351.565 4402.510
nxt ~ currentd + pval + relt + time + prog + lrn2 | 1     6 -2166.920 0.4658502 4351.840 4402.785
</pre>

and highest accuracy:

<pre class='codeblock'>
                                                                                                               form nvars    loglik  accuracy      AIC      BIC
       nxt ~ currentd + tord + pcr + pval + relt + sc + scsq + lrn + comp + time + rule + lrn2 | grp + trial + blkt    15 -2161.542 0.4851625 4371.085 4506.939
 nxt ~ currentd + tord + pct + pcr + pc + pval + relt + scsq + lrn + time + prog + rule + lrn2 | grp + trial + blkt    16 -2159.711 0.4851625 4369.422 4510.937
 nxt ~ currentd + tord + pct + pcr + pval + relt + sc + scsq + lrn + time + prog + rule + lrn2 | grp + trial + blkt    16 -2159.711 0.4851625 4369.422 4510.937
nxt ~ currentd + tord + pct + pc + pval + relt + scsq + lrn + comp + time + prog + rule + lrn2 | grp + trial + blkt    16 -2160.194 0.4851625 4370.388 4511.903
nxt ~ currentd + tord + pct + pval + relt + sc + scsq + lrn + comp + time + prog + rule + lrn2 | grp + trial + blkt    16 -2160.194 0.4851625 4370.388 4511.903
             nxt ~ currentd + tord + pct + pcr + pval + relt + scsq + lrn + time + rule + lrn2 | grp + trial + blkt    14 -2160.922 0.4861046 4367.844 4498.038
      nxt ~ currentd + tord + pct + pcr + pval + relt + scsq + lrn + comp + time + rule + lrn2 | grp + trial + blkt    15 -2160.922 0.4861046 4369.844 4505.698
 nxt ~ currentd + tord + pct + pcr + pc + pval + relt + scsq + lrn + comp + time + rule + lrn2 | grp + trial + blkt    16 -2160.869 0.4861046 4371.737 4513.252
 nxt ~ currentd + tord + pct + pcr + pval + relt + sc + scsq + lrn + comp + time + rule + lrn2 | grp + trial + blkt    16 -2160.869 0.4861046 4371.737 4513.252
                          nxt ~ currentd + tord + pct + pcr + pval + relt + scsq + time + lrn2 | grp + trial + blkt    12 -2164.549 0.4865756 4371.097 4489.969
</pre>