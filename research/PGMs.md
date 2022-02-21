---
layout: default
title: Probabilistic Graphical Models (PGMs)
---

<i>[Back to Home Page](../README.md)</i>

This page includes several projects on learning the structure and parameters of Probabilistic Graphical Models (PGMs).
We focus on Conditional Random Fields (CRFs), which model conditional probability distributions P(Y|X) and thus
generalize Markov Random Fields (MRFs).

<i>From my thesis</i>: CRFs can offer computational and statistical advantages over generative models, yet traditional
CRF parameter and structure learning methods are often too expensive to scale up to large problems. We develop methods
capable of learning CRFs for much larger problems. We do so by decomposing learning problems into smaller, simpler
subproblems. These decompositions allow us to trade off sample complexity, computational complexity, and potential
for parallelization, and we can often optimize these trade-offs in model- or data-specific ways. The resulting methods
are theoretically motivated, are often accompanied by strong guarantees, and are effective and highly scalable in
practice.

### Code

[Statistical Inference and Learning Library (SILL)](SILL.md):
Probabilistic Graphical Models (Markov Random Fields and Conditional Random Fields) library for inference and learning.
Also includes discriminative methods such as boosting, plus several sub-projects.

### Documents

Joseph K. Bradley.
<br><b>Learning Large-Scale Conditional Random Fields.</b>
<br><i>Ph.D. Thesis, Machine Learning Department, Carnegie Mellon University, 2013.</i>

* [Thesis PDF](/assets/papers/2013_JosephBradley_thesis.pdf)
* [Defense PPT](/assets/papers/2013_JosephBradley_defense.ppt)
* My thesis links together ideas for PGM structure and parameter learning and for sparse regression by discussing trade-offs between sample complexity, computational complexity, and potential for parallelization.

Joseph K. Bradley and Carlos Guestrin.
<br><b>Sample Complexity of Composite Likelihood.</b>
<br><i>International Conference on Artificial Intelligence and Statistics (AISTATS), 2012.</i>

* [Paper PDF](/assets/papers/2012_aistats_complike.pdf)
* [Poster PPT](/assets/papers/2012_aistats_complike_poster.ppt)                                                                                                                                                                                                                                                                                                                        |
* This paper considers parameter learning for complex PGMs for which exact inference is intractable.  It proves finite-sample guarantees for composite likelihood, which avoids intractable inference during learning by effectively breaking the model into simpler components.

Joseph K. Bradley and Carlos Guestrin.
<br><b>Learning Tree Conditional Random Fields.</b>
<br><i>International Conference on Machine Learning (ICML), 2010.</i>

* [Paper PDF](/assets/papers/2010_crf_structure.pdf)
* This paper points out that estimating tree CRFs is considerably harder than estimating tree MRFs, and that the natural generalization of Chow-Liu is not necessarily the best option for estimating tree CRFs.  We suggest some heuristics which improve performance.
