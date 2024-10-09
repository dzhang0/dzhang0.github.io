---
classes: wide
title: Active sensing for localization
tags: ml sensing wireless LSTM
header:
    teaser: "assets/posts/activesensing/2ris_position_active.gif"
excerpt_separator: <!--more-->
---
A no-math intuitive account of my journal publication in TWC 2024.
<!--more-->

Active sensing is a sequential sensing strategy that enables fast and high-precision sensing, specifically for mm-wave wireless applications. 
When we talk about active sensing, we mean that the set of sensing vectors is sequentially designed as a function of existing measurements. As more measurements become available, the sensing vector becomes better and better at sensing the target. 

In this journal, I designed an active sensing strategy for uplink localization with multiple reconfigurable intelligent surfaces (RISs). The user with an unknown position repeatedly transmits pilot symbols to the base station (BS). The BS adaptively adjusts its beamforming vector and the RISs based on existing pilots received.  

<div style="text-align:center"><img src="/assets/posts/activesensing/2ris_position_active.gif" style="width:20em"/></div>


Below is an illustration of the beam pattern produced by the active sensing strategy. After six (or any number of) measurements, the two sensing devices (RISs 🔵) can produce a very narrow beam focus toward the target (in red 🔴). Notice that there is constructive interference around the user and deconstructive interference outside of the proximity of the user, which enables very accurate positioning. This beampattern is otherwise difficult to achieve with conventional approaches. 

<div style="text-align:center"><img src="/assets/posts/activesensing/2ris_position_active.gif" style="width:20em"/></div>

## Active sensing via learning

It is difficult to design an adaptive sequence of beams using conventional methods. That involves rigorous math which maps pilots to a posterior distribution which is later used to determine the Cramer-rao bound, then optimizing the bound to determine the best beam (this is covered in the journal). 

In this work, we show that machine learning can do better because it can better model the complex wireless environment and machine learning can jointly design the sequence of sensing vector to achieve the optimal performance. 




## Summary

Quantifying representational similarity is fundamental to neuroscience & ML. Shape metrics offer a principled way to compare responses of many networks. We develop shape metrics for stochastic neural responses. This method is highly scalable and can be used to compare thousands of networks simultaneously. These analyses can provide direct insight into how representational geometry relates experimental variables of interest (e.g. behaviour, task performance, etc.).

