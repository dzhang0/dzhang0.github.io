---
classes: wide
title: Active sensing for localization
tags: ml wasserstein probability geometry
header:
    teaser: "assets/posts/activesensing/2ris_position_active.gif"
excerpt_separator: <!--more-->
---
A no-math intuitive account of my journal publication in TWC 2024.
<!--more-->

Active sensing is a sequential sensing strategy that enables fast and high-precision sensing, specifically for mm-wave wireless applications. 
When we talk about active sensing, we mean that the set of sensing vectors is sequentially designed as a function of existing measurements. As more measurements become available, the sensing vector becomes better and better at sensing the target. 

For example in this journal, I designed an active sensing strategy for multiple reconfigurable intelligent surfaces (RISs), such that after six (or any number of) measurements, the two sensing devices (RISs) can produce a very narrow beam focus toward the target (in red). Notice that there is constructive interference around the user and deconstructive interference outside of the proximity of the user, which enables very accurate positioning. This beampattern is otherwise difficult to achieve with conventional approaches. 

<div style="text-align:center"><img src="/assets/posts/activesensing/2ris_position_active.gif" style="width:20em"/></div>


## Summary

Quantifying representational similarity is fundamental to neuroscience & ML. Shape metrics offer a principled way to compare responses of many networks. We develop shape metrics for stochastic neural responses. This method is highly scalable and can be used to compare thousands of networks simultaneously. These analyses can provide direct insight into how representational geometry relates experimental variables of interest (e.g. behaviour, task performance, etc.).

