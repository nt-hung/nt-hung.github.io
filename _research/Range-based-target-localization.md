---
title: "Cooperative simultaneous target localization and pursuit"
layout: single-portfolio
excerpt: "<img src='/images/research/navigation.png' alt=''>"
collection: research
order_number: 10
---

<!-- Range-based navigation is defined for an agent, for example, a scuba-diver or
an autonomous underwater vehicle (AUV) to find its own state (position, and possibly with velocity and acceleration) using
the information measured by the agent itself and the ranges to a known single or multiple
beacons. If an agent like AUV can measure its velocity vector (using
Doppler Velocity Log (DVL)), then only the position of the AUV needs to be determined.
In other situations, velocity and acceleration need to be determined as well. -->

Cooperative simultaneous target localization and pursuit (cooperative SLAP) is a problem defined for one or
multiple autonomous robots/vehicles acting as mobile sensors to find the state of unknown moving target using some sort of information
measured about the target. The state of the target typically includes the target’s position, velocity, and
even possibly acceleration, depending on the model of the target adopted. The information about the target can be ranges, bearings, or both, depending on sensing capability of the robots.  

![](/images/research/navigation.png =300x250)

## Contributions

We propose a cooperative distributed control and estimation strategy to solve the cooperative SLAP problem using only range measurements from the robots to the target. 

## Videos - an example using an autonomous vehicle to localize and pursue a target simultaneously using the MPC scheme in [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/S0921889020304486) 

<iframe width="560" height="315" src="https://www.youtube.com/embed/5fzQ0DSwtUQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Videos - an example using three robots to localize and pursue a moving target [[Paper]](/files/pdf/research/IEEE_TCST_preprint.pdf) 

<iframe width="560" height="315" src="https://www.youtube.com/embed/J94cYoKW4y0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Videos - an example using 2 robots to localize and pursue a target [[Paper]](/files/pdf/research/IEEE_TCST_preprint.pdf)

Experimental setup:
- Robots: Medusa marine robots, developed by IST Lisbon.
- Software components: Linux, ROS (C++, Python).
- Navigation: GPS, DLV, AHRS.
- Vehicle communication network: wifi (UDP protocol).  
- Information to the target: ranges, measured by acoustic modems, provided by Evologics company.

<iframe width="560" height="315" src="https://www.youtube.com/embed/voMQCpJ-chs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Related publications
- Nguyen T. Hung, Francisco Rego, Antonio M. Pascoal, "Cooperative distributed estimation and control of multiple autonomous vehicles for range-based underwater target localization and pursuit", conditionally accepted with minor revision at IEEE Transactions on Control System and Technology.\
[[Preprint]](/files/pdf/research/IEEE_TCST_preprint.pdf). 
- Nguyen T. Hung, N. Crasta, David Moreno-Salinas, António M. Pascoal, Tor A. Johansen,
"Range-based target localization and pursuit with autonomous vehicles: An approach using
posterior CRLB and model predictive control", Robotics and Autonomous Systems, 2020. \
[[Preprint]](/files/pdf/research/RAS2020_preprint.pdf) - [[Web]](https://www.sciencedirect.com/science/article/abs/pii/S0921889020304486) - [[Code]]() - [[Videos]](https://www.youtube.com/watch?v=jXkh-W7ksyM).
- Nguyen T. Hung, Antonio M. Pascoal, "Range-based navigation and target localization: observability analysis and guidelines for motion planning", IFAC2020, to appear. \
[[Preprint]](https://www.dropbox.com/s/90u31vku7omcrbc/IFAC2020.pdf?dl=0) - [[Web]]().
