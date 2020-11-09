---
title: "Hierarchical multiple testing"
layout: post
toc: false
comments: true
hide: false
search_exclude: true
categories: [r]
---

I was first introduced to the *multiple testing problem* when I conducted microarray gene expression analyses, quite some time ago. This concept was tricky for me to understand at first, and I have had many conversations with collaborators around p-values, adjusted p-values and false discovery rates since.

The book [Modern Statistics for Modern Biology](https://www.huber.embl.de/msmb/index.html) by Susan Holmes and Wolfgang Huber provides a great introduction to the topic in its chapter on [Testing](https://www.huber.embl.de/msmb/Chap-Testing.html), including a hat tip to XKCD's famous [Jelly bean cartoon](https://imgs.xkcd.com/comics/significant.png)

![Jelly beans](https://www.huber.embl.de/msmb/images/xkcdmulttest-newspapertitle.png)

While I was familiar with several standard methods to account for multiple testing among *independent* hypotheses, e.g. the approach proposed by [Benjamini and Hochberg](https://www.researchgate.net/publication/221995234_Controlling_The_False_Discovery_Rate_-_A_Practical_And_Powerful_Approach_To_Multiple_Testing), they book also points out methods for grouped or hierarchically structured data. For example, testing associations at different levels of phylogenetic trees, or within nested groups of an annotation ontology.

Kris Sankaran's and Susan Holmes' 2014 paper on the [structSSI R package](https://cran.r-project.org/web/packages/structSSI/index.html) in the [Journal of Statistical Software](https://www.jstatsoft.org/article/view/v059i13) provides a great, very readable summary of several approaches, together with a software implementation of the group Benjamini-Hochberg (GBH) procedure of [Hu, Zhao, and Zhou (2010)](https://www.tandfonline.com/doi/abs/10.1198/jasa.2010.tm09329) and the hierarchical false discovery rate (HFDR) controlling procedure of [Benjamini and Yekutieli (2003)](https://www.researchgate.net/publication/246367725_Hierarchical_FDR_testing_of_trees_of_hypotheses).

Highly recommended!
