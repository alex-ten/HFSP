---
title: Initial performance and learning
category: descriptive
doctype: entry
entrynum: 2
---

### 2.1. Training and test PC distributions

We might see interesting patterns, if we differentiate the subjects by two criteria: by their initial performance and by their learning outcome. This will give us 4 groupings. Those who perform poorly initially can either improve, or fail to improve, and similarly, those who perform well in the beginning might improve slightly, or fail to improve (and more likely perform worse). Each of these groups may be reliably different in their exploration styles and self-reports. To help us split the subjects into each of these four groupings, we look at the distributions of the initial performance, performance at the end of free exploration, and learning outcome. 

Histograms in [Figure 2.1](#f-2-1){: .animated} show how the subjects from each of the groups performed on each of the *learnable* tasks at two stages of the experiment (PC training and PC test) as well as how well they learned (delta PC). The last row shows the distributions over the entire data collapsed across groups and tasks. The F group did not have an actual testing stage after the open-ended free play period. Rather than looking at the test trials of the S group, PC test for both F and S groups was defined as PC over the last few trials of *free play*. **Several variations of these histograms are provided** (use the navigation controls below the figure to access them and see the [notes](#important_notes){: .animated} explanation).

{% include caption.html 
    obj='figure' 
    num=page.entrynum
    ext='1'
    label='PC and learning for each task split by group<br>(left = PC training, middle = PC test, right = dPC)' %}
{% include carousel2.html thumbnails='true' path='img/train_test_delta_hists_10_10_a.svg::img/train_test_delta_hists_15_15_b.svg::img/train_test_delta_hists_10_10_c.svg::img/train_test_delta_hists_7_7_d.svg' %}

<a href='#important_notes'></a>
#### Notes
- Figures **a**, **b**, and **c** vary in the number of trials over which a particular PC score was calculated and the number of bins used.
- **(a)** PC training = percent correct over 15 trials of training; PC test = percent correct over the last 15 trials of free exploration; number of bins = 11.
    - As [Figure 1.1](#f-1-1){: .animated}, both PC training and PC test appear bimodal. As discussed earlier, this bimodality is an artifact of arbitrary binning.
- **(b)** is the same as **(a)**, but the number of bins is 16.
    - Here, bimodality is much more subtle and doesn't quite show in the combined histograms. 
- **(c)** PC training = percent correct over the last 10 trials of training; PC test = percent correct over the last 10 trials of free exploration; number of bins = 11.
    - The reasoning behind ignoring the first 5 trials of both training and test stages is to reduce the noise attributable to the those trials. During training, the subjects were completely unfamiliar with the tasks and those who started their familiarization with erroneous responses would get a lower overall PC training score. In contrast, those who started with correct responses, would have an inflated PC score. The same reasoning may be applied to the testing stage (the last 15 free play trials), with a proviso that subjects, instead of being unfamiliar with the tasks, forgot the relevant feature(s). 
    - But note that, by looking at any number of trials of free play as a test measure, we cannot guarantee that these trials were played after a sufficient amount of time has been spent on the task, (some PC test scores might come from the only N trials a subject had played the task, and these trials might be scattered all over the free play period). However, compared to PC training distributions, PC test scores seem reliably higher, as also seen by the histograms of delta PC.
- **(d)** PC training = percent correct over the last 7 trials of training; PC test = percent correct over the last 7 trials of free exploration; number of bins = 8.
    
If we let [Figure 2.1](#f-2-1){: .animated}(c) guide the splitting of subjects by performance and learning outcome, it seems reasonable to perform a median split by performance, since no obvious bimodality is present. As for the learning outcome, we see that most of the people showed little to no improvement (between 0 and .2). There is a smaller group of people who did improve quite considerably (.2 or more), and an even smaller group that did worse. It is worth noting that when PC training and PC test are calculated over the same number of trials, the dPC score can be interpreted straightforwardly as the difference between the number of correct trials between test and training stages. Thus, the inclusive region between -.2 and .2 can be viewed as a "no change" region, and the regions above and below, as "improvement" and "deterioration' regions, respectively. Thus, it would make sense to divide people by learning outcome into 3 groups, but splitting more simply at .2 is also meaningful, as we could differentiate between "improvers" and "non-improvers".

### 2.2. Group-level performance during free-play

In light of [Figure 2.1](#f-2-1){: .animated}, [Figure 2.2](#f-2-2){: .animated} seems interesting. The dPC distributions of F and S groups are virtually identical, yet we see and gradual increase of PC during free play in the F group, and a no such increase in the S group, which is the one that aims to maximize learning. I think this is in line with an idea that this group learns faster, and then, by virtue of being instructed to maximize learning sticks to the R task, thereby keeping PC over the entire free-play period constant (as suggested <a href='{{site.baseurl}}/content/analyses/other/index.html#13-what-might-the-learning-outcome-be-related-to' class='animated'>here</a>). 

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='2'
    label='Average PC during free-play split by group' %}
[![alt]({{site.baseurl}}/img_compressed/smoothed_pc.svg)]({{site.baseurl}}/img/smoothed_pc.svg)

#### Notes
- The lines represent probability of a correct response as a function of trial number. The raw (and very noisy) probabilities curves are shown in opaque colors, and their liberally smoothed counterparts (rolling average over 10 trials) appear in more solid colors. The between-group difference can be seen even from the unsmoothed data curves.
