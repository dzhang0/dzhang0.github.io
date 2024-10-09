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

[![Open In Arxiv](https://arxiv.org/abs/2312.09002)](https://arxiv.org/abs/2312.09002)

Active sensing is a sequential sensing strategy that enables fast and high-precision sensing, specifically for mm-wave wireless applications. 
When we talk about active sensing, we mean that the set of sensing vectors is sequentially designed as a function of existing measurements. As more measurements become available, the sensing vector becomes better and better at sensing the target. 

In this journal, I designed an active sensing strategy for uplink localization with multiple reconfigurable intelligent surfaces (RISs). The user with an unknown position repeatedly transmits pilot symbols to the base station (BS). The BS adaptively adjusts its beamforming vector and the RISs based on existing pilots received. The system diagram is as follows:

<div style="text-align:center"><img src="/assets/posts/activesensing/sys_model.jpg" style="width:20em"/></div>

Below is an illustration of the beam pattern produced by the active sensing strategy. After six (or any number of) measurements, the two sensing devices (RISs 🔵) can produce a very narrow beam focus toward the target (in red 🔴). Notice that there is constructive interference around the user and deconstructive interference outside of the proximity of the user, which enables very accurate positioning. This beampattern is otherwise difficult to achieve with conventional approaches. 

<div style="text-align:center"><img src="/assets/posts/activesensing/2ris_position_active.gif" style="width:20em"/></div>


## Active sensing via learning

It is difficult to design an adaptive sequence of beams using conventional methods. That involves rigorous math which maps pilots to a posterior distribution which is later used to determine the Cramer-rao bound, then optimizing the bound to determine the best beam (this is covered in the journal). 

In this work, we show that machine learning can do better because it can better model the complex wireless environment and machine learning can jointly design the sequence of sensing vector to achieve the optimal performance. 

The neural network architecture is shown below. The idea is that an LSTM network can be used to process the temporal input (pilots). At each sensing stage, the LSTM cell receives a new measurement and maps the measurement (along with historical measurements) to the sensing vectors in the next stage. By concatenating a chain of LSTM cells, a sequence of sensing vectors can be designed. At the end of the sensing stage, an estimated position of the user is obtained based on all received pilots. 
<div style="text-align:center"><img src="/assets/posts/activesensing/lstm_cell.jpg" style="width:20em"/></div>





