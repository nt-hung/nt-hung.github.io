---
title: "Range-based navigation and target localization with autonomous vehicles"
layout: single-portfolio
excerpt: "<img src='/images/research/china_nl.png' alt=''>"
collection: research
order_number: 10
---

Typically, range-based navigation is defined for an agent, for example, a scuba-diver or
an AUV to find its own state (position, and possibly with velocity and acceleration) using
the information measured by the agent itself and the ranges to a known single or multiple
beacons. If an agent like AUV can measure its velocity vector (using
Doppler Velocity Log (DVL)), then only the position of the AUV needs to be determined.
In other situations, velocity and acceleration need to be determined as well.

Range-based target localization (or tracking), on the other hand, is defined for one or
multiple autonomous vehicles acting as mobile sensors to find the state of the target using only ranges from the vehicles to
the target. The state of the target typically includes the target’s position, velocity, and
possibly acceleration, depending on the model of the target adopted. From a theoretical standpoint, the navigation and localization are dual.   

Target pursuit is defined as a task of driving the vehicle(s) to converge to and stay in the vicinity of the
target. This task is crucial when the entities are in underwater environment where range
is only able to be measured in a relatively short distance.

## Contribution

We propose a systematic approach to solve the cooperative target localization and
pursuit using multiple autonomous vehicles. We identify a few sub-problems where we isolate
specific technical challenges that are present in Problem 2. By studying and solving each
sub-problem, we hope to gain insights into a general solution for the original problem.
Also, while addressing each sub-problem we expect to find as byproducts some interesting
results that stand on their own.

1. The first sub-problem involves in characterizing the motion of trackers under which
the target’s state is observable. Using tools from the function analysis, a set of
conditions are derived for different type of target maneuvers are derived, providing
guidelines for trackers’ motion planning [Hung and Pascoal, 2020a].

2. The second sub-problem is to find the optimal motions for the trackers such that
the range-information acquired for estimating the target state is maximal. Using
a Bayesian FIM, a tool from estimation theory, an optimal relative motion of the
trackers respect to the target is characterized. We also propose a receding horizon
planning, control, and estimation framework for the target localization and pursuit
problem where the constraints on the trackers’ inputs and the uncertainty of the
target are taken into account explicitly [Hung et al., 2020a].

3. After solving the aforementioned sub-problems, we come back the original problem. We exploit the knowledge about observability and the optimal trajectory for range-based target localization to plan desired motions for the trackers. We then propose a cooperative distributed estimation and control (DEC) strategy to address the constraints on the topology of the inter-tracker communication network. To this effect, a distributed extended Kalman filter (DEKF) is adopted for the cooperative estima-
tion of the target’s state, and a distributed consensus control strategy is proposed for the cooperative pursuit of the target. The later aims at driving all trackers to the vicinity of the target while holding an optimal target-trackers relative-geometry
that maximizes the range information for estimating the target’s state. To make the proposed DEC more efficient in terms of communications, we proposed event triggered mechanisms for the DEKF and for the distributed consensus control strategy where the communication among the tracker take place when found necessary. The stability of the complete closed-loop DEC system is rigorously proved.

## Related publications

- Nguyen T. Hung, N. Crasta, David Moreno-Salinas, António M. Pascoal, Tor A. Johansen,
"Range-based target localization and pursuit with autonomous vehicles: An approach using
posterior CRLB and model predictive control", Robotics and Autonomous Systems, Volume 132,
2020, 103608, ISSN 0921-8890. [download](https://www.sciencedirect.com/science/article/abs/pii/S0921889020304486), [code]().
- Nguyen T. Hung, Antonio M. Pascoal, "range-based navigation and target localization: observability analysis and guidelines for motion planning", IFAC2020, to appear. [download](https://www.dropbox.com/s/90u31vku7omcrbc/IFAC2020.pdf?dl=0).