---
title: Multinomial logistic model
category: modeling_choices
doctype: entry
entrynum: 1
---

### The setup

In this section, I will describe some preliminary steps taken to perform model selection. As you remember, we are trying to find a good model of task choice, given a prior decision to end the current streak and choose a different task (i.e. considering "switch" trials only). I considered a multinomial logistic regression family of models that assume that a task with maximal value (or utility) is chosen amongst alternatives. The value is computed as a linear combination of individual-specific and task-specific predictors (see Yves Croissant's tutorial <a href='{{base.url}}/pdfs/Croissant_2012_mlogit.pdf' class='animated' target='_blank'>[pdf]</a>{: .animated} for more information on conditional logistic regression). For example, facing a set of choices, an individual might consider her current level of performance on each of the tasks or how interesting she finds the each of the tasks to be (alternative-specific variables). The choice might also be influenced by the individual characteristics, like group assignment (individual-specific variable).

Given the exploratory nature of this effort, I have identified a set of 19 potentially interesting predictors. These include various measures of performance, time spent on each task, subjective ratings, and several other:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 892px">
<colgroup>
<col style="width: 92px">
<col style="width: 89px">
<col style="width: 499px">
<col style="width: 212px">
</colgroup>
  <tr>
    <th class="tg-c3ow">Variable name</th>
    <th class="tg-c3ow">Abbreviation</th>
    <th class="tg-0pky">Description</th>
    <th class="tg-c3ow">Values</th>
  </tr>
  <tr>
    <td class="tg-c3ow">current dummy</td>
    <td class="tg-c3ow">currentd</td>
    <td class="tg-0pky">Dummy variable for indexing the current task being played (the task played right before the switch)</td>
    <td class="tg-c3ow">{0, 1}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">training order</td>
    <td class="tg-c3ow">tord</td>
    <td class="tg-0pky">Ordinal variable indexing the order in which the task appeared during training.</td>
    <td class="tg-c3ow">{1,2,3,4}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">PC training</td>
    <td class="tg-c3ow">pct</td>
    <td class="tg-0pky">Continuous variable representing the hit rate over the training trials. In actuality, it's a discrete variable, due to a fixed number of training trials (same is true for other PC and PC-related measures).</td>
    <td class="tg-c3ow">[0; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">PC rolling</td>
    <td class="tg-c3ow">pcr</td>
    <td class="tg-0pky">Continuous variable representing the hit rate over the last 5 trials of the most recent streak. If less than 5 trials were played before a switch, the score is derived by averaging by the number of trials played.</td>
    <td class="tg-c3ow">[0; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">PC overall</td>
    <td class="tg-c3ow">pc</td>
    <td class="tg-0pky">Continuous variable representing the hit rate over the entire time played so far on a task.</td>
    <td class="tg-c3ow">[0; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">P-value</td>
    <td class="tg-c3ow">pval</td>
    <td class="tg-0pky">Continuous variable representing the probability of the current hit rate, assuming no learning (random guessing). More precisely, it is the likelihood of uniform probability in a binomial distribution with a given number of trials and a given number of hits. </td>
    <td class="tg-c3ow">[0; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Relative time</td>
    <td class="tg-c3ow">relt</td>
    <td class="tg-0pky">Continuous variable representing the amount of time spent on a task relative to time spent on other tasks (i.e. time spent on tasks, normalized by the total play time)</td>
    <td class="tg-c3ow">[0; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Self-challenge</td>
    <td class="tg-c3ow">sc</td>
    <td class="tg-0pky">Continuous variable representing the difference between the PC overall of the a task, and the PC overall of the task providing a baseline level of challenge. The baseline level of challenge is determined by whether the task was learned and its current success rate.</td>
    <td class="tg-c3ow">[-1; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Self-challenge squared</td>
    <td class="tg-c3ow">scsq</td>
    <td class="tg-0pky">Continuous variable representing the deviation from baseline level of self-challenge (values close to 0 represent optimal challenge level, and those close to 1 represent either over- or under-challenging choices).</td>
    <td class="tg-c3ow">[0; 1]</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Learnability 1</td>
    <td class="tg-c3ow">lrn</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of learnability of a task. This rating was given right after training and before free-play.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Interest</td>
    <td class="tg-c3ow">int</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of interest in a task. This rating was given at the very end of the game.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Complexity</td>
    <td class="tg-c3ow">comp</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of complexity of a task. This rating was given at the very end of the game.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Time</td>
    <td class="tg-c3ow">time</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of time spent on a task over the free play period. This rating was given at the very end of the game.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Progress</td>
    <td class="tg-c3ow">prog</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of progress made on a task over the free play period. This rating was given at the very end of the game.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Rule</td>
    <td class="tg-c3ow">rule</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of the likelihood that a task had a rule for correct food choices. This rating was given at the very end of the game.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Learnability 2</td>
    <td class="tg-c3ow">lrn2</td>
    <td class="tg-0pky">Discrete variable representing the subjective rating of learnability of a task. This rating was given at the very end of the game.</td>
    <td class="tg-c3ow">minmax normalized {1, ..., 10}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Group</td>
    <td class="tg-c3ow">grp</td>
    <td class="tg-0pky">Discrete variable representing the group assignment. 0 represents no added instructions (Free play group) and 1 represents the inclusion additional instructions (Strategic group).</td>
    <td class="tg-c3ow">{0, 1}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Trial</td>
    <td class="tg-c3ow">trial</td>
    <td class="tg-0pky">Discrete variable representing the number of trials played so far across all tasks.</td>
    <td class="tg-c3ow">{1, 2, ..., N}</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Block trial</td>
    <td class="tg-c3ow">blkt</td>
    <td class="tg-0pky">Discrete variable representing the number of trials played in the current block (after the last switch).</td>
    <td class="tg-c3ow">{1, 2, ..., N}</td>
  </tr>
</table>

I have attempted to fit all partitions of the set these 19 predictors (resulting in 524,287 fitting attempts). Not all attempts were successful, due to strong correlations between some variables (e.g. pc and sc). Of all attempts, 393,215 were successful. Several variables from each successful fit were recorded, including:

- Model formula (form), in [R's formula object format](https://www.rdocumentation.org/packages/mlogit/versions/0.3-0/topics/mFormula){: .animated}, e.g. `y ~ x1 + x2 + x3 | z1 + z2`
- Number of variables  (nvars)
- Log likelihood (loglik)
- McFadden's R squared (mfR2). It is redundant, since it's derived from loglik, but the software provided it anyways, so there was no cost of computing it
- Accuracy of predictions (number of correct predictions divided by the total number of predictions)
- AIC
- BIC