# Parallel Optimization for Sparse Regression

Sparse regression (Lasso, sparse logistic regression, etc.) is a workhorse of modern machine learning.
This work was on parallel optimization methods which can take advantage of properties of sparse regression to allow
parallelization, reduce computation, or reduce communication. For example, correlation between features can make
optimization difficult when partitioning datasets by features, but algorithms can adapt to this correlation to allow
greater parallelization. Another key property is sparsity in the optimal solution, which can permit more efficient
iterations and reduced communication.

This work included:

* Distributed sparse regression, especially using sparse communication
* General survey and comparison of parallel coordinate descent methods, geared towards understanding when modifications of the basic algorithm can be helpful
* Applying robust sparse Walsh-Hadamard Transform methods to learning "machine learning" models, such as decision trees

## Shotgun: Parallel Coordinate Descent

Our Shotgun algorithm was one of the first parallel coordinate descent methods for sparse regression. It comes with both
theoretical convergence guarantees and strong empirical performance. Since we proposed it, many variants have followed.

The actual algorithm is a very simple generalization of coordinate descent, allowing efficient implementation and  easy
modifications. Intuitively, it allows the amount of parallelization to be chosen based on correlation between features.
Uncorrelated problems allow lots of parallel coordinate updates, while very correlated features permit only a few
parallel coordinate updates.

### Code

The [Github Shotgun Project](https://github.com/akyrola/shotgun) contains code for Lasso and sparse logistic regression.
The code may require tweaks to run since it is C++ and quite old!

### Documents

Joseph K. Bradley, Aapo Kyrola, Danny Bickson, and Carlos Guestrin.
<br><b>Parallel Coordinate Descent for L1-Regularized Loss Minimization.</b>
<br><i>International Conference on Machine Learning (ICML), 2011.</i>

* [arxiv](https://arxiv.org/abs/1105.5379)
* [Main paper, with corrections](/assets/papers/2011_shotgun_corrected.pdf) <i>(This is an updated version which includes a correction to the original proof. Thanks to Martin Takac!)</i>
* Supplements
  * [Supplement: Theory](/assets/papers/2011_shotgun_supplement_theory_corrected.pdf)
  * [Supplement: scalability analysis](/assets/papers/2011_shotgun_scalability_analysis.pdf)
  * [Supplement: Lasso benchmark](/assets/papers/2011_shotgun_supp_benchmark_lasso.pdf)
  * [Supplement: Logreg benchmark](/assets/papers/2011_shotgun_supp_benchmark_logreg.pdf)

## Sparse Walsh-Hadamard Transforms

Walsh-Hadamard Transforms (WHTs) are special cases of multi-dimensional Discrete Fourier Transforms (DFTs).
A DFT takes a length-N vector indexed by 1,...,N and transforms it to another length-N vector.  A WHT does the same thing, but it has special structure.
A WHT operates on an n-dimensional binary finite field, so the vector is of length N=2^n.

<i>Comparing with "machine learning" regression</i>:
For WHTs, features are columns of the WHT matrix, and the sparsity in the solution refers to the WHT signal having a small number of non-zero frequency coefficients.
Since the WHT has special structure, we can locate and estimate these non-zero coefficients in sub-linear time.
Suppose the length-N signal has K non-zero coefficients.
Lasso must look at the full N-by-N WHT matrix, taking at least N^2 time.
Our methods can subsample cleverly, taking O(K*log^2(N)) samples and O(K*log^3(N)) time.

<i>Basic idea</i>: We subsample the signal, take the WHT of this shorter sequence, and use aliasing properties of the WHT to show that non-zero coefficients are separated out into (mostly) separate bins.  We examine each bin, decide how many non-zero coefficients it contains, and decode those coefficients.

### Documents

Xiao Li, Joseph K. Bradley, Sameer Pawar, and Kannan Ramchandran.
<br><b>Robustifying the Sparse Walsh-Hadamard Transform without Increasing the Sample Complexity of O(K log N).</b>
<br><i>IEEE International Symposium on Information Theory (ISIT), 2014.</i>

* [PDF](/assets/papers/2014_isit_wht.pdf)
