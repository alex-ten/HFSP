---
layout: default
title: Materials
---
{% include toc.html %}

## 1. Monster Task 

Inria hosts its own version of the task, made AMT-agnostic: <a href='http://pstk.bordeaux.inria.fr/6' class='animated'>http://pstk.bordeaux.inria.fr/6</a>

The only valid code at the moment is INRIA. Corresponding code is in the standalone branch of our repo.

### 1.1. Task setup
The goal of the active sampling task was up to the participants, although some of them received an explicit instruction to learn as much as possible about it. For them at least, the goal was to figure through trial and error out what food different monsters presented on the screen liked to eat. There were 4 different monster families.Monsters in each family varied along different dimensions. For example, within a family, an individual monster could have a unique height, or width, or both, as in [Figure 1](#f-1){: .animated} below:

{% include caption.html 
    obj='figure' 
    num=1
    label='Examples of 1D and 2D monster families' %}
<table class='imagegrid'>
    <tr>
        <td style='white-space: nowrap'>(a) One variable dimension </td>
        <td><a href="{{site.baseurl}}/img/fam1d.png"><img src="{{site.baseurl}}/img/fam1d.png" alt="allocation_variance_clean" /></a></td>
    </tr>
    <tr>
        <td style='white-space: nowrap'>(b) Two variable dimensions </td>
        <td><a href="{{site.baseurl}}/img/fam2d.png"><img src="{{site.baseurl}}/img/fam2d.png" alt="choice_bias_clean" /></a></td>
    </tr>
</table>
    
The monsters can vary along 1 or 2 dimensions. These dimensions determined what food preferences monsters had. For example, in a family of blue bears, the short ones preferred pancakes while the tall ones preferred waffles. Participants would then need to determine, based on a monster’s features, what food they preferred.

### 1.2. Monster families and their food preferences
Each monster family was randomly assigned how many dimensions determined their food preferences. In the [~~data file~~]() (not on the website yet), these are referred to as categories. These categories are:
- category1D: the monster family only varies along one dimension, and this dimension determines a food preference
- categoryIgnore1D: the monster family varies along 2 dimensions, but only one dimension determines a food preference
- category2D: the monster family varies along 2 dimensions, and both dimensions determine a food preference
- categoryRandom: the monster family varies along 2 dimensions, but food preferences are random

As mentioned, there are also always 4 monster families. In the data file, they are named as:
* Bear
* Bunny
* GreenMonster
* Squid

There are also 4 pairs of food options:
* pancakes/waffles
* bananas/oranges
* broccoli/carrot
* grilled_cheese/tacos

The food pairings were randomly assigned to each monster family.

During the task, one monster would be presented on the screen, and two food choices would appear as buttons. The participant would then need to select one food option as a guess if that was the food the monster preferred. They would then receive feedback if they were correct or not. Over time, they could then learn a monster’s preference (except for the random condition monster family, as described below).

### 1.3. Task Versions
There were 3 versions of this task run on Mechanical Turk:
* Strategic (2 conditions)
* Free Play with Familiarization (2 conditions)
* Free Play Only

**Strategic** version included 3 stages during the task. These are the (1) train, (2) free, and (3) test states. During the train state, participants are forced to guess food preferences for a certain number of monsters in each monster family to familiarize the participant to them. During the free state, the participant can then choose which monster family they want to practice with, and can free switch between monster families. The test state then follows, which is the same format as the train state (but the monsters/families are not in the same order).

**Free Play with Familiarization** version included 2 states: (1) train and (2) free. These are the same as what is described above.

**Free Play Only** contained just the (1) free state.
As indicated, the Strategic and Free Play with Familiarization Phase also each have 2 conditions. This condition only changed the instructions given to the participant. One condition explicitly stated that one of the monster families may have unpredictable food preferences. The other condition omitted this sentence.

### 1.4. Instrictions
The general instructions presented to all groups were as follows:

> In this game, you will see 4 monster families:

> In each family there are several individuals, and the appearance of an individual might predict what food they like to eat. 

> When you interact with a monster family, different individuals will be presented to you. For each individual, two food items will be displayed, and you can click on the one you think it prefers. You will receive feedback whether your guess was correct or not. 

> On each trial, you can freely select to see another monster from the same family, or to switch to a different family. 

> Some families have food preferences that you can discover based on their appearance. 

> `[i+ or i- instruction]`

> `[F or S instruction]`

> Please, ensure your volume is at a comfortable listening level.

Depending on group and condition, the general instructions were amended as follows. The informed (i+) condition emphasized the possibility of a potentially unlearnable tasks:

> However, there might also be a monster family with unpredictable preferences.

The freely exploring (F) group were presented with the description of the 3 phases of the experiment:

> The task is organized in 3 phases:

> Introduction: We will give 15 trials per family to introduce them to you. This will take approximately 3 minutes.

> Free choice: During the next 250 trials, you will be able to freely select which monster family to interact with. You can switch at any moment from one family to another and as many times as you want. This will take approximately 10 minutes.

> Questionnaire: There will be a post-task questionnaire at the end. This will also take approximately 3 minutes to complete.

> (You may play longer if you would like, but we will not pay any additional bonus for the extra time you spend on the task. If you do continue to play over the required 250 trials, please be aware of how much time is left remaining to submit the HIT.)

While the strategic group received an explicit instruction to maximize learning (appearing twice) and the additional description of the test phase:

> In the main section of the task, we ask you to play for 250 trials and try to maximize your learning **about all the 4 families**. 

> The task will be organized in 4 phases:

> Introduction: We will give 15 trials per family to introduce them to you. This will take approximately 3 minutes.

> Free Choice: You will have 250 trials in which you will freely select the monster family to interact with. You can switch at any moment from one family to another and as many times as you want. Try to maximize your learning for all 4 families during this period. This will take approximately 10 minutes.

> Testing: We will briefly test how well you learned to predict the food preferences within each family. This will take approximately 3 minutes.

> Questionnaire: There will be a post-task questionnaire at the end. This will also take approximately 3 minutes to complete.

> Please, ensure your volume is at a comfortable listening level.

A complete content of instructions for all groups and conditions can be found <a href='{{site.base_url}}/pdfs/instructions.pdf' target='_blank' class='animated'>here</a>.

## 2. Self-reports
Participants were first asked one question at the end of training and a series of questions at the end of testing or free play. All questions were answered on 10-point Likert scale.

Post-training question:
- *Future-learn-0*. Before continuing, please rate each monster family based on how much you think you can learn about its food preferences during the rest of the task:
> [1] Definitely Cannot Learn More -- [10] Definitely Can Learn More

Final questions:

1. *Interested*. Rate each monster family based on how much you were interested in discovering what they preferred eating:
> [1] Less Interested -- [10] More Interested 

2. *Complex*. Rate each monster family based on how complex you thought they were: 
> [1] Less Complex -- [10] More Complex 

3. *Time*. Rate each monster family based on how much time you spent on them: 
> [1] Less Time -- [10] More Time 

4. *Progress*. Rate each monster family based on how much progress you felt you made for learning their food preferences:
> [1] Less Progress -- [10] More Progress 

5. *Rule*. Rate each monster family based on how likely you think it had a rule for food preferences:
> [1] Definitely No Rule -- [10] Definitely a Rule 

6. *Future-learn-1*. Rate each monster family based on how much more you think you could learn if you had more time to play with it:
> [1] Definitely Could Not Learn More -- [10] Definitely Could Learn More 

## 3. Raw data files
The data was sorted based on the version that was run (Strategic, Free with Familiarization, Free Only). There are 2 data files contained in each folder (data, extra_data).
Column legend for the `data` file:
- **participant:assignmentId**: this is a unique identifier for each participant
- **condition**: this indicates whether or not a participant was told that there is a monster family that has unpredictable food preferences, as described under Task Versions. (0 = text is shown to participant; 1 = text is NOT shown to participant)
- **stage**: this indicates what state the participant was in for this trial, as described under Task Versions (train, free, or test)
- **trial**: the overall trial number for the task
- **blockTrial**: the trial number for the current monster family (the trial number resets every time a new monster family is either presented or selected by the participant)
- **trialStartTime**: the start time of the trial in ms, in relation to when the participant started the task
- **monster**: which monster image was presented. Each monster family can vary in 2 dimensions, so the 2 numbers following the name of the monster family indicate the specific features the monster had. There is a maximum of 6 variations for each dimension. For example, Bear_3_6 indicates that the monster presented was part of the Bear family, had a level 3 width, and a level 6 height. For the monster family that varied over only 1 dimension, the second number would stay constant.
- **family**: which monster family the monster presented for the trial belongs to
- **category**: what category type was used for determining the dimensions used for food preferences, as described under Monster Families and Food (category1D, categoryIgnore1D, category2D, categoryRandom)
- **preferredFood**: what this particular monster’s food preference is (i.e. what was the correct response for this trial)
- **choice**: what food option the participant selected for this trial
- **correct**: whether the participant was correct or not
- **rt**: the response time of the participant after the monster and the food options were presented

Column legend for the `extra_data` files:
- **participant:assignmentId**: this is a unique identifier for each participant
- **condition**: this indicates whether or not a participant was told that there is a monster family that has unpredictable food preferences, as described under Task Versions. (0 = text is shown to participant; 1 = text is NOT shown to participant)
- The remaining columns in the `extra_data` file correspond to the questions described in [self-reports](#2-self-reports){: .animated}. Each question has a shortened question ID that is listed in the square brackets next to the question text (future-learn-0, interested, complex, time, progress, rule, future-learn-1). All question responses are on a 10-point Likert scale.
    - In the data columns, each question ID is also followed by which family the question was asking about. For example, interested-Bear would contain the responses given to the [interested] question for the Bear family.