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

However, it is difficult to train a single neural network to learn this mapping. The overall architecture looks daunting but it basically means that 

<div style="text-align:center"><img src="/assets/posts/scheduling/framework_v17_page-0001.jpg" style="width:50em"/></div>




