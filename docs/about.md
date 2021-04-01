---
layout: page
title: "About Me"
permaklink: about
---

# Hello World!

I am currently seeking a job (!) and meanwhile hoping to develop sme data projects on video game: historic e-sport championship data and characteristics of players in battle-royale games. 

I earned my PhD from Columbia University in the City of New York, where I developed an analytical framework with Professor Qiang Du on using a classical numerical technique of linear multistep methods (LMMs) for the data-driven discovery of dynamics and a universal machine learning problem. I'll go into those briefly.

## PhD Research Breakdown
For my PhD research, as noted I had two major topics: LMMs for discovery of dynamics and a universal machine learning problem.

### LMMs for Discovery of Dynamics

LMMs are used for solving ordinary differential equations (ode) numerically. The ''Euler step'' is perhaps the most well-known example, where the definitely of a derivative is used explicitly to write the LMM. In the movie *Hidden Figures*, the breakthrough that the amazing and tenacious Katherine Johnson had that saved the day was using an Euler step!

Recently, researchers have been using them to *learn* parts of the differential equation, rather than to solve them. Used in this new way, well-behaved methods performed strangley, so my advisor Professor Du and I sought to get to the bottom of it. Our analytical framework, based on the tried-and-true classical, decades-old framework, helped partially explain the behavior. Some nice methods for the forward problem of solving an ode were not good for the inverse problem of learning the ode. Interestingly, not ALL methods had that issue! 

You can check out more at [our publishing](https://epubs.siam.org/doi/abs/10.1137/19M130981X) on *SIAM Journal on Numerical Analysis* and the [pre-print](https://arxiv.org/abs/1912.12728) on the arXiv.

### Universal Machine Learning Problem

Machine learning (ML) is a lot of things, but one thing is certain: Given some measure of correctness, we seek to [predict, describe, or prescribe](https://blog.dominodatalab.com/data-science-at-the-new-york-times/) given some data. To do so, we learn at least one function given a so-called loss function, the latter of which tells us quantitatively the measure of correctness. 

In this component of my thesis, we devleop a universal learning framework and problem from which these different types of machine learning problem (prediction, description, and prescription) can be realized. Ultimately, we situate ML problems in optimization theory and discuss the relationship between three common ML paradigms of supervised, unsupervised, and reinforcement learning using the framework.

## Current Endeavors

For now, I'm trying to write a story about video games using historic data I've pulled and a kaggle dataset on the battle royale game. I'll be posting progress soon!






