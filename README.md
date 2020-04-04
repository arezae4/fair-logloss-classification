# Fairness for Robust Log Loss Classification

This repository provides Python implementation for our AAAI 2020 paper [Fairness for Robust Log Loss Classification](https://arxiv.org/abs/1903.03910).

### Abstract

Developing classification methods with high accuracy that also avoid unfair treatment of different groups has become increasingly important for data-driven decision making in social applications. Many existing methods enforce fairness constraints on a selected classifier (e.g., logistic regression) by directly forming constrained optimizations. We instead re-derive a new classifier from the first principles of distributional robustness that incorporates fairness criteria into its worst-case logarithmic loss minimization. This construction takes the form of a minimax game and produces a parametric exponential family conditional distribution that resembles truncated logistic regression. We present the theoretical benefits of our approach in terms of its convexity and asymptotic convergence. We then demonstrate the practical advantages of our approach on three benchmark fairness datasets.

### Dependency

1. [numpy](https://www.scipy.org/scipylib/download.html)
2. [scipy](https://www.scipy.org/scipylib/download.html)

### Datasets

The provided version of [Adult](https://github.com/IBM/AIF360/blob/master/aif360/data/raw/adult/README.md) [(Code)](https://github.com/IBM/AIF360/blob/master/aif360/datasets/adult_dataset.py), and [COMPAS](https://github.com/IBM/AIF360/blob/master/aif360/data/raw/compas/README.md) [(Code)](https://github.com/IBM/AIF360/blob/master/aif360/datasets/compas_dataset.py) datasets are taken from [IBM AIF360 Toolkit](https://github.com/IBM/AIF360)
 
### Experiments

`test_fairlogloss.py` trains and tests a fair classifier given a fairness critria:
* **Demographic Parity** (*DP*)
* **Equalized Odds** (*EqOdd*)
* **Equalized Opportunity** (*EqOpp*)

To run the experiment for each dataset run:

```console
$ python test_fairlogloss.py [adult|compas] [dp|eqodd|eqopp] 
```

### References

1. Ashkan Rezaei, Rizal Fathony, Omid Memarrast, Brian Ziebart. "Fairness for Robust Log Loss Classification" (2019) [[arXiv]](https://arxiv.org/abs/1903.03910)
