# 4.0 Guiding Questions
* Which networks are best for society?
* Which networks are formed by the agents?

## 4.1 Strategic Network Formation
* Economic Game Theoretic Models of Network Formation
  * Costs and benefits for each agent associated with each network
  * Agents choose links
    * Contrast incentives and social efficiency 
* Modeling Choices
  * How should we model incentives to form and sever links?
    * Is consensus needed (undirected/directed)?
    * Can they coordinate changes in the network?
    * Is the process dynamic or static?
    * How sophisticated are agents?
    * What do they know when making a decision?
    * Do they make errors?
    * What happens on the network?
    * Can they compensate each other for relationships?
    * Are links adjustable in intensity?
* Some Questions
  * Which networks are likely to form?
  * Are some more stable than others to various perturbations?
  * Are the networks that efficient?
  * How addicted are they if they are not efficient?
  * Can such models provide insight into observed characteristics of networks?
* Economic Analysis [Jackson Wolinsky 96]
  * ui(g) - payoff to i if the network is g
  * Undirected network formation
  * Connections to Model:
    * 0≤δ≤1 a benefit parameter for i from connection between i and j
    * 0≤cij cost to i of link to j
    * l(i,j) shortest path length between i,j
    * ui(g) = Σδl(i,j)-  Σj in N(g)cij
* Symmetric Version
  * Benefit from a friends is δ<1
  * Benefit from a friend of a is is δ2
  * Cost of a link is c>0

## 4.2 Pairwise Stability and Efficiency
* Modeling Incentives/ Equilibrium
  * What if models as a game where each agent announces who they wish to link to and a link forms if and only if both agents name each other?
  * Nash equilibrium: ni agent can gain from changing his/her action
* Modeling Incentives: Pairwise Stability
  * No agents gains from severing a link - relationships must be beneficial to be maintained
  * No two agents both gain from adding a link - Beneficial relationships are pursued when available
* Pairwise Stability
  * ui(g) ≥ ui(g-ij) for i and ij in g
    * No agents gain from severing a link
  * ui(g+ij) > ui(g) implies uj(g+ij) < uj(g) for ij ij not in g
    * No two agents boht gain from adding a link (at least one strictly)
    * Weak concept, but often narrows thighs down
* Efficiency 
  * Pareto efficient g: there does not exist g’ s.t
    * ui(g’) ≥ ui(g) for all i, strict for some
  * Efficient g (pareto if transfers):
  * G maximizes Σ ui(g’)

## 4.3 Connections Model
* Reference back to Economic Analysis [Jackson Wolinsky 96]
* Efficient Networks in the Symmetric Connection Model
  * Low cost c<  δ-  δ2
    * Complete network is uniquely efficient
  * Medium cost: δ-  δ2 < c < δ + (n-2)δ2/2
    * Star networks with all agents are uniquely efficient
  * High cost: δ +(n-2)δ2/2 < c
    * Empty network s uniquely efficient


## 4.5 Pairwise Stability in the Connections Models 
* Pairwise Stability
  * Low cost c<  δ-  δ2
    * Complete network is pairwise stable 
  * Medium / low cost: δ-  δ2 < c < δ 
    * Star networks is pairwise stable
    * Others are also pairwise stable
  * Medium / high cost: δ-  δ2 < c < δ + (n-2)δ2/2
    * Star networks is not pairwise stable (no loose ends)
    * Empty network s uniquely efficient
  * High cost δ +(n-2)δ2/2 < c
    * Empty network is pairwise stable
* Inefficiency
  * Payoff to center:
    * 3δ - 3c
  * Not pairwise stable if
    * δ<c
  * Overall payoff: 6δ + 6δ2 - 6c
    * Peripheral player gain indirect benefits
    * Center player does not account for them

## 4.6 Externalities and that Co Author Model
* Externalities
  * Positive
    * uk(g+ij) ≥ uk(g) if ij not ing for every k ≠ i,j
  * Negative
    * uk(g+ij) ≤ uk(g) if ij not in g for every k ≠ i,j
  * Inefficiency in connections model due to positive externalities - “no loose ends”
  * What about models with negative externalities?
* Example: “Coauthor” [Jackson Wolinsky 96]
  * Agents get value from research collaboration
    * Value for each relationships depends on time each puts into it
    * Plu an interaction term, which is product of the time spent
  * ui(g) = Σj: ij in g[1/di +1/dj + 1/(didj)] → 1+ Σj: ij in g[1/dj + 1/(didj)] 
  * No direct costs to links
  * N is even 
    * Efficient networks: pairs
    * Pairwise stable networks consist of complete connect connects, each a different size, one had more than the square of the number of nodes in the other
    * By adding a link, dilute existing synergies, only add if new coathour bring comparable worth
* Stable and Efficient only condice in special cases
  * Can transfers help in other cases?
  * What can we say about when transfers improve efficiency?
  * Are transfers in players’ interests?

## 4.7 Network Formations and Transfers
* Strategic Formation Models:
  * Saw conflict between stability and efficiency 
  * Can Transfers help?
  * Modeling stability and Dynamics
    * Refining pairwise stability
    * Dynamic process
    * Forward looking behavior
  * Directed Networks
  * Fitting such models 
    * Introduce heterogeneity 
    * Introduce randomness - meeting process
* What are transfers?
  * Outside intervention, taxing or subsidizing relationships - e.g gvt support of R and D relationships 
  * Bargaining among the individual involved in the relationships
  * Favors exchanges among friends
* Modeling Transfers
  * Change utilities from uI(g) to ui(g) + ti(g)
  * E.g., peripheral player pay center of star in connections model to maintain connections
* Egalitarian Transfers
  * Set ti(g) = Σj uj(g)/n - ui(g)
  * Then ui(g) + ti(g) = Σj uj(g)/n
    * This now shows that every agent has societal incentives
* Transfers can Fail 
  * Put in some basic requirements on transfers
    * Completely isolated nodes that generate no value get 0
    * Nodes that are completely interchangeable get same transfers
* Intuition
  * CoaseL without frictions, transfers can solve inefficiencies 
  * What is special here?
  * Combination of multiple externalities that all need to be handled at once.
* Efficiency and Stability
  * Tension due to externalities, either positive or negative or mixed
  * Network setting introduced interesting problem: not entirely correctable with bargain or transfers
* Efficient Networks take some simple firms in a variety of models 
* Effient networks are pairwise stable need not coincide
* Transfers may help, but not alway without violating some basic conditions

## 4.8 Heterogeneity on Strategic Models
* Enriching Such Models
  * Costs depend on geography y and characteristics of nodes
    * Easier to be friends with neighbors
    * Easier to relate to people with similar background
  * Benefits depend on characteristics of nodes
    * synergies  from working  together, triaging, sharing risk, exchanging favors
    * Complementaries: benefits from diversity
* Can economic models match observables?
  * Small worlds derived from costs/benefits
    * Low costs to local links - high clustering
    * High value to distance connection - low diameter
    * High cost of distance connection - few distant links
  * Ex: Islands connections model [JR-04]
    * J players live on an island, K islands
    * Cost c of links to layer on the island
    * Cost C>c of link to player on another island
    * Results:
      * High clustering with islands, few links across
      * Small distances
      * Look at image above 
  * Proposition JR04
    * Truncate connections:
      * ui(g) = Σj: l(i,j)≤D δl(i,j) - di(g)c
    * If c < δ - δ2 and C < δ +(J -1)δ2 then 
      * Players on each island form a clique
      * Diameter is bounded by D+1
      * δ-δ3 < C implies a lower bound on individual clustering is (J-1)(J-2)(J2K2)
* Strategic Formation
  * Efficient networks and stable Networks need to coidenide
  * Need not coincide even when transfers are possible, and with complete information
  * Depends on 
    * Setting
    * Restriction on transfers, endogenous transfers
    * Forward looking, errors

* Challenges to an Economic Approach 
  * Stark (overly regular) network structures emerge
    * Need some heterogeneity
    * Simulation help fitting
* Over-emphasize choice versus chance for some (especially large) applications
* How to identify payoff structure in applications
  * Relating network structure and costumes: payoffs
* Models that marry strategic with random are needed
  * Weakness of Random are Strengths of Economic approach, and vice versa
  * Mixed Models
    * Allow for welfare/ efficiency analysis
    * Take model to data and fit observed networks
    * Do so across applications

## Summary
* Strategic models: choice based formation, welfare analysis 
* Formation:
  * Pairwise stability
* Welfare
  * Pareto efficiency, utilitarian measure/efficiency 
* Tension: stable and efficient networks need not coincide 
  * Positive externalities - under-connected
  * Negative externalities - over connected
  * Transfers cannot always help 
* Small worlds: low costs of local links gives clustering 
  * High benefits from distance links give short paths
* Adding heterogeneity can lead to estimable models
