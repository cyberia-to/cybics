---
tags: cybics, mathematics, article, draft, research
alias: Hoeffding's inequality, Hoeffding inequality, Hoeffding bound, Hoeffding
crystal-type: pattern
crystal-domain: cybics
crystal-size: enzyme
---

a concentration bound: the average of bounded independent random variables stays close to its true mean with a probability that grows exponentially in the number of samples

let $X_1, \dots, X_k$ be independent with $X_i \in [a_i, b_i]$, and let $\bar X = \tfrac1k \sum_i X_i$ have mean $\mu = \mathbb{E}[\bar X]$. then for any $t > 0$,

$$\Pr\big[\,|\bar X - \mu| \ge t\,\big] \;\le\; 2\exp\!\left(-\frac{2k^2 t^2}{\sum_i (b_i - a_i)^2}\right).$$

for variables on a common range $X_i \in [0,1]$ this is $\Pr[\,|\bar X - \mu| \ge t\,] \le 2\,e^{-2k t^2}$.

---

## what it gives

the bound turns a qualitative promise — the sample average converges to the mean — into a quantitative, finite-sample rate. it is the sharp form of the law of large numbers: where that says "converges eventually," Hoeffding says the deviation probability decays like $e^{-2kt^2}$, exponentially in the sample count $k$.

inverted, it is a sample-complexity rule. estimating $\mu$ within error $\varepsilon$ at confidence $1-\delta$ takes

$$k \;\ge\; \frac{1}{2\varepsilon^2}\,\ln\frac{2}{\delta}$$

samples — the error shrinks as $1/\sqrt{k}$, and tighter confidence costs only a logarithm.

---

## why bounded, why independent

two assumptions carry the result. boundedness ($X_i \in [a_i,b_i]$) removes any need to know the variance: the range alone controls the tail. independence lets fluctuations cancel rather than reinforce — under correlation the bound weakens, which is why an estimator built on Hoeffding must draw its samples independently.

---

## in settlement mining

cyber's [[reward specification]] estimates each neuron's [[Shapley value]] by Monte-Carlo over random orderings, and Hoeffding is the convergence guarantee. each published sample is an independent, bounded draw of the same marginal, so the swarm average concentrates on the true share at rate $e^{-2kt^2}$: more mining means more independent samples means an exponentially tighter attribution estimate, with no aggregator and no added trust. the same bound sizes the difficulty schedule — how many samples a contested cluster needs before its settlement is final to a chosen precision.

the lottery supplies both assumptions the bound requires: beacon-seeded orderings give the independence, and the bounded range of a single marginal gives the boundedness.

---

## relation to the wider family

Hoeffding is the entry point to concentration of measure — the principle that a function of many independent variables is nearly constant. sharper cousins use more information: Bernstein and Chernoff bounds tighten it when the variance is small, and McDiarmid extends it to any function that changes little when one input changes. all share the exponential-in-$k$ shape that makes sampling estimators trustworthy.

---

see [[Shapley value]] for the quantity a swarm estimates, [[reward specification]] for settlement mining, and [[KL divergence]] and [[entropy]] for the information measures concentration bounds sit beside.
