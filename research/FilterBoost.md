---
layout: default
title: Boosting-by-Filtering
---

<i>[Back to Home Page](../README.md)</i>

We examine boosting in the filtering framework, where the learner does
not use a fixed training set but rather has access to an example oracle
which can produce an unlimited number of examples from the target distribution.
This setting is useful for modeling learning with datasets too large to fit
into a computer, learning in memory-limited situations, or learning from
an online source of examples (e.g. from a web crawler).

### Code

Two implementations of FilterBoost are available here:

* [Java code from original paper](FilterBoost/FilterBoost_code.tgz): This code is quite old and probably less efficient than the SILL code, but it is stand-alone and should be easier to get working.
* [SILL Project codebase](SILL.md): This SELECT Lab codebase is mainly for probabilistic graphical models, but it includes a section for discriminative learning which includes FilterBoost and other algorithms.  This codebase has more dependencies and may not be stable.

### Documents

Joseph K. Bradley and Robert E. Schapire.
<br><b>FilterBoost: Regression and Classification on Large Datasets.</b>
<br><i>Advances in Neural Information Processing Systems (NIPS), 2008.</i>

* [Paper (PDF) with appendix](/assets/papers/2008_neurips_FilterBoost.pdf)
* [Slides (PPT) from talk at NeurIPS](/assets/papers/2008_neurips_FilterBoost.ppt)

Joseph K. Bradley.
<br><b>FilterBoost: Regression and Classification on Large Datasets.</b>
<br><i>Data Analysis Project (Master's thesis equivalent) for the Machine Learning program at Carnegie Mellon University, 2009.</i>

* [Paper (PDF)](/assets/papers/2009_dap_filterboost.pdf): This is an extended version of the original paper which adds multiclass extensions using error-correcting output codes.
