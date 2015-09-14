---
layout: post
title: "MOSAIC: back and better than ever"
description: "With a bit of rebranding and improved visualizations of the algorithm, MOSAIC easily find a home."
category: projects
tags: [software, ortholog detection]
comments: true
share: true
---

In our [last update]({% post_url projects/2014-05-28-MOSAIC-Rejected %}), I described the rejection of our comparative genomic method paper based on the concerns of a single reviewer. These concerns were clearly addressed both in figures and in the main text. However, we could have made the presentation clearer and more considerate to a broader audience of, e.g. interested (but potentially overworked) non-experts.

Today, I'm happy to report that that our paper has been accepted to _Genes, Genomes, and Genetics (G3)_ under the title ["Rock, paper, scissors: harnessing complementarity in ortholog detection methods improves comparative genomic inference."](http://www.g3journal.org/content/5/4/629.long) They say that rejection tends to improve the quality and impact of manuscripts ([see write-up](http://www.nature.com/news/rejection-improves-eventual-impact-of-manuscripts-1.11583)). In our case, I think that the extra time and improved focus on clarity and approachability absolutely improved the presentation of the method.

<figure align="center">
    <img src="{{ site.url }}/images/MOSAIC_opt.jpg"  WIDTH="300" BORDER="0" ALIGN="middle" > 
    <figcaption align="left"><i>A schematic of MOSAIC's sequence selection algorithm. Steps: (1) Construct graph; (2) Choose the sequence from a random OD method for each species; (3) Iterate through species. For each species, pick the orthologs with highest similarity to the current best choices for all other species; (4) Return current best choices if no changes are made after iterating through all species; (5) To find global optimum, repeat steps 1-4 with random sampling paths.</i></figcaption>
</figure>

A bit of background on the paper: comparative genomics often relies on the comparison of evolutionarily related sequences from different species (orthologs). Many methods analyze orthologous sequences, but what happens if the orthologs themselves are poorly called? In our experience, this leads to a "garbage in, garbage out" scenario. For this reason, we were motived to improve ortholog detection by building a statistical framework for harnessing the deep complementarity between methodologically diverse ortholog detection methods. 

<figure align="middle">
    <img src="{{ site.url }}/images/MOSAIC_MSA.jpg" HEIGHT="400" WIDTH="500" BORDER="0" ALIGN="middle"> 
    <figcaption align="left"><i>The result of sequence integration for carbonic anhydrase 12. Orthologs that were not returned for a given species are denoted with a horizontal black bar. Those that were filtered using pre-integration sequence identity cutoffs are indicated with gray bars with the global percent identity from pairwise alignment to human included. Species name label colors denote the species of origin for orthologs in the MOSAIC alignment.</i></figcaption>
</figure>
  

In "Paper, Rock, Scissors", 1.) we demonstrate this methodological complementarity, 2.) we develop a tool for taking advantage of it, 3.) we show that our tool maintains or improves data quality across wide variety of measures while also retrieving a great deal more sequences, and 4.) apply our method to find an intriguing and otherwise undetectable positively selected site in TPSAB1, an enzyme linked to asthma, heart disease, and irritable bowel disease. 

<figure align="middle">
    <img src="{{ site.url }}/images/MOSAIC_PSS.jpg" HEIGHT="400" WIDTH="450" BORDER="0" ALIGN="middle"> 
    <figcaption align="left"><i>Example: a MOSAIC-specific PSS in Tryptase Alpha/Beta 1 (TPSAB1). The tetrameric TPSAB1 structure is shown with positively selected sites highlighted. The site detected by component methods and by MOSAIC is colored orange, whereas the MOSAIC-specific PSS is featured in red. A bound inhibitor (white) pinpoints the active site of the enzyme.</i></figcaption>
</figure>


