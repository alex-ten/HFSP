---
title: Effects of IVs on model performance metrics
category: open_loop
doctype: entry
entrynum: 3
---

Next, I took a more systematic approach to examining the effects of individual predictors on model performance. A quick way to do this would be to fit a linear regression model of all predictor variables on a dependent performance metric (e.g. AIC). If we regress binary variables (0 = excluded from model, 1 included in model) on AIC, we can interpret the resulting coefficients as linear effects of including them on the relative estimated Kullback-Leibler distance between the corresponding model and the true model of our data:

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

Since all predictor variables are binary, we can directly compare the coefficients. Predictors `currentd`, `relt`, `time`, `pval`, and `int` had the largest negative effects on AIC (i.e. decreased the distance to the true model the most). Although the 10 best AIC-ranked models were not the same as the best BIC-ranked models, the relative importance of the predictors was the same when the variable inclusion data was regressed on BIC:

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

The ranking of the most important variables was preserved. 