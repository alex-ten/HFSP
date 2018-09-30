---
title: Multinomial logistic model
category: open_loop
doctype: entry
entrynum: 1
---

Consider task selection as a classification problem. Given a set of certain quantities, what is the probability of selecting each of the available tasks? Suppose the task selection decision is carried out on every single trial by considering the current task's percent correct (PC) and the relative amount of time spent on the current task (RT). These variables are combined into a single utility score for each task:


$$ u_{k,i} = b_k \cdot x_i $$


Here, \\(u_{k,i}\\) is the utility of task \\(k\\) on trial \\(i\\), \\(x_i\\) is the vector of input variables PC and RT, and \\(b_k\\) is a vector of free parameters (one for each input variable) associated with task \\(k\\). The utility scores are in turn combined (via a softmax function) to yield a discrete probability distribution over the available choices:

$$ Pr(Y_i = c | x_i) = \frac{e^{b_c x_i}}{\sum_{k=1}^{K}e^{b_k x_i}} $$


where the \\(Pr(Y_i = c \mid x_i)\\) is the probability of choosing task \\(c\\) on trial \\(i\\), given \\(x_i\\), that is equal to the exponent of the utility of task \\(c\\) on trial \\(i\\), normalized by the sum of the exponentiated utilities over all tasks. In addition to classification probabilities, the model's free parameters can be interpreted in a simple way to describe the relationships between predictors and task selection. The model gives us a set of K-by-M coefficients (one for each predictor-outcome pair), which when adjusted (pivoted) and exponentiated can be interpreted as the odds of choosing one task over another as the predictor changes in value. For example, coefficient \\(w_{k,m}\\) will give us:

$$ \frac{Pr(Y_i = k)}{Pr(Y_i = k')} = w_{k,m}x_{m,i} $$

where \\(x_{m,i}\\) is the \\(i\\)-th observation of \\(m\\)-th variable (e.g. percent correct), and \\(w_{k,m}\\) tells us how the odds of choosing task \\(k\\) relative to some reference (pivot) task \\(k'\\) changes as variable \\(x_{m}\\).

I tried this multinomial logistic regression approach with two percentage variables for a more straightforward interpretation. PC is the percent correct so far, and RT is the number of trials played on a task so far, normalized by the sum of all trials played so far. Note that the model considers predictor variable values of the task that is being played, ignoring the corresponding quantities of other tasks. I think this is a major drawback, which we should discuss. 

[Figure 1.1](#f-1-1){: .animated} below shows some of the results. Two models were fitted for each of the groups (I used the [statsmodels](https://www.statsmodels.org/dev/generated/statsmodels.discrete.discrete_model.MNLogit.html){: .animated} package to execute the fitting): 

{% 
    include caption.html 
    obj='figure' 
    num=page.entrynum
    ext=1
    label='Multinomial logit model' 
%}
[![MNLogit model]({{site.baseurl}}/img_compressed/MNLogit_pc_rt.svg)]({{site.baseurl}}/img/MNLogit_pc_rt.svg)

### Confusion matrices
Consider the confusion matrices first. Cells on the diagonal show the proportions of correct classifications, and those off the diagonal show incorrect predictions. For example, the free exploration group model made the correct prediction in 82.5% of all trials followed by 1D, but mispredicted 5.4%, 5.7% and 6.8% of those trials to be followed by tasks I1D, 2D, and R, respectively. Seems like both models do a descent job in terms of prediction, considering linearity of prediction, simplicity of predictors and their choice. It is also obvious that the S group's model is more accurate, which is consistent with our previous observation that the S group's behavior seemed more constrained and less variable. We can also see that tasks 1D and R are were easier to predict. Since the coefficients are stable across predictions, it means that selecting 1D and R is associated with relatively stable configurations of PC and RT. At the same time both model almost never incorrectly predict 1D selection. The situation is similar with the case of R task, but the F model confuses it with 2D 20% of the time. In fact, it does not do a good job in predicting 2D at all. 

Note that since we are considering all trials, it is be relatively easy to predict the selection on the next trial provided that there is a strong tendency to repeat the current task. For instance, if PC is consistently high on task 1D and consistently low on R, predicting that the next trial is 1D based on high PC on the current trial is relatively trivial. The confusion matrices seem to show how similar the performances were between different tasks in both groups.

### Percent correct
Now, let's look at the OvR (one-versus-rest) matrices. Note that for easier comparison, the colormap is normalized across all four color grids. The grids show coefficient values associated with PC and RT variables, adjusted according each class as a pivot. Let's begin with the *first row* of the F model's PC coefficients. Here, the reference class is 1D, so each entry off the diagonal in this row corresponds to the odds of choosing either I1D, 2D, or R over 1D as PC increases. Concretely, the odds of choosing I1D over 1D as PC increases by 1% is 0.971. Since it is smaller than 1, it means when PC on the current task increases, the probability that the next trial is 1D is greater than that of I1D. Considered as a whole, the coefficient matrix of the F model shows a tendency to stick to easier tasks, as coefficient values decrease consistently from left to right in each row. The PC table of the S model shows a similar but slightly weaker trend. However, consider the values under the diagonal in both tables (especially the bottom row). The odds of choosing a task easier than R associated with higher values of PC are higher for the F group compared to group S. This could mean that either (A) there were relatively more trials leading to selecting the R task with high PC values in the S group, or (B) that PC on the R task was higher in the S group. We know that B isn't true, so the difference in coefficients points to a more challenging task selection behavior in group S. That is, there were more high PC trials (e.g. 1D and I1D) followed by the R task. Although small, some of these differences between coefficients might be significant due to very narrow confidence intervals that the software gives.

### Relative time
The differences between coefficients of the RT variable of the two models are less subtle. Consider the odds of selecting a harder task over 1D as proportion of time spent on the current task increased. They are all less than 1 in the F group, but greater than 2 in the F group. So, trials followed by tasks harder than 1D tended to have higher portion of time spent relative to time spent on the alternatives. That means that either the S group people stuck to harder task more (increasingly so for harder tasks), or that they were more likely to switch to a harder task as the more and more time was being spent on the current task, or both. This pattern seems to be consistent across reference tasks in the S model, as shown by increasing coefficients (from left to right) in each row of the matrix. 

The F group shows a different but interesting pattern. There seems to be a bias against intermediate difficulty tasks: I1D and 2D. The bias is more obvious in the case of I1D. The odds of selecting 1D, 2D or R over I1D practically doubled as relative time spent on the current task increased. At the same time, the odds of selecting I1D over anything else halved as RT increased. So there were considerably less trials followed by I1D with a lot of time spent on the current activity. The same was true for the 2D task, but for a lesser degree. For some reason, participants in the F group seemed to switch to or stick to the easiest or the hardest tasks, not so much to intermediate ones.

### Predictions
We can use model coefficients to analyze and compare how different models behave under various conditions. [Figure 1.2](#f-1-2){: .animated} shows the probabilities made by each model as a function of PC and RT. Different rows show how predictions change as a function of RT, when PC is clamped to different values (40%, 60%, 80%, and 100%). Also note the black vertical lines at RT = 25, which are depicted as reference to the situation in which an equal amount of time is spent on all tasks (e.g. the first trial of free play). 

I suggest the following interpretation. Each subplot shows different scenarios (a PC and RTs) and relative frequencies of trials that were followed by each of the tasks. Lowest levels of RT are associated with the least popular tasks in both groups (I1D in group F and 1D in group S). So the only trials after which these unpopular options were selected were the trials on which the current RT value was low. Since switches were *very* rare compared to repetitions, these "unpopular selection trials" were mostly the ones on which the unpopular task itself was played. The same holds for other tasks too. In group F, the probability of selecting (and playing) 2D was the highest at intermediate level of PC (=60%) and when the time spent on the current trial was approximately between 20% and 30%. This probability decreases with time, because most likely, performance improves after playing the task (2D) a certain amount of time. Interestingly however, that at high levels of PC, spending more time on the current task meant spending more time on 1D in group F and on R in group S. For some reason sticking is associated with 1D and R, but not the intermediate tasks, probably because the intermediate tasks require effort but don't provide much reward. 1D seems to be rewarding for its easily obtainable positive feedback, and R could be rewarding for its potential disclosure. 

Also interestingly, the S model's predictions seem to be consistent across different levels of PC. Even high levels of current PC and RT lead to selecting R. This shows that the default behavior seen in some people in the F group of sticking to the easy task is overriden by instruction. When people reach high levels of PC on the current task and when they've spent a lot of time on it, they are likely to switch to R.


{% 
    include caption.html 
    obj='figure' 
    num=page.entrynum
    ext=2
    label='Model predictions' 
%}
[![MNLogit model predictions]({{site.baseurl}}/img_compressed/predictions_for_rt.svg)]({{site.baseurl}}/img/predictions_for_rt.svg)