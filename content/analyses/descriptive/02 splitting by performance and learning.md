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

### 2.2. Overall group-level performance during free play

In light of [Figure 2.1](#f-2-1){: .animated}, [Figure 2.2](#f-2-2){: .animated} seems interesting. The dPC distributions of F and S groups are virtually identical, yet we see and gradual increase of PC during free play in the F group, and a no such increase in the S group, which is the one that aims to maximize learning. I think this is in line with an idea that this group learns faster, and then, by virtue of being instructed to maximize learning sticks to the R task, thereby keeping PC over the entire free-play period constant (as suggested <a href='{{site.baseurl}}/content/analyses/other/index.html#13-what-might-the-learning-outcome-be-related-to' class='animated'>here</a>). 

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='2'
    label='Average PC during free-play split by group' %}
[![alt]({{site.baseurl}}/img_compressed/smoothed_pc.svg)]({{site.baseurl}}/img/smoothed_pc.svg)

#### Notes
- The lines represent probability of a correct response as a function of trial number. The raw (and very noisy) probabilities curves are shown in opaque colors, and their liberally smoothed counterparts (rolling average over 10 trials) appear in more solid colors. The between-group difference can be seen even from the unsmoothed data curves.

### 2.3. Group-level performance during free play split by task
Each panel in [Figure 2.3](#f-2-3){: .animated} shows group-level performance on the corresponding task along with the proportion of subjects from each group who played that task. 

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    ext='3'
    label='Average PC and %select during free-play split by group and task' %}
[![alt]({{site.baseurl}}/img_compressed/smoothed_pc_free2.svg)]({{site.baseurl}}/img/smoothed_pc_free2.svg)

#### Notes
- Task selection -- people in the S group challenge themselves more throughout the play phase:
    - Most strikingly, the %select curve of 1D of the S group is entirely below that of the F group, and vice versa in case of task R. That is, at no point during free play, were there more people from the S group playing task 1D than there were people from the F group playing it. Similarly, at no point were there less S people playing the R task than there were F people playing it.
    - The gaps between %select curves of the two groups from tasks 1D and R seem to be in phase. It seems like there are points of convergence immediately followed by divergence around trials 70 and 160. 
    - We can also see that more people in the F group played I1D compared to the S group (particularly between trials 70 and 210)
    - %select curves of the 2D task start diverging just before trial 150, after which, consistently, a higher proportion of people select this task in the S group than in the F group.
- PC:
    - Performance within each task appears to be grossly on the same level between the 2 groups.
    - For tasks 1D and I1D, subjects from the S group seem, rather consistently, to underperform compared to the F group. However, S group's absolute level of PC seems sufficiently high.
    - Since PC (%correct) is 50% for the R task and ~90% for the 1D task for both F and S, the S group has substantially lower PC overall during the play phase (shown in [Figure 2.2](#f-2-2){: .animated})
- I1D vs 2D task selection also differs by F/S, but only weakly:
    - S group select the 2D slightly more, and the I1D slightly less.than the F group
    - S group have slightly lower PC on the I1D task than the F group

