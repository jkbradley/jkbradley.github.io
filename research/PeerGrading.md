---
layout: default
title: Peer Grading in Massive Open Online Courses (MOOCs)
---

<i>[Back to Home Page](../README.md)</i>

Massive Open Online Courses (MOOCs) have been both hyped as steps towards cheaper, more democratic education and criticized as low-quality substitutes for traditional education.
In this project, we propose to address one of the major challenges in MOOCs: grading and feedback.
Improving the quality of grading and feedback to students would improve learning outcomes and add value to MOOC course credits, making MOOCs a more useful and sustainable educational resource.

Limited resources in large courses prevent personalized feedback from instructors.
We therefore turn to <i>peer grading and feedback</i>, which has the potential to support inexpensive and scalable MOOCs.
Peer grading has been tested with limited success, yet we believe that further research could make it practical and reliable.

This project aims to develop a deeper understanding of peer grading via a combination of theoretical analysis and empirical testing.
We aim to establish bounds on reliability and scalability of peer grading systems.
Analysis of these fundamental properties will lay groundwork for long-term MOOC research and development.
We will use our analysis to develop practical grading and feedback systems which combine student and instructor input.

<b>Major challenges</b>

* <i>Limited grading resources</i>: We cannot expect students to grade more than a few peers.  Likewise, we cannot expect instructors to grade more than a tiny fraction of students.
* <i>Noisy grades</i>: Non-expert grades will be noisy.  Students may put varying amounts of effort into grading.
* <i>Ground truth</i>: Collecting ground truth (e.g., instructor grades) is expensive.  The topic itself may be subjective.

<b>Primary research questions</b>

* <i>Reliability</i>: What a priori quality guarantees can we give for peer grading systems?  During a course, how can reliability be assessed and improved by the system or instructor?
* <i>Scalability</i>: What are fundamental scaling limits of peer grading systems (e.g., in terms of sample comlexity), and what assumptions or system modifications can change those limits?
* <i>Cardinal vs. ordinal assessment</i>: How does the basic assessment method affect reliability of peer grades?  Are cardinal grades or pairwise comparisons better, and in which types of tasks? 
* <i>Incentives</i>: How can we build interpretable incentives into the system to encourage students to give higher quality peer grades and feedback? 
* <i>Interventions</i>: What other interventions can improve the reliability or scalability of peer grading?  Interventions might include targeted use of instructor grading, systems for student complaints, and adaptive grader-gradee assignment.

### Documents

Nihar B. Shah, Joseph K. Bradley, Abhay Parekh, Martin Wainwright, and Kannan Ramchandran.
<br><b>A Case for Ordinal Peer-evaluation in MOOCs.</b>
<br><i>NeurIPS Workshop on Data Driven Education, 2013.</i>

* [Paper (PDF)](/assets/papers/2013_neurips_moocs.pdf)

N. Shah, S. Balakrishnan, J. Bradley, A. Parekh, K. Ramchandran and M. Wainwright.
<br><b>Estimation from Pairwise Comparisons: Sharp Minimax Bounds with Topology Dependence.</b>
<br><i>JMLR 17(58): 1-47, 2016</i>.

* [JMLR page](https://jmlr.org/papers/v17/15-189.html)
* [Paper (PDF)](/assets/papers/2016_jmlr_pairwise_comparisons.pdf)
* There was an earlier version presented at [AISTATS 2015](http://proceedings.mlr.press/v38/shah15.html).  See the [PDF](/assets/papers/2015_aistats_pairwise_comparisons.pdf) and [supplement](/assets/papers/2015_aistats_pairwise_comparisons_supp.pdf).
