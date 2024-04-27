---
title: "Competition of Mechanisms: Tracing How Language Models Handle Facts and Counterfactuals"
weight: 5
# aliases: ["/first"]
author: ["Francesco Ortu*", "Zhijing Jin*", "Diego Doimo", "Mrinmaya Sachan", "Alberto Cazzaniga", "Bernhard Schölkopf" ] # multiple authors
# author: ["Me", "You"] # multiple authors
date: 2024-02-20T19:33:35-08:00
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
canonicalURL: "/publications/"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: true
searchHidden: true
ShowReadingTime: false
ShowBreadCrumbs: false
ShowPostNavLinks: false
ShowWordCount: false
ShowRssButtonInSectionTermList: false
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
---
[![paper](https://img.shields.io/badge/ArXiv-2402.11655-red?style=for-the-badge&logo=arxiv)](https://arxiv.org/abs/2402.11655)[![github](https://img.shields.io/badge/GitHub-black?style=for-the-badge&logo=github)](https://github.com/francescortu/comp-mech)


![figure](../figure/fig1.png)
## Abstract
Interpretability research aims to bridge the gap between the empirical success and our scientific understanding of the inner workings of large language models (LLMs). However, most existing research in this area focused on analyzing a single mechanism, such as how models copy or recall factual knowledge. In this work, we propose the formulation of competition of mechanisms, which instead of individual mechanisms focuses on the interplay of multiple mechanisms, and traces how one of them becomes dominant in the final prediction. We uncover how and where the competition of mechanisms happens within LLMs using two interpretability methods, logit inspection and attention modification. Our findings show traces of the mechanisms and their competition across various model components, and reveal attention positions that effectively control the strength of certain mechanisms. Our code and data are at this https URL.



