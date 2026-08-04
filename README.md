# Objective Priors for the Degrees of Freedom of a Multivariate t Distribution and the t-Copula

## Overview

This repository contains the R code and R Markdown reports used to reproduce
the results in:

> Villa, C. and Rubio, F.J. (2018). Objective priors for the number of degrees
> of freedom of a multivariate t distribution and the t-copula.
> *Computational Statistics and Data Analysis* **124**: 197–219.
> [DOI: 10.1016/j.csda.2018.03.010](https://doi.org/10.1016/j.csda.2018.03.010) |
> [Preprint (arXiv:1701.05638)](https://arxiv.org/abs/1701.05638)

Inference on the number of degrees of freedom ($\nu$) of a multivariate t
distribution — and, until this work, of the t-copula — has historically been
problematic, particularly when $\nu$ is treated as a discrete parameter.
This paper proposes an **objective Bayesian approach** for estimating $\nu$ in
both settings, using a **loss-based criterion** that sidesteps the difficulty
of assigning objective probabilities directly to a discrete parameter. The
resulting prior is truncated, reflecting the fact that both the multivariate
t distribution and the t-copula converge to normality as $\nu$ grows large.
The methodology is validated on simulated data and applied to daily
logarithmic returns of IBM stock and CRSP database returns.

## Repository structure

```
OBayesMTCopT/
├── PriorTKL.Rmd / .html      # Construction of the loss-based prior for ν
├── PriorTW.Rmd / .html      # Weakly informative prior for ν
├── DKLtn.Rmd / .html        # Kullback Leibler divergence between a multivariate t and a multivariate normal
├── DKLt.Rmd / .html         # Kullback Leibler divergence between two multivariate t
├── PostOBayesT.Rmd / .html  # Application
└── tcop.Rmd / .html         # t-copula
```

## Requirements

The following R packages are required. Verify against the `library()` calls
at the top of each `.Rmd` file:

```r
install.packages(c("mvtnorm", "copula", "knitr", "rmarkdown"))
```

## Citation

If you use this code, please cite:

```bibtex
@article{villa2018obayes,
  author  = {Villa, C. and Rubio, F.J.},
  title   = {Objective priors for the number of degrees of freedom of a
             multivariate t distribution and the t-copula},
  journal = {Computational Statistics and Data Analysis},
  volume  = {124},
  pages   = {197--219},
  year    = {2018},
  doi     = {10.1016/j.csda.2018.03.010}
}
```

## License

No licence file is currently included in this repository. If you intend to
reuse or adapt this code, please contact the authors.
