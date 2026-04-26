---
permalink: /dcam
hidden: true
classes: wide
# layout: single-hf
# layout: single
layout: default
title: "dCAM: Explaining multivariate data series classification"
author_profile: true
redirect_from: 
  - /dcam
  - /dcam.html
---

# dCAM: Dimension-wise Class Activation Map for Explaining Multivariate Data Series Classification
Paul Boniol, Mohammed Meftah, Emmanuel Remy, Themis Palpanas


![dcam example](https://boniolp.github.io/assets/img/dcam_example.jpg)

## Abstract
<p style='text-align: justify;'>
Data series classification is an important and challenging problem in data science. Explaining the classification 
  decisions by finding the discriminant parts of the input that led the algorithm to some decision is a real need 
  in many applications. Convolutional neural networks perform well for the data series classification task; though, 
  the explanations provided by this type of algorithms are poor for the specific case of multivariate data series. 
  Addressing this important limitation is a significant challenge. In this paper, we propose a novel method that 
  solves this problem by highlighting both the temporal and dimensional discriminant information. Our contribution 
  is two-fold: we first describe a convolutional architecture that enables the comparison of dimensions; then, we 
  propose a method that returns dCAM, a Dimension-wise Class Activation Map specifically designed for multivariate 
  time series (and CNN-based models). Experiments with several synthetic and real datasets demonstrate that dCAM is 
  not only more accurate than previous approaches, but the only viable solution for discriminant feature discovery 
  and classification explanation in multivariate time series.
</p>

## Papers

| Research paper | [dCAM: Dimension-wise Class Activation Map for Explaining Multivariate Data Series Classification, SIGMOD (2022)](https://www.researchgate.net/publication/361416963_dCAM_Dimension-wise_Class_Activation_Map_for_Explaining_Multivariate_Data_Series_Classification) | [bibtex](https://dblp.org/rec/conf/sigmod/BoniolMRP22.html?view=bibtex) |
| Journal Version | [dCNN/dCAM: Anomaly Precursors Discovery in Multivariate Time Series with Deep Convolutional Neural Networks, DCE (2023)](https://www.researchgate.net/publication/376477657_dCNNdCAM_anomaly_precursors_discovery_in_multivariate_time_series_with_deep_convolutional_neural_networks) |  |
| data  | [dCAM website](https://helios2.mi.parisdescartes.fr/~themisp/dCAM/) |  |
| code  | [GitHub repo](https://github.com/boniolp/dCAM) |  |
| ACM SIGMOD ARI | [Reproducibility report](https://reproducibility.sigmod.org/rep_rep/2023/Carbone-SIGMODReproReport23.pdf) | |

[Back to main page](https://boniolp.github.io/)
