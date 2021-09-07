## 3.1 Growing Random Networks
* Why do we care about these networks?
  * It is a richer model that may capture things that might not have been captured in other models
  * Natural form of heterogeneity and age
  * A form of dynamics
  * Natural way of varying degree distributions
    * Not pre specified as in static models
* Distribution of Expected Degrees
  * Expected degree for node i at m<i<t is m +m/(i+1)+ m/(i+2) + ….. + m/t or m(1+log(t/i)) → Harmonic numbers
  * Nodes that have expected degree less than d at some time t are those such that m(1+log(t/i)) < d, so it is those → i<t e-(d-m)/m
* Degree Distribution of growing random networks
  * Distribution of expected degrees is such that d-m is exponentially distributed (mean m)
  * It is a good approximation for large t - need to be more cautious when dealing with large number arguments

## 3.2 Mean Field Approximations
* Continuous Time Approximation
  * ddi(t)/dt = m/t and di(i) = m
    * New links are gained per unit time
    * di(i) = m → starting condition
  * di(t) = m + m log(t/i)
  * Similar equation to the Growing Random Networks
* Preferential Attachments
  * Other methods of linking tan uniformly at random rto existing nodes
  * Would it be possible to get other degree distributions → power laws
  * Power Law [Simon 1955]
    * Rich get richer - growth of existing objects is proportional to size
    * New objects enter over time (Natural Growth)
    * Previous Models don't have “Fat tails” of degree distributions
    * Nodes born over time, form links at random with existing nodes
      * Form links with probability proportional to the number of links a nides already has → “rich get richer”

## 3.3 Preferential Attachment
* Preferential Attachments
  * (Refers to a network describing and following birth vs. connectedness in the network)
  * Newborn nodes form m links to existing nodes
  * tm links in total (t as time)
  * Total degree is 2tm
  * Probability of attaching to i is di(t)/2tm
* Mean Field Approximations
  * Continuous time approximation (as mentioned above)
  * Distribution of expected degrees
  * Simulate the model to check
* Distribution of Expected Degrees
  * Nodes that have expected degree less than d at some time t are those such that 
  * m (t/i)½<d → i> tm2/d2
* Power Law
  * ft(d) = 2m2/d → log(f(d)) = log(2m2) - 3log(d)

## 3.4 Hybrid Models
* Hybrid Models
  * More on Growing Random Network Models:
    * More general Degree Distributions
    * Other than extremes of random or preferential attachment
  * Some fits of hybrid models
* Simple Hybrid
  * Fraction a uniformly at random, 1-a via searching neighborhoods of friends
    * There are a bunch of nodes that are already out there and if a new node is born then if first finds links uniformly at random then it pick new nodes to link up to based on the connection it has already made
  * Meeting “Friends of Friends”
    * Find new nodes via others: Network based search
    * New node meet a “m” nodes uniformly at random and directs links to them
    * Meets (1-a) m of their neighbors and attached to them
    * The distribution of neighbors nodes is not the same as the degree distribution - eben with independent link formation
    * A neighbor is more likely to be higher degree
* Relation to Preferential Attachment
  * In a network with half degree k and half degree 2k individuals:
    * Randomly select a link and then a node on one end of it - ⅔ chance that is has a degree of 2k, ⅓ chance that it has degree k
* Degree Distribution
  * Nodes that have expected degree less than d at same time t are those i such that:
  * (m + xam)(t/i)1/x- xam < d ; where x = 2/(1-a)
  * critical  i is such that i/t = [(m+xam)/(d+xam)]x
    * F(d) = (t-i)/t
  * F(d) = 1-((m+amx)/(d+amx))x ; where x = 2/(1-a)
* Spans Extremes
  * F(d) = 1-((m+amx)/(d+amx))x ; where x = 2/(1-a)
    * A near 1 nearly exponential
    * A near 0 nearly preferential

## 3.5 Fitting Hybrid Models 
* Fitting to data
  * F(d) = 1-((m+amx)/(d+amx))x ; where x = 2/(1-a)
  * log(1-f(d)) = c-x log(d+amx)
    * Estimate “m” directly
    * Select a to minimize distance between actual distribution and models distribution
* Fitting “Friends of Friends” model
  * Fit to estimate ratio of random to network based links → r = mr/mn
    * Before r = a/(1-a)
  * “r” ranges from 0 to infinity, while “a” ranges from 0 to 1
* Friends of Friends/Hybrid Models:
  * They provide us with:
    * Variety of degree distributions
    * Tie degree distributions to way in which links are formed:
      * Fat tails from the network meeting process
      * More likely to meet well connected nodes
    * Clustering from network meeting process
      * Connecting to friends of friends
    * Diameter naturally as small as E-R network 
    * Assortativy in degree based on age

## 3.6 - 3.9  ERGMs (Exponential Random Graph Models)
* Popular Set of Models: ERGMs
  * Flexible way to introduce various local features and dependencies
  * estimated  statistically
* Markov, p*, ERGMs
  * The other models are not great for fitting data, especially with clustering or other dependencies
  * Link ij’s probability could depend on presence of jk and ik
  * But then thing interlock and need to specify full interdependencies
* Using p*/ERG Models
  * Pr(g) = epx[Σ βk sk (g)]/c
  * Power of such models: con put all sports of statistics in sk → can have it depends on arbitrary shapes, be specific to certain nodes/links
* ERGMs
  * Pr(g) = [epx[Σ βk sk (g) + ….. + Σ βk sk (g)]]/[Σg’ epx[Σ βk sk (g) + ….. + Σ βk sk (g)]]
    * MCMC (Markov Chain Monte Carlo) techniques for estimation have led to these becoming standard
    * Sampling g’s will not lead to accurate estimates (not just MCMC limitation)
  * Issues
    * MCMC estimation techniques are inaccurate
      * Can just one compute the parameters
    * Consistency of estimators of ERGMs:
      * When are parameters accurate and how many nodes are needed
    * How can we use these models to sample?
      * How to extend to larger data, infer missing data

## Summary
* Growing random networks: provide heterogeneity based on age - analyze via mean field
* Can lead to power laws with pure preferential attachment
* Many networks lie between the extremes: friends of friends
* Class of models providing statistical fits: ERGMs
* Allows formation based on structures beyond links- correlations
* Can be challenging to estimateL need to calculator relative probabilities
* New techniques/variations based on direct static coins offer alternatives
