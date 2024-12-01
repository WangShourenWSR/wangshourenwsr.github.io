---
layout: page
title: Sparse Logistic Regression with Majorization
description: Optimization for sparse logistic regression with majorization methods.
img: assets/img/projects/majorization/1.jpg
importance: 3
category: work
related_publications: false
---

In this project, I investigate sparse logistic regression using the L1 norm, a well-known technique for introducing sparsity in machine learning models. The L1 norm penalty, while widely applied in tasks such as lasso regression, presents challenges due to its non-differentiability, making traditional gradient-based optimization methods unsuitable. To address this, I explore the use of sub-gradient methods for optimization. Additionally, I delve into the majorization method, which provides a surrogate function to iteratively minimize the cost when a closed-form solution is unavailable. The method guarantees monotonic improvement from an initial solution by optimizing an upper bound on the objective function. This work reviews logistic regression with the L1 norm and discusses the application of majorization for optimization in sparse logistic regression. I compare the performance of the majorization method with gradient descent (GD) methods using L1 and L2 norms and propose future research directions focusing on low-rank approximations.

For detailed report, <a href="/assets/pdf/projects/majorization/report.pdf" download>please download the project report PDF file</a>


The project is implemented in MATLAB and has not yet been uploaded to GitHub. For access to the project code, please feel free to contact me directly.
