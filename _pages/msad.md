---
permalink: /msad
hidden: true
classes: wide
# layout: single-hf
# layout: single
layout: default
title: "Choose Wisely: An Extensive Evaluation of Model Selection for Anomaly Detection in Time Series"
author_profile: true
redirect_from: 
  - /msad
  - /msad.html
---

# Choose Wisely: An Extensive Evaluation of Model Selection for Anomaly Detection in Time Series
Emmanouil Sylligardos, Paul Boniol, John Paparrizos, Panos Trahanias, Themis Palpanas

<p align="center">
<img src="https://boniolp.github.io/assets/img/msad_pipeline.jpg" alt="Evaluation pipeline" width="570"/>
</p>


## Abstract
<p style='text-align: justify;'>
Anomaly detection is a fundamental task for time-series analytics with important implications for the downstream performance of many applications. 
  Despite increasing academic interest and the large number of methods proposed in the literature, recent benchmark and evaluation studies demonstrated 
  that no overall best anomaly detection methods exist when applied to very heterogeneous time series datasets. Therefore, the only scalable and viable 
  solution to solve anomaly detection over very different time series collected from diverse domains is to propose a model selection method that will 
  select, based on time series characteristics, the best anomaly detection method to run. Existing AutoML solutions are, unfortunately, not directly 
  applicable to time series anomaly detection, and no evaluation of time series-based approaches for model selection exists. Towards that direction, 
  this paper studies the performance of time series classification methods used as model selection for anomaly detection. Overall, we compare 17 
  different classifiers over 1800 time series, and we propose the first extensive experimental evaluation of time series classification as model 
  selection for anomaly detection. Our results demonstrate that model selection methods outperform every single anomaly detection method while being in 
  the same order of magnitude regarding execution time. This evaluation is the first step to demonstrate the accuracy and efficiency of time series 
  classification algorithms for anomaly detection, and represents a strong baseline that can then be used to guide the model selection step in general 
  AutoML pipelines.
</p>

<p align="center">
<img src="https://boniolp.github.io/assets/img/msad_intro_fig.jpg" alt="Overall results" width="570"/>
</p>


## Papers

| Research paper | Choose Wisely: An Extensive Evaluation of Model Selection for Anomaly Detection in Time Series, PVLDB (2023), [Researchgate](https://www.researchgate.net/publication/373337385_Choose_Wisely_An_Extensive_Evaluation_of_Model_Selection_for_Anomaly_Detection_in_Time_Series),[VLDB](https://www.vldb.org/pvldb/vol16/p3418-boniol.pdf) | [bibtex](https://boniolp.github.io/assets/pdfs/msad.txt) |
| Webapp | [ADecimo](https://adecimots.streamlit.app/) |  |
| Source code | [MSAD](https://github.com/boniolp/MSAD) |  |

[Back to main page](https://boniolp.github.io/)
