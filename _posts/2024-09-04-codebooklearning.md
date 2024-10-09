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

I presented this paper at SPAWC in Lucca, Italy (poster at the bottom). This publication further investigates the codebook design problem for active sensing (background on active sensing can be found [here]({% post_url 2023-12-25-activesensing %}). 

In this paper, I design a beamforming codebook for a reconfigurable intelligent surface (RIS) based active sensing scheme for uplink localization, in which the mobile user sends a sequence of pilots to the base station (BS), and the RIS is adaptively configured by carefully choosing RIS codewords from a codebook in a sequential manner to progressively focus on the target.

Most existing codebook designs for RIS are not tailored for active sensing where the choice of next codeword depends on the measurement available so far, and are not designed to dynamically focus reflection toward the target. Moreover, most existing codeword selection methods rely on exhaustive search in beam training to identify the codeword with the highest signal-to-noise ratio (SNR), thus incurring substantial pilot overhead as the codebook scales.

Here, I propose a learning-based approach for codebook construction and codeword selection for active sensing. The proposed learning approach can locate a target in the service area by recursively selecting a sequence of codewords from the codebook as more measurements become available without exhaustive beam training. The codebook design and the codeword selection fuse key ideas from vector quantized-variational autoencoder (VQVAE) and long short-term memory (LSTM) network to learn respectively the discrete function space of the codebook and the temporal dependencies between measurements. 
<div style="text-align:center"><img src="/assets/posts/codebooklearning/nnarchitect_v3_page-0001.jpg" style="width:50em"/></div>


<div style="text-align:center"><img src="/assets/posts/codebooklearning/poster.jpg" style="width:50em"/></div>


