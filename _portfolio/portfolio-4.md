---
title: "Paper Review: \"Developing a deep learning framework with two-stage feature selection for multivariate financial time series forecasting\""
excerpt: "<img src='/images/portfolio/time_series.png'>"
collection: portfolio
category: Deep Learning
---

* __With__: Félix Fourreau
* __Ressources__: [Report](/files/portfolio/ts_report.pdf); [Slides](/files/portfolio/ts_slides.pdf); [Code](https://www.kaggle.com/code/mathiswauquiez/time-series-financial-forecasting)
* __When__: 2025
* __Associated to__: [MVA](https://www.master-mva.com/)

This project was done as part of the MVA course on Learning for Time Series. The goal was to review a paper that uses a two stage feature selection method, based on RreliefF and a modified version of the Grey Wolf Optimizer, called Binary Grey Wolf Optimizer with Cuckoo Search to select the most relevant features for a multivariate time series forecasting problem. The authors then uses these features to train a RNN model. Multiple issues arises in this paper, which we discussed in depth. This was an "interesting" project, where we learned as much about feature selection as we did about how research papers can sometimes pass through the peer review process with major flaws and suspicious results. We did not manage to replicate the results of this paper (notably, our accuracy was worse on the test set, as opposed to the paper's results).