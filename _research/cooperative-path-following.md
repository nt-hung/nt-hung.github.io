---
title: "Cooperative path following of multiple autonomous vehicles"
layout: single-portfolio
excerpt: "<img src='/images/research/CPF_illustration.png' alt=''>"
collection: research
order_number: 60
---

Cooperative path following (CPF) is a typical formation control problem, defined as steering a group of autonomous
vehicles along given spatial paths while holding a desired inter-vehicle formation pattern.
A simple example of CPF is illustrated in Fig.1.1. In this setup, each vehicle is dedicated
with a local task, i.e. converge to and follow its preassigned path (the straight line), while
cooperating with other vehicles via a wireless communication network to position itself
relative to other vehicles such that all vehicles are aligned in a side-by-sided formation
in time.

![](/images/research/CPF_illustration.png)


## Contribution

We proposed a solution that involves in decoupling the original CPF problem into two sub-problems: i) single
path following of input-constrained vehicles and ii) coordination of an input-constrained multi-agent system (MAS). The first is solved by adopting a sampled-data model predictive control (MPC) scheme, whereas the latter is tackled using a novel distributed control law with an (ETC) mechanism. The proposed strategy yields a closed-loop CPF system
that is input-to-state-stable (ISS) with respect to the system’s state (consisting of the
path following error of all vehicles and their coordination errors) and the system’s input,
which includes triggering thresholds for ETC communications and communication delays.

## Related publications

- Nguyen T. Hung, Antonio M. Pascoal, Tor A. Johansen, "Cooperative path following of constrained autonomous vehicles with model predictive control and event-triggered communications",
International Journal of Robust Nonlinear Control, 2020; 30: 2644– 2670. [download](https://onlinelibrary.wiley.com/doi/abs/10.1002/rnc.4896), [code]()
- Francisco C. Rego, Nguyen T. Hung, Colin N. Jones, Antonio
	   M. Pascoal and A. Pedro Aguiar, Chapter 8: "Cooperative Path-
	   Following Control with Logic-Based Communications: Theory and
	   Practice", Navigation and Control of Autonomous Marine Vehicles,
	   IET books, 2019. [download](https://digital-library.theiet.org/content/books/10.1049/pbtr011e_ch8), [code](). 
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->