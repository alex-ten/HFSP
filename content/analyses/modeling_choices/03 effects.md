---
title: Quality of predictors
category: modeling_choices
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

As BIC is less tolerant to variables with small effects, some of the variables that seemed to have a considerable (negative) effect on AIC did not sufficiently reduce BIC. This provides further evidence supporting the importance of some of the variables.

Finally, it is interesting to look at how the variables contributed to model accuracy:

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

### 3.2. Akaike weights

The analyses in the previous section give us some idea about the relative importance of different variables, but tell us little about their particular effects on the dependent variable in question, the task choices. For that, we need to look at individual models. However, since we have taken an all-subset approach, we have many models, some of which are not much different from each other. This can be seen by looking at the differences between the minimum-AIC model and other models:

$$ \Delta_i = AIC_i - AIC_{min} $$

Conventionally, a score less than 2 indicates a lack of sufficient differences between the models to select one over the other (see <a href='{{base.url}}/pdfs/Burnham2004.pdf' class='animated' target='_blank'>Burnham & Anderson, 2004</a>). In our set, there were 41 models at a distance less than 2 from the lowest-AIC model. Another useful measure that tells us of the relative quality of individual models is the Akaike weight:

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

This can't be helped by restricting the set of models to only those with lower AIC values (e.g. by AIC < 5,000 criterion) since there are still a lot of them. So, there is considerable uncertainty as to which model should be selected. Nevertheless, these weights can be used cumulatively across many models to indicate the importance of individual parameters (and the corresponding variables). Concretely, we can add up Akaike weights across models that included each of the variables to obtain individual parameter weights (e.g. if there were 3 models that included `pval` with weights, .1, .2, and .3, the parameter weight for `pval` would be equal to .6).The figure below shows these cumulative parameter weights across all models in our analysis:

<a href='{{site.baseurl}}/r/param_weights.svg'><img src='{{site.baseurl}}/r/param_weights.svg' alt='Akaike_param_weights'></a>

Note that variables `pc` and `sc` were highly correlated, so each model that included both was not fit. Therefore, there Akaike weighting procedure does not apply equally well to these two variables as there were less (fitted) models that included them. However, since we saw that each had a relatively large effect on AIC reduction, I will include it in the variable selection exercise that follows.

### 3.3. Variable selection

Akaike weights suggest some relative importance of variables not pointed out by the regression approach, including `prog`, `scsq`, and `lrn2`. Upon some critical reflection, some self-reported measures appear to be in ambiguous relationships with task choices, because of the tendency of subjects to stick to the newly chosen task and the tendency to perform better on that task as a result. The `time` variable is the most straightforward example: if a subject switches to a certain task, they will likely stick to it for several trials and thus report more time spent on that task. Subjective progress ratings are likely to be correlated with time spent on a task, since more time on a task improves performance. These kinds of variables aid in predicting task choices considerably, but contribute little to explaining them. So despite their effect on reducing model AIC, it is best to dismiss them.

Other variables are even more tricky. For instance, it is not clear what time instance(s) (or period(s)) the reported **interest** ("Rate each monster family based on how much you were interested in discovering what they preferred eating ...") reflects. It is not controversial to say that a momentary interest in a certain task should add to the tendency to switch to that task at that instant, but it is difficult to say how interest in a task at time point A affects the tendency to choose that task at some distant time B. It is equally unclear how some general, ineffable sentiment about interest in a task (disregarding specific time) should predict task switches. Moreover, the very act of asking someone to rate interest in something might increase one's curiosity about that thing; whereas no such interest would have manifested, had the question not suggested it. Considering all that, I think we cannot justifiably relate the interest ratings to task choices. Some or all of the same logic applies to self-reported ratings of current and future learnability (`lrn` and `lrn2`), complexity (`comp`) and (`rule`). It might be useful to consider models with only objective behavioral predictors: `relt`, `pval`, `pc`, `pcr`, `scsq`, `pct`, and `tord`.

Since Akaike information criterion scores are essentially relative to a given set of candidate models, we can re-evaluate the relative importance of each of these variables against the backdrop of a more restricted pool of variables. This time, I have limited the candidate set of models to only include predictor subsets of the 7 behavioral variables mentioned above. This amounts to 255 model fits. Below is the list of top 10 AIC-ranked candidates:

<pre class='codeblock'>
                                                          form nvars    loglik  accuracy      AIC      BIC
             nxt ~ currentd + pcr + pval + relt + scsq | 1     5 -2259.106 0.4394724 4534.213 4579.497
       nxt ~ currentd + pct + pcr + pval + relt + scsq | 1     6 -2258.253 0.4342911 4534.506 4585.452
        nxt ~ currentd + pcr + pc + pval + relt + scsq | 1     6 -2258.500 0.4338201 4535.000 4585.945
                    nxt ~ currentd + pcr + pval + relt | 1     4 -2260.593 0.4295808 4535.186 4574.810
              nxt ~ currentd + pct + pcr + pval + relt | 1     5 -2259.784 0.4281677 4535.569 4580.853
      nxt ~ currentd + tord + pcr + pval + relt + scsq | 1     6 -2258.848 0.4418276 4535.697 4586.642
nxt ~ currentd + tord + pct + pcr + pval + relt + scsq | 1     7 -2257.896 0.4319359 4535.793 4592.399
               nxt ~ currentd + pcr + pc + pval + relt | 1     5 -2260.092 0.4309939 4536.185 4581.469
 nxt ~ currentd + tord + pcr + pc + pval + relt + scsq | 1     7 -2258.183 0.4333490 4536.366 4592.972
  nxt ~ currentd + pct + pcr + pc + pval + relt + scsq | 1     7 -2258.243 0.4342911 4536.486 4593.092
</pre>

Repeating another step from the previous analysis, we can see that the two most dominant variables still have very large effects. However, there are some differences. Both `relt` and `pval` have smaller effects. Also, `pc` and `pct` had their impacts on AIC reduced. One the other hand, `pcr` had a larger negative effect on AIC.

<pre class='codeblock'>
                Estimate Std. Error      t value      Pr(>|t|)
currentd    -1039.939170   8.391335 -123.9301149 1.057172e-223
relt         -151.207973   8.391335  -18.0195362  7.476202e-47
pval          -86.575006   8.391335  -10.3171905  5.687574e-21
pc             -6.549726   8.391335   -0.7805344  4.358268e-01
pcr            -3.430711   8.391335   -0.4088397  6.830130e-01
scsq           -2.581166   8.391335   -0.3075990  7.586478e-01
pct            -2.077423   8.391335   -0.2475676  8.046755e-01
tord            2.655720   8.391335    0.3164836  7.519039e-01
(Intercept)  5738.961272  12.788408  448.7627582  0.000000e+00
</pre>

Cumulative Akaike weights show a similar pattern. However, models with `pc` do not seep to be as important as the regression approach suggests. Instead, there seems to be a tapering trail of importance of `pcr`, `scsq`, `pct`, and `pc`:

<a href='{{site.baseurl}}/r/cum_weights_behav.svg'><img src='{{site.baseurl}}/r/cum_weights_behav.svg' alt='Akaike_cum_weights_behav'></a>

### 3.4. A closer look at behavioral variables
We can now closely examine the best model from the smaller subset as suggested by AIC. This model includes 4 best behavioral variables available: `relt`, `pval`, `pc`, and `scsq`.

#### 3.4.1. Model confusion
First, let us take a look at the quality of model predictions. Overall, the accuracy is better than chance (~ 37%), but clearly, the model makes false predictions more often than not. Below is the confusion matrix of the model, along with a number of related statistics:

<pre class='codeblock'>
Confusion Matrix and Statistics

          Reference
Prediction   1   2   3   4
         1  79  36  41  42
         2 105 210  93  86
         3 130 109 273  90
         4 150 168 140 371

Overall Statistics
                                          
               Accuracy : 0.4395          
                 95% CI : (0.4182, 0.4609)
    No Information Rate : 0.2774          
    P-Value [Acc > NIR] : < 2.2e-16       
                                          
                  Kappa : 0.2434          
 Mcnemar's Test P-Value : < 2.2e-16       

Statistics by Class:

                     Class: 1 Class: 2 Class: 3 Class: 4
Sensitivity           0.17026  0.40153   0.4991   0.6299
Pos Pred Value        0.39899  0.42510   0.4535   0.4475
Neg Pred Value        0.80000  0.80786   0.8199   0.8315
Prevalence            0.21856  0.24635   0.2577   0.2774
Detection Rate        0.03721  0.09892   0.1286   0.1748
Detection Prevalence  0.09326  0.23269   0.2836   0.3905
Balanced Accuracy     0.54926  0.61201   0.6452   0.6657
</pre>

Sensitivity (also called recall) is the ratio of true positives and false negatives. The number of correct guesses is divided by the number of misses for a given class (in the confusion matrix above it is the number on a diagonal divided by the column sum of off-diagonal elements). Intuitively, it tells us how many trials on which in reality a certain task was preferred to other alternatives was correctly identified. We can see that the model is more confused by trials on which easier tasks are selected. Sensitivity is the lowest for 1D, and increases with task difficulty. This might reflect the slight imbalance of predicted classes (i.e. a bias toward more frequent observations, see confusion matrix prevalence scores), but may also indicate that choosing a harder task corresponds to more structured behavior (considering our set of predictors). This could imply that switching to an easy task may be driven by factors that we did not account for, such as boredom which was not explicitly included as a predictor. Note however, that `relt` could be correlated with boredom.

Finally, precision (positive predictive value) is the ratio of true positives and the sum of true and false positives. It tells us the amount of correct guesses relative to all positive guesses of a given class. In other words, out of all guesses the model made for a certain class, what proportion was correct? Here again we see that the model was more precise in predicting more difficult tasks.

#### 3.4.2. Estimates of fixed effects
The table below shows the values of fitted parameters:

<pre class='codeblock'>
Coefficients :
                 Estimate  Std. Error z-value  Pr(>|z|)    
2:(intercept)    0.078753    0.069234  1.1375   0.25533    
3:(intercept)    0.062078    0.075996  0.8169   0.41401    
4:(intercept)    0.024365    0.086536  0.2816   0.77829    
currentd       -21.264302 1714.250055 -0.0124   0.99010    
pcr             -0.277324    0.126434 -2.1934   0.02828 *  
pval             3.210516    0.596565  5.3817 7.380e-08 ***
relt            -1.385366    0.274082 -5.0546 4.314e-07 ***
scsq            -0.898549    0.522936 -1.7183   0.08575 .  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
</pre>

- **`currentd`** has a large effect but lacks statistical significance. That is because its standard error is very large, which is in turn, a reflection of large sampling variation of the corresponding estimate. I do not fully understand why the sampling variation for a dummy variable should be so large. I understand that it helps prediction by increasing the number of true negatives (people do not switch to tasks they are currently playing) but does not help to increase the true positive rate. But I am not sure why it means that sampling variation of the corresponding parameter estimate should be so large. 

- **`pval`**. The model suggests a significant positive effect of `pval`. The positive sign means that tasks with higher `pval` were more likely to be switched to (remember that `pval` is interpreted as the true likelihood of a binary distribution with .5 probability of success). In other words, the more probable it was that responses on a certain task were random (i.e. that the task has not been learned) the more likely it was selected on a switch trial. This is in line with a learning-based exploration, since the subjects seem to choose unlearned tasks. Our group-level regression does not tell us whether it is some subjects that follow such a strategy or whether most subjects do, but only sometimes.

- **`relt`** had a highly significant negative effect on task selection. It appears that tasks on which participants were spending less time, relative to other tasks, were more likely to be chosen. This suggests a tendency to actively explore parts of the environment that have been neglected in the past. It does not indicate the lack of exploitation, however, since we are only looking at switch trials and as we have seen there seemed to be a lot of sticking to easy tasks.

- **`scsq`**, the squared challenge score indicates the optimality of task difficulty (measured by as total percent of correct responses). The closer the score is to 0, the less over- or under-challenging it is relative to the baseline-optimum level of challenge, defined as the `pc` of the easiest task not yet learned, as indicated by a cutoff criterion of `pval`. The negative effect (marginally significant) effect suggests a slight tendency to chose optimally challenging tasks.