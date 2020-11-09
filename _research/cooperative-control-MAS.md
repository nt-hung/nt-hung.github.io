---
title: "Consensus/synchronization of nonlinear multi agent system"
layout: single-portfolio
excerpt: "<img src='/images/research/ternary.png' alt=''>"
collection: research
order_number: 10
---
Suppose that we have a network of multi nonlinear agent system, where each agent dynamics are described a model, given by 
$$
\bf{dot{x}}_i=A\bfx_i + {\bf f}({\bf x}_i,t) + B {\bf u}_i 
$$
for all $i \in {1,...,N}$.
Furthermore, the communications among the agents are constrained by a network topology that can be modeled by a directed graph.
The consensus/synchronization problem is defined for fiding a distributed control strategy for ${\bf u}_i$ s.t. asymtotically, the trajectories of all agents are synchronized (reach consensus), i.e. ${\bf x}_i(t)={\bf x}_j(t)$ for all $i,j \in {1,...N}$ as $t\to \infinity$. 

## Contribution
My work proposed a solution to the above problem with an event-triggered communications (ETC) mechanism. In con-
trast to previous work reported in the literature, we consider the case where the dynamics of each agent contain linear and Lipschitz nonlinear terms and the underlying communication graph is directed. The strategy proposed has two important
properties: i) it achieves practical consensus, that is, the synchronization error that
measures the disagreement among the agents’ states converges to a ball centered at
the origin, with a radius that can be made arbitrarily small and ii) the minimum of
the inter-event times for each agent is lower bounded by a strictly positive number,
hence Zeno behavior is excluded. Furthermore, it affords system designers adequate
tools to trade off the frequency of communications among agents against the level
of performance achieved in MAS consensus/synchronization. The results obtained
are illustrated via numerical simulations.

## Related publications

[Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research}