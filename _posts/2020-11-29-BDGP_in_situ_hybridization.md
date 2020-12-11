---
title: "Fastai: Drosophila embryogenesis"
layout: post
toc: false
comments: true
hide: false
search_exclude: false
categories: [fastai, fruitflies]
---

To learn more about *deep learning* methods, I have begun working through the
[fastai book](https://github.com/fastai/fastbook). 

As always, the best way for me to learn is to dive into a small project of my own - an attitude strongly supported by the fastai authors.

The book uses [image classification](https://github.com/fastai/fastbook/blob/master/01_intro.ipynb) as an example, so I decided to look for a suitable image analysis project to help me learn.

Years ago, I studied the development of the [fruitfly](https://en.wikipedia.org/wiki/Drosophila_melanogaster) , especially the formation of its muscle system during embryogenesis.

![Fruit fly](https://cdn.arstechnica.net/wp-content/uploads/2013/01/fruit_fly.jpg)

So I decided to return to my scientific roots and explore images of fruitfly embryogenesis.

## The BDGP project

In 2009 the [Berkeley Drosophila Genome Project](https://insitu.fruitfly.org/cgi-bin/ex/insitu.pl) documented the expression patterns of most fruitfly genes using *in situ* hybridization. The researcherstook a large number of digital images of individual embryos, each stained with a specific probe to highlight the transcripts of one gene.

In total, the [BDGP project](https://insitu.fruitfly.org/cgi-bin/ex/insitu.pl) examined 8532 genes and documented them with 140427 digital photographs.

Embryonic development takes about 22 hours and has been subdivided into separate stages discernable under the microscope.

![Drosophila embryogenesis stages](https://embryology.med.unsw.edu.au/embryology/images/thumb/e/ec/Drosophila_table.JPG/550px-Drosophila_table.JPG)

Here is the expression of one gene, Ecdysone-inducible gene L2 (* ImpL2*) at 
[stage 7]() of development, for example:

![ImpL2 expression](https://insitu.fruitfly.org/insitu_image_storage/img_dir_10/insitu10383.jpe)

Gene expression is dynamic, e.g. it changes over time as the embryo develops. To see how *ImpL2* changes over time, check out the [BDGP's full report](https://insitu.fruitfly.org/cgi-bin/ex/report.pl?ftype=3&ftext=SD07266)

After staining and imaging a large number of fruitfly embryos ([Weiszmann et al, 2009](https://pubmed.ncbi.nlm.nih.gov/19360017/)), the researchers carefully

1. Identified single embryos in the field of view, and cropped the image accordingly.
2. Oriented each image so that the anterior end of the embryo faced left.
3. Assigned a developmental stage.
4. Described the (often complex) expression patterns they observed using a [controlled vocabulary](https://insitu.fruitfly.org/cgi-bin/ex/insitu.pl?t=html&p=annotation) of anatomical terms.

Using this large image dataset, the BDGP project performed and published numerous analyses, e.g.

- [Global analysis of patterns of gene expression during Drosophila embryogenesis](https://pubmed.ncbi.nlm.nih.gov/17645804/)

![](https://www.ncbi.nlm.nih.gov/pmc/articles/instance/2323238/bin/gb-2007-8-7-r145-4.jpg)

- [Systematic image-driven analysis of the spatial Drosophila embryonic expression landscape](https://pubmed.ncbi.nlm.nih.gov/20087342/)
- [A quantitative spatiotemporal atlas of gene expression in the Drosophila blastoderm](https://pubmed.ncbi.nlm.nih.gov/18423206/)

and many more.

The images have been made available publicly, e.g. via [this site](https://insitu.fruitfly.org/cgi-bin/ex/insitu.pl?t=html&p=downloads) - 250 GB of image data in total.

Other researchers have used this resource and implemented machine learning models, e.g.

- [Automated annotation of developmental stages of Drosophila embryos](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3892688/)
- [AnnoFly: annotating Drosophila embryonic images based on an attention-enhanced RNN model](https://academic.oup.com/bioinformatics/article-abstract/35/16/2834/5270662?redirectedFrom=fulltext)
- [Deep Low-Shot Learning for Biological Image Classification](https://www.groundai.com/project/deep-low-shot-learning-for-biological-image-classification-and-visualization-from-limited-training-samples/1)

<strike>Unfortunately, the FTP server requires a login/password, which is not provided on the page. The [contacts](https://insitu.fruitfly.org/cgi-bin/ex/insitu.pl?t=html&p=contact_us) form seems to be broken (not surprising for a website of a research project conducted more than 10 years ago).

I contaced [Susan Celniker](https://www.genetics.org/content/204/3/845), a researcher at the Lawrence Berkeley National Laborator and key driver of the Drosophila genome / BDGP efforts to see if she could help me out 🤞🏻.
</strike> 

The BDGP FTP server is up serving anonmous requests without a login again! Thanks a lot, BDGP team!



## Fly-FISH

Another project used fluorescent microscopy to generate even higher resolution images of gene expression patterns during fruitfly embryogenesis: [Fly-FISH](http://fly-fish.ccbr.utoronto.ca/)

The images have sub-cellular resolution and are beautiful:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ox27uj3fgcc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

