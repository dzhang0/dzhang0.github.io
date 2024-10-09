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

Active sensing is a sequential sensing strategy that enables fast and high-precision sensing, specifically for mm-wave wireless applications. 
When we talk about active sensing, we mean that the set of sensing vectors is sequentially designed as a function of existing measurements. As more measurements become available, the sensing vector becomes better and better at sensing the target. 

In this journal, I designed an active sensing strategy for uplink localization with multiple reconfigurable intelligent surfaces (RISs). The user with an unknown position repeatedly transmits pilot symbols to the base station (BS). The BS adaptively adjusts its beamforming vector and the RISs based on existing pilots received. The system diagram is as follows:

<div style="text-align:center"><img src="/assets/posts/activesensing/sys_model.jpg" style="width:20em"/></div>

Below is an illustration of the beam pattern produced by the active sensing strategy. After six (or any number of) measurements, the two sensing devices (RISs 🔵) can produce a very narrow beam focus toward the target (in red 🔴). Notice that there is constructive interference around the user and deconstructive interference outside of the proximity of the user, which enables very accurate positioning. This beampattern is otherwise difficult to achieve with conventional approaches. 

<div style="text-align:center"><img src="/assets/posts/scheduling/JSTSP_cover.jpg" style="width:50em"/></div>


## Active sensing via learning




## My project

I wrote up the results for a conference paper, which was accepted to IEEE Int'l Conference on Acoustics, Speech and Signal Processing 2023 (ICASSP) taking place in Rhodes Greece [(arXiv:2210.14308)](https://doi.org/10.48550/arXiv.2301.11955)!
Figure 1 of the paper (below) shows the architecture of the model.
I developed a method that serves as a (non)linear drop-in replacement for or _augmentations_ to existing transform coding modules in the AV1 codec.
The TL;DR is that a base autoencoder and hyperprior are trained on a large dataset of video frames prediction residuals.
To allow the model to operate at different bit rates, we can train auxiliary parameters (gain modulations; pink) to control the rate-dependent output scale at each layer.
In the paper, we show the model can be trained end-to-end, and that we can augment the DCT with learned gain modulations (quantization matrices), and hyperpriors to significantly improvement performance at a fraction of the cost of a full-blown nonlinear transform (e.g. a deep net).

![architecture](/assets/posts/scheduling/JSTSP_cover.jpg)
