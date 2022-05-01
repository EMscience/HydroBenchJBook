# Information-Theoretic Performance Measures

HydroBench allows the computation of multi-dimensional entropies (H(.)), Mutual Information MI(.,.) and Tranfer Entropy - TE represented as MI(.,.|.). 
By using these metrics, two model diagnostics can be undertaken:

1. understanding the tradeoffs between predictive and functional model performances.
2. understanding model internal functions that lead to the predictive performance using Process Networks.

MI is used as a predictive performance metrics while TE is used as an indicator of model functional performance. 

The computation of MI and TE requires different [joint](https://en.wikipedia.org/wiki/Joint_probability_distribution) 
and [marginal](https://en.wikipedia.org/wiki/Marginal_distribution) probabilities of the various flux and store hydrological
variables referred in the input table header. In order to compute these probabilities, HydroBench employed histogram based
probability estimation. 

Table 1 below shows the syntax, description and equations of the Information-theoretic metrics. For their implementation,
please refere to the example notebook. 
 

![InformationTheoreticMetrics](./images/InformationTheoreticMetrics.png)