---
title: "Consensus/synchronization of nonlinear multi agent system"
layout: single-portfolio
excerpt: "<img src='/images/research/digraph.png' alt=''>"
collection: research
order_number: 100
---
Suppose that we have a network of multiple nonlinear agent system, where each agent's dynamics are described by a model, given by 

$$\Sigma_i : {\bf \dot{x}}_i=A{\bf x}_i + {\bf f}({\bf x}_i,t) + B {\bf u}_i $$

for all $i \in \{1,...,N\}$. Here, ${\bf x}_i \in \mathbb{R}^{n}$ is the state and ${\bf u}_i \in \mathbb{R}^{m} $ is the input of agent $i$; the function ${\bf f}({\bf x},t)$ is assumed to be Lipchizt in ${\bf x}$. 
Furthermore, the communications among the agents are constrained by a network topology that can be modeled by a directed graph (as shown in the figure).

The consensus/synchronization problem is defined as finding a distributed control strategy for ${\bf u}_i({\bf x}_i,{\bf x}_j)$, where $j$ is in the set of the neighbors of $i$ s.t. asymtotically, the trajectories of all agents are synchronized (reach consensus), i.e. ${\bf x}_i(t)={\bf x}_j(t)$ for all $i,j \in \{1,...N\}$ as $t\to \infty$. 

This type of consensus/synchronization problem appears in many applications involved in [cooperative control of multiple autonomous vehicle](https://nt-hung.github.io/research/cooperative-path-following/), [synchronization of robot's network](https://www.tandfonline.com/doi/abs/10.1080/00207179.2020.1849806?journalCode=tcon20), sensor network, and modeling of biology systems.    

![](/images/research/digraph.png)


## Contribution
We proposed a solution to the consensus/synchronization problem with an event-triggered communications (ETC) mechanism. In contrast to previous work reported in the literature, we consider the case where the dynamics of each agent contain linear and Lipschitz nonlinear terms and the underlying communication graph is directed. The strategy proposed has two important
properties: i) it achieves practical consensus, that is, the synchronization error that
measures the disagreement among the agents’ states converges to a ball centered at
the origin, with a radius that can be made arbitrarily small and ii) the minimum of
the inter-event times for each agent is lower bounded by a strictly positive number,
hence Zeno behavior is excluded. Furthermore, it affords system designers adequate
tools to trade off the frequency of communications among agents against the level
of performance achieved in MAS consensus/synchronization. 

## Related publications

-  Nguyen T. Hung, Antonio M. Pascoal, "Consensus/synchronization of networked nonlinear
multiple agent systems with event-triggered communications", International Journal of Control, 2020. \
[[Preprint]](/files/pdf/research/IJC2020_preprint.pdf) - [[Web]](https://www.tandfonline.com/doi/full/10.1080/00207179.2020.1849806) - [[Code]](https://github.com/hungrepo/consensus-synchronization-of-MAS/tree/master/IJC2020).
- Nguyen T. Hung, F. C. Rego and A. M. Pascoal, "Event-Triggered Communications for the Synchronization of Nonlinear Multi Agent Systems on Weight-Balanced Digraphs," 2019 18th European Control Conference (ECC), Naples, Italy, 2019. \
[[Preprint]]() - [[Web]](https://doi.org/10.23919/ECC.2019.8796277) - [[Code]]().

<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->