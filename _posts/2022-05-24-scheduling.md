---
classes: wide
title: Learning based scheduling
tags: ml gnn scheduling
header:
    teaser: "assets/posts/scheduling/JSTSP_cover.jpg"
excerpt_separator: <!--more-->
---
A no-math intuitive account of my journal publication in JSTSP 2022. 
<!--more-->

Journal paper: <a href="https://arxiv.org/abs/2205.06396">Arxiv</a>, <a href="https://ieeexplore.ieee.org/abstract/document/9783100">IEEE</a>

In this journal, I designed a learning-based approach for user scheduling problems in reconfigurable intelligent surface (RIS) assisted multiuser downlink. Here, the key question is that the base station (BS) is equipped with M antennas, which can serve at most M users simultaneously over the same resource block, if the total number of users in the network K is greater than M, how should the BS optimally schedule a subset of users at each timeslot in conjunction with the optimal RIS configuration and the BS beamforming to achieve high network throughput while ensuring fairness across the users?

## Learn to schedule

The idea is to use a single neural network to map received pilots from all the users to schedule, RIS pattern and BS beamforming vector simultaneously as follows (this figure is selected as the coverpage of this JSTSP issue)
<div style="text-align:center"><img src="/assets/posts/scheduling/JSTSP_cover.jpg" style="width:25em"/></div> 

However, it is difficult to train a single neural network to learn this mapping. 



<div style="text-align:center"><img src="/assets/posts/scheduling/JSTSP_cover.jpg" style="width:25em"/></div>

Active sensing is a sequential sensing strategy that enables fast and high-precision sensing, specifically for mm-wave wireless applications. 
When we talk about active sensing, we mean that the set of sensing vectors is sequentially designed as a function of existing measurements. As more measurements become available, the sensing vector becomes better and better at sensing the target. 

In this journal, I designed an active sensing strategy for uplink localization with multiple reconfigurable intelligent surfaces (RISs). The user with an unknown position repeatedly transmits pilot symbols to the base station (BS). The BS adaptively adjusts its beamforming vector and the RISs based on existing pilots received. The system diagram is as follows:

<div style="text-align:center"><img src="/assets/posts/activesensing/sys_model.jpg" style="width:20em"/></div>

Below is an illustration of the beam pattern produced by the active sensing strategy. After six (or any number of) measurements, the two sensing devices (RISs 🔵) can produce a very narrow beam focus toward the target (in red 🔴). Notice that there is constructive interference around the user and deconstructive interference outside of the proximity of the user, which enables very accurate positioning. This beampattern is otherwise difficult to achieve with conventional approaches. 



