# Contribution Evaluation Sub-problem in Incentive Mechanism of Federated Learning [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

## A Principled Approach to Data Valuation for Federated Learning

<strong>Year:</strong> 2020

<strong>Conference & Journal:</strong> Federated Learning(by 丛明舒)

<strong>Authors:</strong> Tianhao Wang, Johannes Rausch, Ce Zhang, Ruoxi Jia, and Dawn Song (ETH)

### The problems can be solved:

- Computation is time-consuming
- Canonical Shapley Value neglects the order of data sources, yet in FL the importance of a data source
could depend on when it is used for training. For example, the data sources used toward the end of learning process could be less inuential.

### Solutions:
- <strong>Fairness:</strong>
- 
In order to balance fairness, the authors add selected clients of previous iterations $I_{1:t-1} = I_{1} + ... + I_{t-1}$.
Modify the shapley value equation as follow:

$$
s_{t}^{v}(i) = \frac{1}{|I_{t}|} \sum_{S \subseteq I_{t} \backslash \lbrace i \rbrace} \frac{1}{\binom{|I_{t}|-1}{|S|}}[v(I_{1:t-1} + (S \cup {i})) - v(I_{1:t-1} + S)]
$$

- <strong>Expensive computation:</strong> 
  
  Leveraging the existing approximation methods developed for the canonical Shapley Value. The two methods called _[Permutation Sampling-based Approximation](http://proceedings.mlr.press/v89/jia19a/jia19a.pdf)_ and  _[group testing-based approximation](https://eprints.soton.ac.uk/383963/1/__soton.ac.uk_ude_personalfiles_users_jo1d13_mydesktop_Sasan%2520Maleki%2520-%2520Thesis.pdf)_





