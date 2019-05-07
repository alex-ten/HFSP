---
layout: default

---

{% include toc.html %}

## 1. The setup
The participants played multiple trials of a game, where the objective of each trial was to correctly classify a given stimulus. This was implemented as a guessing game in which participants could guess what various monsters liked to eat. The active sampling component of the game allowed participants to switch between different monster families whenever they wanted (i.e. to choose a stimulus type). 

### 1.1. Stimuli
There were 4 different monster families for participants to choose from. Monsters in each family had a similar appearance, but individuals within families could vary along up to 2 dimensions:

<table class='imagegrid' style='width: 100%; height:auto; display: block; margin: 0 auto;'>
    <tr>
        <td style='white-space: nowrap'> One variable dimension </td>
        <td><a href="{{site.baseurl}}/img/fam1d.png"><img src="{{site.baseurl}}/img/fam1d.png" alt="allocation_variance_clean"  style='width: 50%; height:auto; display: block; margin: 0 auto;/'/></a></td>
    </tr>
    <tr>
        <td style='white-space: nowrap'> Two variable dimensions </td>
        <td><a href="{{site.baseurl}}/img/fam2d.png"><img src="{{site.baseurl}}/img/fam2d.png" alt="choice_bias_clean" style='width: 50%; height:auto; display: block; margin: 0 auto;/'/></a></td>
    </tr>
</table>

### 1.2. Task description
For each participant, each monster family was uniquely mapped onto one of the 4 task types. The task types determined the difficulty of learning about predictability of individual food preferences within a family. The task types were:

- **1D**: individual monsters varied along a single dimension which dimension determined their food preferences
- **I1D**: individual monsters varied along 2 dimensions, but only one determined food preferences, so that the other one could be **ignored** 
- **2D**: individual monsters varied along 2 dimensions, both of which determined food preferences
- **R**: individual monsters varied along 2 dimensions, but food preferences were **random** across individuals

Food preferences of individual monsters in nonrandom tasks were constant within each participant. Thus, by trial and error, participants could eventually learn to consistently predict the monsters' food preferences, or learn that food preferences were unpredictable. Different tasks were intended to have different levels of difficulty of learning. Task 1D was expected to be the simplest one to learn, followed by I1D, followed by 2D. Food preferences in the R task could not be learned by design, making it impossible. Note, however, that if the goal is to learn anything about a family, rather than to learn to successfully predict food preferences of individuals, the task becomes learnable, since it is possible to learn that food preferences are random (although extremely hard). 

### 1.3. Experimental treatments
Each participant was randomly assigned to one of 2 different instruction groups (Free (F) or Strategic (S)) and one of 2 different explicitness conditions (Uninformed (i-) or Informed (i+)). Thus, 4 independent groups were formed.

We tried to not impose or suggest any external goal to participants assigned to the F group. They were simply asked to play the game and were informed about what the game involved. For the strategic group, the goal was explicitly set by instructing the participants to maximize learning about each monster family.

In each group, we either emphasized to the participants about the possibility of unpredictable food preferences in one of the families or simply stated that families could have food preferences based on appearance.

#### 1.3.1 Instrictions
The general instructions presented to all groups were as follows:

<p style = 'border:2px; border-style:solid; border-color:#000000; padding: 1em; width: 75%; height:auto; display: block; margin: 0 auto;'>
    In this game, you will see 4 monster families:<br/><br/>

    In each family there are several individuals, and the appearance of an individual might predict what food they like to eat.<br/><br/>

    When you interact with a monster family, different individuals will be presented to you. For each individual, two food items will be displayed, and you can click on the one you think it prefers. You will receive feedback whether your guess was correct or not.<br/><br/>

    On each trial, you can freely select to see another monster from the same family, or to switch to a different family.<br/><br/>

    Some families have food preferences that you can discover based on their appearance.<br/><br/>

    <code>[i+ or i- instruction]</code><br/><br/>

    <code>[F or S instruction]</code><br/><br/>

    Please, ensure your volume is at a comfortable listening level.
</p>

Depending on group and condition, the general instructions were amended as follows. The informed (i+) condition emphasized the possibility of a potentially unlearnable tasks:

<p style = 'border:2px; border-style:solid; border-color:#000000; padding: 1em; width: 75%; height:auto; display: block; margin: 0 auto;'>
    However, there might also be a monster family with unpredictable preferences.
</p>

The freely exploring (F) group were presented with the description of the 3 phases of the experiment:

<p style = 'border:2px; border-style:solid; border-color:#000000; padding: 1em; width: 75%; height:auto; display: block; margin: 0 auto;'>
    The task is organized in 3 phases:

    Introduction: We will give 15 trials per family to introduce them to you. This will take approximately 3 minutes.<br/><br/>

    Free choice: During the next 250 trials, you will be able to freely select which monster family to interact with. You can switch at any moment from one family to another and as many times as you want. This will take approximately 10 minutes.<br/><br/>

    Questionnaire: There will be a post-task questionnaire at the end. This will also take approximately 3 minutes to complete.<br/><br/>

    (You may play longer if you would like, but we will not pay any additional bonus for the extra time you spend on the task. If you do continue to play over the required 250 trials, please be aware of how much time is left remaining to submit the HIT.)
</p>

While the strategic (S) group received an explicit instruction to maximize learning (appearing twice) and the additional description of the test phase:

<p style = 'border:2px; border-style:solid; border-color:#000000; padding: 1em; width: 75%; height:auto; display: block; margin: 0 auto;'>
    In the main section of the task, we ask you to play for 250 trials and try to maximize your learning **about all the 4 families**. 

    The task will be organized in 4 phases:<br/><br/>

    Introduction: We will give 15 trials per family to introduce them to you. This will take approximately 3 minutes.<br/><br/>

    Free Choice: You will have 250 trials in which you will freely select the monster family to interact with. You can switch at any moment from one family to another and as many times as you want. Try to maximize your learning for all 4 families during this period. This will take approximately 10 minutes.<br/><br/>

    Testing: We will briefly test how well you learned to predict the food preferences within each family. This will take approximately 3 minutes.<br/><br/>

    Questionnaire: There will be a post-task questionnaire at the end. This will also take approximately 3 minutes to complete.<br/><br/>

    Please, ensure your volume is at a comfortable listening level.
</p>

A complete content of instructions for all groups and conditions can be found <a href='{{site.base_url}}/pdfs/instructions.pdf' target='_blank' class='animated'>here</a>.

### 1.5. Self-reports
Participants were first asked one question at the end of training and a series of questions at the end of testing or free play. All questions were answered on 10-point scale:

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

### 1.6. Sanity checks

It appears that our manipulation of task difficulty produced the anticipated effect (see [Figure 1a](#f-1a){:.animated}). A 3-way mixed ANOVA for examining the independent effects of group and condtion, as well as the within-subjects effect of task difficulty (`tid`) only revealed the main effect of the latter variable, and no interactions ($$F(3,975) = 140.477, p<.001$$):

<pre class='codeblock'>
    Call: summary(aov(pc_first ~ grp*cnd*tid + Error(sid), data=data))

    Error: sid
               Df Sum Sq Mean Sq F value Pr(>F)
    grp         1  0.065 0.06498   2.224  0.137
    cnd         1  0.000 0.00003   0.001  0.973
    grp:cnd     1  0.052 0.05197   1.779  0.183
    Residuals 325  9.495 0.02922               

    Error: Within
                 Df Sum Sq Mean Sq F value Pr(>F)    
    tid           3  9.754   3.251 140.477 <2e-16 ***
    grp:tid       3  0.113   0.038   1.630  0.181    
    cnd:tid       3  0.128   0.043   1.839  0.138    
    grp:cnd:tid   3  0.037   0.012   0.540  0.655    
    Residuals   975 22.566   0.023                   
    ---
    Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
</pre>

<div class='caption' id='f-1a'>
    <em>
        <b>Figure 1a. Hit counts across subjects for each task split by group and conditions</b>
    </em>
</div>
<a href='{{site.baseurl}}/final/f1a.svg'><img src='{{site.baseurl}}/final/f1a.svg' alt='histogram of pc' style='width: 40%; height:auto; display: block; margin: 0 auto;/'></a>

To examine further, whether our experimental manipulations worked as intended, we need to have a closer look at other sources of within-subject variability in performance that coincided with task difficulty: monster type and order of presentation. Within each subject, each task difficulty was uniquely associated with one out of four monster types (Bear, Bunny, GreenMonster, and Squid). Although some parameters of variability, like the number of variable dimensions and the conditional predictability of food preferences varied *across* monster types (each could be 1D, I1D, 2D, or R), specific monster features varied *within* monster types, which could result in varying difficulty among them. Moreover, there could be order effects on performance as well, for example increasing performance on later tasks due to increasing familiarity with the general procedure, increasing attention, etc. Note that if any of these potential random effects is significant, they are likely to interact with the experimental manipulation (e.g. an easy task should be even easier with an easy monster type, and easier still at the right time).

Both random effects of monster type ($$F(3,738) = 27.065, p < .001$$) and task order ($$F(3,738) = 2.995, p < .001 $$) were significant:

<table>
    <tr>
        <td>
            <div class='caption' id='f-1b'>
                <em>
                    <b>Figure 1b. Effects of monster type on performance</b>
                </em>
            </div>
            <a href='{{site.baseurl}}/final/f1b.svg'><img src='{{site.baseurl}}/final/f1b.svg' alt='histogram of pc' style='width: 100%; height:auto; display: block; margin: 0 auto;/'></a>
        </td>
        <td>
            <div class='caption' id='f-1c'>
                <em>
                    <b>Figure 1c. Effects of task order on performance</b>
                </em>
            </div>
            <a href='{{site.baseurl}}/final/f1c.svg'><img src='{{site.baseurl}}/final/f1c.svg' alt='histogram of pc' style='width: 100%; height:auto; display: block; margin: 0 auto;/'></a>
        </td>
    </tr>
</table>

For whatever reason, the Bunny monster type was harder to learn, and more so in simpler tasks. The same was true, but to a lesser extent for the Green Monster type. Apparently, the simplest 1D task with Bunny monsters was harder than the I1D task with Bear and Squid monsters; and the I1D task was just as hard for Bunnies as 2D was for other monster types. This might have to do with the saliency of feature variability. In any case, this effect was not planned or anticipated. However, assignment of task order and mapping of monster types were both randomized for each participant, so across groups, conditions, and difficulty levels, the distributions of monster types and task order was uniform.

## 2. Judgments of learnability

## 3. Effect of explicit instruction to learn

## 4. Post-play questions

## 5. Individual variation