---
tags: cybics, mathematics, article, draft, research
alias: Prelec's theorem, Prelec theorem, Prelec, truth-serum theorem, BTS theorem, information-score theorem
crystal-type: pattern
crystal-domain: cybics
crystal-size: enzyme
---
# Prelec's theorem

honest reporting can be made the equilibrium of an elicitation game even when the true answer never arrives — the result that lets a protocol score honesty on claims no outcome will ever settle

Daniel Prelec (Science, 2004) introduced the [[Bayesian Truth Serum]], a mechanism for eliciting honest answers to questions whose truth is subjective, private, or never observed. its guarantee is the theorem: truthful reporting is a Bayes–Nash equilibrium of the elicitation game, scored with no reference to any outcome.

## the setup

each agent reports two things about a question:

- a first-order answer — its own belief or private signal $p_\nu$;
- a meta-prediction — its estimate of how the population will answer, $m_\nu$.

the mechanism scores every agent against the aggregate of all others. it consults no ground truth, because in this regime there is none to consult.

## the score

an agent's score sums an information term and a prediction term:

$$s_\nu = \underbrace{D_{KL}(p_\nu \,\|\, \bar m_{-\nu}) - D_{KL}(p_\nu \,\|\, \bar p_{-\nu})}_{\text{information gain}} - \underbrace{D_{KL}(\bar p_{-\nu} \,\|\, m_\nu)}_{\text{prediction accuracy}}.$$

the information term rewards answers that are surprisingly common — chosen more often than the population collectively predicted. (Prelec's original writes this as a log-ratio of an answer's actual to predicted frequency.) the prediction term rewards an accurate meta-prediction of how others answer.

## the theorem

truthful reporting of both the signal and the meta-prediction is a Bayes–Nash equilibrium, and as the population grows it is the equilibrium of highest expected score for every agent.

the intuition: a genuine private signal shifts an agent's own belief away from the crowd's prediction more than it shifts that prediction itself, so private information scores positive on the information term. the only way to forecast the meta-prediction well is to report it honestly. copying the consensus drives the information term to zero — a copyist contributes what the crowd already expected.

## why it matters

[[proper scoring rules]] reward calibrated belief against a realized outcome. Prelec's theorem extends honest elicitation to the case with no outcome at all — the [[wisdom of the crowds]] made incentive-compatible. that is the regime of a knowledge graph, where the truth of a [[cyberlink]] is rarely settled by an external event.

in cyber the theorem is load-bearing. the [[valence]] a [[neuron]] attaches to a [[cyberlink]] is its meta-prediction; the [[Bayesian Truth Serum]] score accumulates into [[karma]]; and because honesty is the equilibrium, [[karma]] measures genuine private signal rather than conformity. the [[reward specification]] leans on this to separate signal from copying before [[Shapley value|Shapley]] attribution divides any reward.

## limits

the guarantee holds against unilateral deviation. a coordinated cartel that mutually predicts its own answers can still farm the score — the open collusion frontier the [[reward specification]] addresses by other means: [[karma]] non-transferability, stake-weighting, and [[identity]] cost.

---

see [[Bayesian Truth Serum]] for the mechanism as cyber deploys it, [[proper scoring rules]] for the outcome-based cousin, [[wisdom of the crowds]] for the aggregation principle it secures, and [[reward specification]] for its role in rewards.
