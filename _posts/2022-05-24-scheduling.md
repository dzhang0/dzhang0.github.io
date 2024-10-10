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

Journal paper: <a href="https://arxiv.org/abs/2205.06396">Arxiv</a>, <a href="https://ieeexplore.ieee.org/abstract/document/9783100">IEEE</a>. I presented a <a href="https://ieeexplore.ieee.org/abstract/document/9746441">conference</a> version of this paper at ICASSP in Singapore. 

In this journal, I designed a learning-based approach for user scheduling problems in reconfigurable intelligent surface (RIS) assisted multiuser downlink. Here, the key question is that the base station (BS) is equipped with M antennas, which can serve at most M users simultaneously over the same resource block, if the total number of users in the network K is greater than M, how should the BS optimally schedule a subset of users at each timeslot in conjunction with the optimal RIS configuration and the BS beamforming to achieve high network throughput while ensuring fairness across the users?

## Learn to schedule

The idea is to use a single neural network to map received pilots from all the users to schedule, RIS pattern and BS beamforming vector simultaneously as follows (btw this figure is selected as the cover for this JSTSP issue)

<div style="text-align:center"><img src="/assets/posts/scheduling/JSTSP_cover.jpg" style="width:25em"/></div> 

However, it is difficult to train a single neural network to learn this mapping. We make three key observations and design a three-stage framework to successively determine the schedule, RIS pattern and beamforming vector: 1) scheduling and beamforming require different precision of channel knowledge, 2) scheduling decision is implicit in the designed beamformers for all users and 3)channel estimation with fixed scheduling and RIS configuration is much easier. 

Based on the above observations, we design the following framework. The overall architecture looks daunting but it basically divides the joint scheduling and beamforming problem into three stages. The first stage uses a GNN takes very short received pilots and the user weights from all potential users as inputs in order to make the scheduling decisions. We then use a second GNN to design the RIS configuration for the scheduled users in a second stage. The second GNN works on a smaller set of users, so it can take longer pilot sequences as a feature. Finally, we propose a beamformer fine-tuning stage as the third stage to refine the beamformers using the weighted minimum mean square error (WMMSE) algorithm based on
the explicitly estimated channels for additional performance gain.
<div style="text-align:center"><img src="/assets/posts/scheduling/framework_v17_page-0001.jpg" style="width:50em"/></div>




