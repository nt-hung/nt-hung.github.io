---
title: "Cooperative path following of multiple autonomous vehicles"
layout: single-portfolio
excerpt: "<img src='/images/research/circle_MPC1_mission.png' alt=''>"
collection: research
order_number: 60
---

Cooperative path following (CPF) is a typical formation control problem, defined as steering a group of autonomous
vehicles along given spatial paths while holding a desired inter-vehicle formation pattern.
An example of CPF is illustrated in the figure below. In this setup, each vehicle is dedicated
with a local task, i.e. converge to and follow its preassigned path, while
cooperating with other vehicles via a wireless communication network to position itself
relative to other vehicles such that all vehicles are aligned in a triangular formation
in time.

Although many path following methods have been developed over the last decade, the main challenge is how to handle constraints on the vehicles (e.g. limit on linear and angular velocities) and the constraints on the network topology and save the communication bandwidth.  

![](/images/research/CPF_illustration.png)


## Contribution

We proposed a solution that involves in decoupling the original CPF problem into two sub-problems: i) single
path following of input-constrained vehicles and ii) coordination of an input-constrained multi-agent system (MAS). The first is solved by adopting a sampled-data model predictive control (MPC) scheme, whereas the latter is tackled using a novel distributed control law with an event-triggered communication mechanism. The proposed strategy yields a closed-loop CPF system
that is input-to-state-stable (ISS) with respect to the system’s state (consisting of the
path following error of all vehicles and their coordination errors) and the system’s input,
which includes triggering thresholds for ETC communications and communication delays.

## Related publications

- Nguyen T. Hung, Antonio M. Pascoal, Tor A. Johansen, "Cooperative path following of constrained autonomous vehicles with model predictive control and event-triggered communications",
International Journal of Robust Nonlinear Control, 2020. \
[[Preprint]](/files/pdf/research/JRNC2020_preprint.pdf) - [[Web]](https://onlinelibrary.wiley.com/doi/abs/10.1002/rnc.4896) - [[Code]](https://github.com/hungrepo/cooperative-path-following/tree/master/CPF-MPC) - [[Videos]](https://www.youtube.com/watch?v=u_jDrVrIweY)
 
- Francisco C. Rego, Nguyen T. Hung, Colin N. Jones, Antonio
	   M. Pascoal and A. Pedro Aguiar, Chapter 8: "Cooperative Path-
	   Following Control with Logic-Based Communications: Theory and
	   Practice", Navigation and Control of Autonomous Marine Vehicles,
	   IET books, 2019. 
	   [[Preprint]](/files/pdf/research/IETbook_CPF_LBC2019_preprint.pdf) - [[Web]](https://digital-library.theiet.org/content/books/10.1049/pbtr011e_ch8) - [[Code]](https://github.com/hungrepo/cooperative-path-following/tree/master/CPF-Medusa) - [[Videos]](https://www.youtube.com/watch?v=YkpvfibSad0). 
- Nguyen T. Hung, Antonio Pascoal, "Cooperative Path
	   Following of Autonomous Vehicles with Model Predictive Control
	   and Event Triggered Communications", 6th IFAC Conference on
	   Nonlinear Model Predictive Control, Wisconsin, USA, 2018. [[Web]](https://www.sciencedirect.com/science/article/pii/S2405896318326855).  

- Francisco C. Rego, Nguyen T. Hung, Antonio Pascoal, "Cooperative Path
	   Following of Autonomous Marine Vehicles: Theory and
	   Experiments", IEEE OES Autonomous Underwater Vehicle, Porto, Portugal, 2018. \
	   [[Web]](https://doi.org/10.1109/AUV.2018.8729809)   

## Videos - an example of circular formation with CPF

<iframe width="560" height="315" src="https://www.youtube.com/embed/u_jDrVrIweY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->