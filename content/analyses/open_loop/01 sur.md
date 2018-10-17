---
title: Multinomial logistic model
category: open_loop
doctype: entry
entrynum: 1
---

Consider task selection as a classification problem. Given a set of certain quantities, what is the probability of selecting each of the available tasks? Suppose the task selection decision is carried out on every single trial by considering only the current task's percent correct (PC) and the relative amount of time spent on the current task (RT). These variables are combined into a single utility score for each task:


$$ u_{k,i} = b_k \cdot x_i $$


Here, \\(u_{k,i}\\) is the utility of task \\(k\\) on trial \\(i\\), \\(x_i\\) is the vector of input variables PC and RT, and \\(b_k\\) is a vector of free parameters (one for each input variable) associated with task \\(k\\). The utility scores are in turn combined (via softmax function) to yield a discrete probability distribution over the available choices:

$$ Pr(Y_i = c | x_i) = \frac{e^{b_c x_i}}{\sum_{k=1}^{K}e^{b_k x_i}} $$


where the \\(Pr(Y_i = c \mid x_i)\\) is the probability of choosing task \\(c\\) on trial \\(i\\), given \\(x_i\\), that is equal to the exponent of the utility of task \\(c\\) on trial \\(i\\), normalized by the sum of the exponentiated utilities over all tasks. In addition to classification probabilities, the model's free parameters can be interpreted in a simple way to describe the relationships between predictors and task selection. Suppose we had K classes and M predictors. The model would give us a set of K-by-M coefficients (one for each predictor-outcome pair), which when adjusted (pivoted) and exponentiated could be interpreted as the odds of choosing one task over another as the predictor changes in value. For example, coefficient \\(w_{k,m}\\) will give us:

$$ \frac{Pr(Y_i = k)}{Pr(Y_i = k')} = w_{k,m}x_{m,i} $$

where \\(x_{m,i}\\) is the \\(i\\)-th observation of \\(m\\)-th variable (e.g. percent correct), and \\(w_{k,m}\\) tells us how the odds of choosing task \\(k\\) relative to some reference (pivot) task \\(k'\\) changes along with variable \\(x_{m}\\).
