---
layout: post
title: "CauseMap: Published in PeerJ!"
description: "Our paper for examining causality from time series data is now online."
category: projects
tags: software
comments: true
---

It's my pleasure to announce that our paper, ["_CauseMap: fast inference of causality from complex time series_"](https://peerj.com/articles/824/) is now available online at [PeerJ](https://peerj.com/). For those who aren't familiar with PeerJ (it's a relatively new journal), definitely give it a look. This submission was hands-down the best publishing experience I've had. A couple points that were particularly refreshing: 1.) we got back responses within weeks instead of months. 2.) our reviewers provided helpful, civil feedback clearly geared toward improving the manuscript, and 3.) we were able to submit the manuscript through a sleek, modern web interface that significantly cut down the administrative overhead of the submission process. So many thanks to PeerJ for an excellent open access publishing experience :)

A bit about the paper: we present the first open source implementation of Convergent Cross Mapping (CCM), an algorithm developed by the [Sugihara group](http://scrippsscholars.ucsd.edu/gsugihara) at UCSD. This is method is useful for robust causal inference from time series data. Unlike popular tools such as time-lagged regression, instrumental variables, etc.; CCM explicitly accounts for high-dimensional system dynamics encoded within time series data. In fact it's these details that allow us to establish causality, even in the presence of confounding and interdependent non-linearity. For more details, feel free to check out the [paper](https://peerj.com/articles/824/) or [cyrusmaher.github.io/CauseMap.jl](cyrusmaher.github.io/CauseMap.jl)!

<figure align="center">
    <img src="{{ site.url }}/images/Causemap_fit.jpg"  WIDTH="500" BORDER="0" ALIGN="middle" > 
    <figcaption align="left"><i>Figure 1: An example visualization from CauseMap using abundances of Paramecium aurelia and Didinium nasutum (a predator-prey system). (A) For optimal parameter values, the convergence of the cross-map correlation with library size. (B–C). The dependence of the maximum cross-map correlation on assumed dimensionality (measured by E) and the time lag of the causal effect (measured by τp). Note that the second maximum at τp = 5 corresponds to the principal frequency of the P. aurelia and D. nasutum time series, as determined by Fourier transform analysis.</i></figcaption>
</figure>