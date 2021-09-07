## 2.1 Homophily
* Characteristics of nodes: age, race, gender, religion, profession
  * Nodes that have similar characteristics interact with each other more
    * Nodes become segregated
  * Colors represents the nodes characteristics
* Reasons for Homophily
  * Contact Theory: prejudice and conflict between groups can be reduced if members of said group interact with each other.
  * Common set of understandings, culture, or language
  * Social Pressures
  * Social Competition
* Structures of a network are characteristic dependent
* Image: There is a major gap between these in the network shopping that black and whites are not that connected socially

## 2.2 Dynamics and Tie Strength
* Strength of Weak Ties
  * Weak Ties: Nodes that do not interact as much
  * Theory: Weak ties form ‘bridges’, less redundant information
  * Even if there are weak ties, information still passes through and acknowledged
  * People have a few strong ties and many weak ties
* Dynamics
  * Relationships do not stay the same, sometimes the characteristics of the nodes change

## 2.3 Centrality Measures - Degree, Closeness, Decay, and Betweenness
* Position in Network
  * How to describe individual characteristics
    * Degree 
    * Clustering
    * Distance to other nodes
    * Centrality
      * Influence
      * Power
* Degree Centrality
  * How “connected” in a node
  * Degree Captures connectedness
  * Normalize by n-1: Finding the most possible links a specific node can have
  * Image: Node 3 has the same degree as 1 and 2. Just because the position of node three does not seem like it's in the middle does not mean it is not central
* Centrality -> Four different things to measure:
  * Degree: Connectedness
  * Closeness, Decay: ease of reaching other nodes
    * How far I am, on average, from other nodes
  * Betweenness - roles as an intermediary; a connector
    * Do other pairs of nodes have to go through a third node to reach each other
  * Influence, Prestige, Eigenvectors - “not what you know, but who you know”
    * Your are important if you friends are important
    * Being well connected
* Closeness
  * Closeness Centrality: (n-1)/ Σ_{j} | (i,j)
    * Relative distances to other nodes
    * Scales directly with distance - twitch as far is half as central
* Decay Centrality
  * (C_i)^{d} (g) = Σ_{j≠i} δ | (i,j)
  * δ near 1 becomes component size
  * δ near 0 becomes degree 
  * δ in between decaying distance measure
    * Weights distance exponentially
  * Normalize: Decay Centrality
    * C_i^{d} (g) = Σ_{j≠i} δ | (i,j)  / ((n-1) δ)
    * (n-1) δ is the lowest decay possible
* Betweenness (Freeman) Centrality
  * P(i,j) number of geodesics between i and j
  * P_{k}(i,j) number of geodesics between i and j that k lies on
  * Σ_{i, j ≠ k} = [Pk(i,j)/P(i,j)] / [(n-1)(n-2)/2]

## 2.4 Centrality Eigenvector Measures
* Eigenvector Centrality
  * Centrality is proportional to the sum of its neighbors centralities
  * C_i proportional to Σ_{j: friend of i}  C_j
  * C_j = a Σ_{j} g_{ij} C_{j}
  * This helps distinguish more “influential” nodes
* Prestige, Influence, Eigenvector based Centrality
  * Get value from connection to other butptopottoinal to their value
  * Self referential concept
  * C_{i}^{e}(g) = a Σ_{j} g_{ij} C_{j}^{e}(g)
    * Centrality is proportional to the summed centralities of neighbors
  * Ce(g) = a g Ce(g)
    * Ce(g) is an eigenvector: there are many possible solutions since there can be an “n” amount of equations and unknowns
    * Look for the largest eigenvalue: this will be nonnegative
    * Normalize entries to sum to one
* Bonacich Centrality
  * Give each node a base value (adi(g)) for some a>0, then add in all paths of length 1 from i to j multiplied with “b” and j’s base value. 
    * It continues until necessary, but every time you do it your “b” values will differ.
  * Cb(g) = ag1+ (bg * ag1) + (b2g2 * ag1)....... (continues until necessary)

## 2.5 Application Centrality Measures
* What affects Diffusion?
  * First contact points: examine the networks position of injection 
  * Points Matter
* Diffusion Centrality: DC_{i}(p,T)
  * How many nodes are informed
    * i is initially informed
    * Each informed node tell each of its neighbors with prob “p” in each period
    * Run for T amount of periods
      * Sort of like running a simulation
* DC(p, T) = Σ{t = 1...T}(pg)^{t1}
  * If T = 1: proportional to degree
  * If p < 1/λ1 (largest eigenvalue) and T is large, becomes closer to a Bonacich centrality
  * If p ≥ 1/λi (largest eigenvalue) and T is large, becomes closer to an eigenvector centrality

## 2.6 Random Networks
* Which Network form?
  * Random graph models - “How”
  * Economic/game theory models - “Why”
  * How all of these depend on context
* Static Random Networks
  * Useful Benchmark
    * component structure
    * diameter 
    * degree distribution
    * clustering 
  * Tools and methods
    * properties and thresholds
* Properties of Networks
  * Every network has some probability of forming
  * How do we make sense of that?
    * We examine what happens for “large” networks
* Specifying Properties:
  * G(N) = all the undirected networks on the set of nodes N
  * A property is a set A(N) is a subset of G(N)
  * A specification of which networks have that property
* Monotone Properties
  * A property A(N) is monotone if g in A(N) and g subset g’ in A(N)
  * All three of the previous properties are monotone
* Limiting Properties
  * In order to deduce thing about random networks, we often look at “large” networks, by examining limits
    * Examina sequence of E-R Poisson random networks, with probability p(n)

## 2.7 Random Networks: Thresholds and Phase Transitions
* Threshold Functions and Phase Transitions
  * t(n) is a threshold function for a monotone property A(N) if
    * Pr[A(N) | p(n)] -> 1 if p(n)/t(n) -> infinity 
    * Pr[A(N) | p(n)] -> 0 if p(n)/t(n) ->0
  * A phase transition occurs at t(n)
* Threshold for Poisson Random Networks
  * 1/n^2 : the network has some links (avg deg 1/n)
  * 1/n^{3/2}: the network has a component with at least three links (avg deg 1/n1/2)
  * 1/n: the network has a cycle, the network has a unique giant component: a component with at least na nodes some fixed a<1; (avg deg 1)
  * log(n)/n: the network is connected (avg deg log(n))

## 2.8 Threshold Theorem
* Theorem [Erdos and Renyi] A threshold function for the connectedness of a Poisson random network is t(n) = log (n)/n
  * if  p(n) is greater than log (n)/n then we are going to have a connected network
  * if p(n) os less than log (n)/n then the network is not going to be connected
* Proof of the Threshold Theorem
  * If p(n)/t(n) -> 0 then there will be isolated nodes with probability 1
  * If p(n)/t(n) -> infinity then there will not be any components of size less than n/2 with probability 1
  * Intuition for rest is that threshold for isolated node is the same as threshold for small component
* Useful Approximations
  * Exponential Function: ex = limn (1+x/n)n 
  * Taylor series approximation:
    * ex = 1 +x+x2/2!+x3/3!..... = Σ xn/n!

## 2.9 A Small World Models
* Other Static Models
  * Models to generate clustering
  * Models to generate other than Poisson degree distributions
    * Haf fat tails, can we generate models with different tails
* Models to fit data
* Rewired Lattice 
  * E-R model misses clustering
    * clustering  is on the order of p; going to 0 unless average degree is becoming infinite
    * Using ring lattice, we can pick links randomly and rewire them
      * Starts off with high clustering, but high diameter
      * As the links start to get rewired, the diameter becomes lower
      * Don't rewire to many because you want to keep high clustering

## Summary
* Networks based on characteristics: homophily 
* Local aspects, position: centrality measures
* Random Networks: sharp theresholsa, properties, phase transitions
* Small worlds: combining few random links give tree like structure necessary or storan paths without getting rid of local clustering
