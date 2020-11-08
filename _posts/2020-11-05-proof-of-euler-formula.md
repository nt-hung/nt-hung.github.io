---
title: 'Proof of Eulers formula'
date: 2020-11-05
permalink: /posts/2020/11/proof-euler/
excerpt_separator: <!--more-->
usemath: true
tags:
  - General
  - Mathematic
---

As we know Euler’s fomula is very ubiquitous in mathematics, physics, and engineering. The fomula is as follows:

            $$e^{i\theta}=\cos(\theta)+i\sin(\theta)$$

In the book “Linear Algebra and Its Applications”, Prof. Gilbert Strang shared an interesting story about the proof of the formula that: One day there was a letter came to MIT from a prisoner in New York, asking if Euler’s fomula was true? It is really astonishing. Three key functions of mathematics come together in such a graceful way.

The proof of the Euler’s fomulas, in fact is quite simple using the Tayler series.

$ e^{i\theta} = 1 + i\theta + \frac{(i\theta)^2}{2!} + \frac{(i\theta)^3}{3!} + \frac{(i\theta)^4}{4!} $ 