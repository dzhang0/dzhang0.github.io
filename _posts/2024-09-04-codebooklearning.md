---
classes: wide
title: Codebook learning for active sensing
tags: ml codebook sensing wireless
header:
    teaser: "assets/posts/codebooklearning/nnarchitect_v3_page-0001.jpg"
excerpt_separator: <!--more-->
---
A no-math intuitive account of my conference publication in SPAWC 2024.
<!--more-->

Conference paper: <a href="https://ieeexplore.ieee.org/document/10694219">IEEE</a>

I presented this paper at SPAWC in Lucca, Italy. This publication further investigates the codebook design problem for active sensing (background on active sensing can be found [here]({% post_url 2023-12-25-activesensing %}). 

In this paper, 


In this journal, I designed an active sensing strategy for uplink localization with multiple reconfigurable intelligent surfaces (RISs). The user with an unknown position repeatedly transmits pilot symbols to the base station (BS). The BS adaptively adjusts its beamforming vector and the RISs based on existing pilots received. The system diagram is as follows:

<div style="text-align:center"><img src="/assets/posts/activesensing/sys_model.jpg" style="width:20em"/></div>

Below is an illustration of the beam pattern produced by the active sensing strategy. After six (or any number of) measurements, the two sensing devices (RISs 🔵) can produce a very narrow beam focus toward the target (in red 🔴). Notice that there is constructive interference around the user and deconstructive interference outside of the proximity of the user, which enables very accurate positioning. This beampattern is otherwise difficult to achieve with conventional approaches. 

<div style="text-align:center"><img src="/assets/posts/codebooklearning/poster.jpg" style="width:50em"/></div>


