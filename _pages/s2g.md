---
permalink: /s2g
hidden: true
classes: wide
# layout: single-hf
# layout: single
layout: default
title: "Series2Graph: Graph-based Subsequence Anomaly Detection in Time Series"
author_profile: true
redirect_from: 
  - /s2g
  - /s2g.html
---

# Series2Graph: Graph-based Subsequence Anomaly Detection in Time Series
Paul Boniol, Themis Palpanas, Mohammed Meftah, Emmanuel Remy


![s2g framwork](https://boniolp.github.io/assets/img/full_process_sumary_s2g.jpg)

## Abstract
<p style='text-align: justify;'>
Subsequence anomaly detection in long sequences is an important problem with applications in a wide range of domains.
However, the approaches that have been proposed so far in the literature have severe limitations:
they either require prior domain knowledge that is used to design the anomaly discovery algorithms, or become cumbersome and expensive to use in situations with recurrent anomalies of the same type.
In this work, we address these problems, and propose an unsupervised method suitable for domain agnostic subsequence anomaly detection. Our method, Series2Graph, is based on a graph representation of a novel low-dimensionality embedding of subsequences. Series2Graph needs neither labeled instances (like supervised techniques), nor anomaly-free data (like zero-positive learning techniques), and identifies anomalies of varying lengths.
The experimental results, on the largest set of synthetic and real datasets used to date, demonstrate that the proposed approach correctly identifies single and recurrent anomalies without any prior knowledge of their characteristics, outperforming by a large margin several competing approaches in accuracy, while being up to orders of magnitude faster.
</p>
![example s2g](https://boniolp.github.io/assets/img/figure_exp_s2g.jpg)

## Papers

| Research paper | [Series2Graph: Graph-based Subsequence Anomaly Detection in Time Series, PVLDB (2020)](https://boniolp.github.io/assets/pdfs/Series2Graph.pdf) | [bibtex](https://boniolp.github.io/assets/pdfs/series2graph.txt) |
| Demonstration paper | [GraphAn: Graph-based Subsequence Anomaly Detection, demo PVLDB (2020)](https://boniolp.github.io/assets/pdfs/Graphan.pdf) | [bibtex](https://boniolp.github.io/assets/pdfs/graphan.txt) |

[Back to main page](https://boniolp.github.io/)
