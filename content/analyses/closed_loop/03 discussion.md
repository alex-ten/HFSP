---
title: Discussion
category: closed_loop
doctype: entry
entrynum: 3
---

### 3.1. Information gaps

One tentative explanation is that the "strategic" instructions uncovered knowledge gaps different from those that would be otherwise perceived (i.e. in the F group). To make any sense of this proposition, it is important to establish what exactly knowledge gaps are and how they are detected. Let's try to apply Golman and Loewenstein's [G&L's] ({% include citation.html link='pdfs/Golman2016.pdf' cite='Golman & Loewenstein, 2016' %}) framework to our monster task. G&L propose a general model of informational utility, in which attention can drives an agent into a contemplative state, which encompass a set of activated questions, each associated with a set of possible answers (hypotheses). Associated with these answers are beliefs that contribute to the answer's utility through valence and clarity. Answers can be evaluated according to these belief qualities and guide an individual towards favorable outcomes.

Since answers in our study (e.g. "fat and short bears prefer tacos") were not supposed to have any material value or emotional valence, we can ignore the corresponding terms in G&L's general-form utility function and focus on information *clarity*, which corresponds to the entropy of a discrete probability distribution over a set of conceived answers and defines information gaps "... which are represented as activated questions lacking known correct answers ..." (G&L, 2016, p. 4).

Now let's try to take the framework seriously for a moment and imagine that our task happened in a world that it portrays. Consider an overly simplified example first: a single trial on which a participant tries to guess the food preference of a given monster. If this happens in the very beginning of the game, the question might be very specific, e.g.:

> "*What does this monster (M1) prefer?*"

"This monster" refers to whatever the participant perceives in the current stimulus. Accordingly, the set of possible answers is very simple and concise. It can be represented a discrete probability distribution, with 2 outcomes (i.e. a Bernoulli distribution with 1-parameter PMF):

> 1) M1 prefers A

> 2) M1 prefers B

Assume that any prior knowledge one's has does not influence her behavior in the current context. Thus, before any action is taken, each outcome is equiprobable, so the entropy is maximal. The answer becomes more clear as the entropy decreases. Regardless of the learning mechanism, a guess is required in order to receive feedback and tune the associated probability mapping (we may call it supervision). What does depend on the learning mechanism here is how strongly supervision influences representations and how stable these representations are. Note that the simple question we imagined above suggests that the knowledge about a monster family as a whole might be represented as a set of exemplars, each with its own probability mapping to a preferred food choice. If we let memory be imperfect, learned probability mappings can become more uncertain overtime unless the exemplar with a prediction / feedback pair is not encountered repeatedly. Together, gradual learning from the environment and the volatility of representations may explain a tendency to stick to the current family. The volatility of representations need not be incompatible with switching, if we let it subside with repeated supervision (as in Ebbinghaus's characterization of the <a href='https://en.wikipedia.org/wiki/Forgetting_curve' class='animated' target='_blank'>forgetting curve</a>).

So far so good. Suppose the next trial brings a new exemplar, so a new question is added to the cognitive state and immediately attended to:

> "*What does this monster (M2) prefer?*"

Although this question is different, it has the same set of possible answers. At this point, the details of learning machinery become relevant again. One the one hand, the probability distribution of answers to this new question may have maximal entropy, due to equal probability of the possible answers, just like on the first trial. However, if the learning mechanism allows the agent to use past experience for new inferences (e.g. do Bayesian inference), the entropy of this new question may be lower than maximum. Particularly, if the second monster is very similar to the previous one, the participant may be inclined to produce a specific answer depending on the previous trial's feedback. If indeed the mechanism is such, it is not clear why and how the questions should be represented separately. Instead, what the participant might be trying to figure out is how food preferences and monster appearance are related. We can test whether responses to the next monster are random or depend on the previous experiences. (Both scenarios may also be true. We could imagine a Karmiloff-Smithean-like process of representational redescription where separate mappings are learned first and then redescribed into a new format which allows an explicit representation of a food preference rule.)

If Bayesian inference does occur, then participants should be able to represent individual monsters as specific configurations of general features. The exact verbal form of a question added to their cognitive states is not easy to capture. But the precise verbal form of the question is not important. What is important is the set of possible answers (i.e. the hypothesis space) and the specifics of probability mappings of these answers. 

### 3.2. Bayesian inference

#### 3.2.1. Information gap as conditional entropy

The Bayesian inference framework provides an idealized computational description of predicting food preferences from the current statistical knowledge about a given monster family (see {% include citation.html link='pdfs/Tenenbaum1999.pdf' cite='Tenenbaum, 1999'%}, {% include citation.html link='pdfs/Tenenbaum2000.pdf' cite='2000'%}, {% include citation.html link='pdfs/McClelland2013.pdf' cite='McClelland, 2013'%}). We can imagine a learner that is trying to compute the posterior conditional probability of food preference given currently observed features from a handful of statistical quantities:

$$ p(h \vert \textbf{d}) = \frac{p(h)p(\textbf{d} \vert h)}{p(\textbf{d})} $$

Here, $$h$$ is the hypothesis that food A is preferred, $$\textbf{d}$$ is a multidimensional vector of observed monster features (a representation of a monster). Computing the posterior normally requires knowing the following statistical quantities:

- Prior probability (or base rate) of preference for food A, $$p(h)$$
- The likelihood, $$p(\textbf{d} \vert h)$$ that quantifies the how many times the current monster (represented as a collection of features) preferred food A (i.e. the positive examples of food A lovers)
- Unconditional probability of $$\textbf{d}$$ (also called evidence). In general it can be written as $$\sum_{h \in \mathcal{H}} p(h)p(\textbf{d} \vert h)$$. In our specific case with 2 complementary hypotheses, it is simply $$p(h)p(\textbf{d} \vert h) + (1-p(h))p(\textbf{d} \vert h^C)$$, where $$h^C$$ is the only complement of hypothesis $$h$$. 

Just how the mind might compute these quantities is not clear. However, assuming for now that they are known or somehow estimated, we can always compute the entropy -- and in this case, the *conditional entropy*, $$H(h \vert D)$$ -- and interpret it as the *average* amount of uncertainty in predicting food choices from some general set of features, $$D$$. This amounts to knowing the food preferences in a family (or forming a belief about answering a somewhat vague question "What do monsters in this family like to eat?"):

$$ H(h \vert D) = \sum_{\textbf{d} \in \mathcal{D}} p(\textbf{d}) H(h \vert D = \textbf{d}) $$

where $$\mathcal{D}$$ is the multidimensional space of observable features from which individual monsters are sampled, and $$H(h \vert D = \textbf{d})$$ is the uncertainty about the food preference of a particular monster, $$\textbf{d}$$, evaluated as follows:

$$ H(h \vert D=\textbf{d}) =  - \sum_{h \in \mathcal{H}} p(h \vert \textbf{d}) \log p(h \vert \textbf{d}) $$

The posterior conditional probability distribution is quite different from the simple one-parameter Bernoulli PMF. Participants may have to keep track of a number of different parameters. Moreover, the full feature set, $$\mathcal{D}$$ is unknown a priori. Since a lot of information required to compute the precise uncertainty of the probability distribution associated with the question in mind is so illusive, participants may have to either estimate (perhaps using behavioral heuristics) or assume it from the limited experience that they get, much like scientists and statisticians have to estimate unobservable parameters from available data or resort to specific assumptions about them. On the other hand, if subjective certainty about a problem domain is estimated through experience-based statistical values, then active sampling behavior should be predictable, provided that uncertainty minimization is the primary motive. 

#### 3.2.2. A model of Bayesian concept learning

How is the posterior distribution maintained throughout the learning experience? Luckily others have proposed some relevant concept-learning Bayesian models that are able to generalize based on little supervision and can incorporate inter-example similarity. The model description below is based on Johsua Tenenbaum's early work on human concept learning and the derivative [tutorial]('{{site.baseurl}}/pdfs/Murphy2006.pdf'){:.animated} by Kevin Murphy.

Suppose stores a set of $$N$$ positive examples $$X = \{x_1, ..., x_N\}$$ of some category. It is important to assume that the learner does not hold any specific beliefs about the origin of these examples (i.e. thinks they were encountered by chance). We would like to know the probability that some current monster $$y$$ belongs to the category of certain food lovers $$C$$, given the set of observations past $$X$$. In other words, we want to compute the *generalization function*:

$$ p(y \in C \vert X) = \sum_{r \in \mathcal{D}}p(y \in C \vert r)p(r \vert X)$$

where $$r$$ is a region of feature space $$\mathcal{D}$$, and $$p(r \vert X)$$ is the so called *posterior belief state*. This generalization function defines the *posterior predictive distribution* by marginalizing out particular regions $$r$$. Note that $$\sum_{r \in \mathcal{D}}p(r \vert X)$$ is normalized (equal to 1). Note also that the existence of a "rule" implies that $$p(y \in C \vert r) = 1$$ if a new monster $$y$$ lies inside the region $$r$$, that is, if $$y$$ is consistent with $$r$$ (and $$p(y \in C) = 0$$ otherwise). We can simplify it further by ignoring regions of the feature space that are inconsistent with the current observation $$y$$:

$$ p(y \in C \vert X) = \sum_{r \in \mathcal{D_y}}p(r \vert X)$$

where $$\mathcal{D_y}$$ contains all regions of $$\mathcal{d}$$ consistent with $$y$$. The term $$p(r \vert X)$$ is the posterior probability distribution of a rule (or a region) given the set of positive observations. We can compute these computed by applying the Bayes rule:

$$ p(r \vert X) = \frac{p(r)p(X \vert r)}{p(X)} $$

Note that although we are using the same old Bayes rule, we are not directly computing the conditional probability of a hypothesis (about a food preference) given currently observed features, like in the example opening this section. Instead we are computing the conditional probability that the observed features ($$y$$) correspond to category $$C$$ given a set of previously observed positive examples. This probability corresponds to the expectation over consistent hypotheses where weighting is done by the conditional probabilities of various possible rules, given positive observations. Accordingly, the terms prior, likelihood, and evidence are associated with specific terms relating to regions of the feature space.

The computation of the likelihood term $$p(X \vert r)$$ is greatly simplified by assuming that positive examples of a certain rule are sampled randomly and independently from region of feature space $$r$$. Than means that the size of that region alone determines the likelihood of any particular example being sampled from it (since sampling is uniform). Therefore:

$$p(X \vert r) = \frac{1}{|r|^n}$$

where $$\vert r \vert$$ denotes the size of region $$r$$, and $$n$$ is the number of positive examples seen. This expression implies that as the number of positive examples grows, more specific (smaller) regions of the feature space become more likely. For instance, if a participant sees three monsters with somewhat large eyes, the region of feature space corresponding to larger eyes (of some region size $$ \vert r_{large} \vert $$) is more likely than a larger region that includes all eye-sizes ($$ \vert r_{all} \vert  >  \vert r_{large} \vert $$). Although the true feature space in our experiment was in general rather small and discrete, we should assume that it was perceived as continuous (as generally, morphological features of living things are continuous). Assuming continuous features allows for the dynamic construction and adjustment of plausible feature space regions, because the participant who sees two extreme positive examples (e.g. eye size 3 and 6) they can infer that features of intermediate values exist and may lie within the same region as the observed positive examples.


The origin of prior is interesting. Intuitively, it seems like some regions should be more likely than others. For example, after observing several monsters that vary along a single dimension, regions 