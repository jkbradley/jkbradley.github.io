---
layout: default
title: Statistical Inference and Learning Library (SILL)
---

<i>[Back to Home Page](../README.md)</i>

This codebase was developed within the Select Lab for inference and learning with Probabilistic Graphical
Models (PGMs).  It includes code from several of my projects, as well as others within the lab.
There are also several sub-projects which were built on top of SILL and are linked below.

## Library Contents

* Models
  * Variables: discrete and real-valued
  * Factors
    * Basic: tabular, Ising, Gaussian
    * Higher-order: mixture, hybrid
    * Also: marginal (for MRFs) and conditional (for CRFs), templated (for parameter tying)
  * Model types and representations
    * Bayesian Networks (BNs)
    * Markov Random Fields (MRFs)
    * Conditional Random Fields (CRFs)
    * Factor Graphs
    * <i>Note</i>: Junction trees and high-treewidth models supported
* Inference
  * Junction tree inference (exact)
  * Belief propagation (several variants)
  * Gibbs sampling
* Parameter Learning (<i>mostly max-likelihood</i>)
  * Low-treewidth MRF learning (non-iterative)
  * Low-treewidth CRF learning
  * EM for mixtures of Gaussians
  * Iterative Proportional Fitting
  * Factor learning
* Structure Learning
  * Chow-Liu (trees)
  * Generalized piecewise-likelihood-based Chow-Liu (tree CRFs)
  * Order-based search (low-treewidth BNs)
  * Local/greedy structure search (low-treewidth)
* Optimization (<i>used for parameter learning</i>)
  * Methods: gradient descent, conjugate gradient, L-BFGS, stochastic gradient
* Discriminative Learning (<i>mostly separate part of library</i>)
  * Base classifiers: decision stump, decision tree, naive Bayes, prototype-based K-nearest neighbors
  * Regression methods: linear regression, logistic regression (binary and multiclass)
  * Boosting: AdaBoost, FilterBoost, MadaBoost
  * Multiclass support
    * Conversions to binary: all-pairs
    * Algorithms: AdaBoost variants (MH, OC), FilterBoost variants (OC)
  * Multilabel support: conversion to multiclass
  * <i>Also</i>: Classifier cascades

## Code

The SILL codebase is still available in the [Google Code archive](http://code.google.com/p/sill/).
