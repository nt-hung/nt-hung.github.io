---
title: 'The history of optimal control - Part I'
date: 2025-1-01
permalink: /posts/2020/11/proof-euler/
excerpt_separator: <!--more-->
usemath: true
tags:
  - Scientific story
  - Mathematic
---

As we know Euler’s fomula is very ubiquitous in mathematics, physics, and engineering. The formula is as follows:

$$e^{i\theta}=\cos(\theta)+i\sin(\theta)$$

I never though how to prove this formula until seeing a simple proof with an interesting story behind in the book “Linear Algebra and Its Applications”, Gilbert Strang. One day there was a letter came to MIT from a prisoner in New York, asking if Euler’s formula was true? It is really astonishing. Three key functions of mathematics come together in such a graceful way.

<!--more-->

The proof of the Euler’s formulas, in fact is quite simple using the Taylor series.

$$ e^{i\theta} = 1 + i\theta + \frac{(i\theta)^2}{2!} + \frac{(i\theta)^3}{3!} + \frac{(i\theta)^4}{4!} + \frac{(i\theta)^5}{5!} ... $$ 

Because $i^2=-1$, 

Real$( e^{i\theta})= 1 - \frac{\theta^2}{2!} + \frac{\theta^4}{4!} + ... = \cos(\theta)   $, and 

Img$( e^{i\theta})=  i(\theta - \frac{\theta^3}{3!} + \frac{\theta^5}{5!} + ...) = i\sin(\theta).$

Thus the formula is correct. 

