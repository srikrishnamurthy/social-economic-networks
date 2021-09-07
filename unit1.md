
## 1.0 Guiding Questions:
* What do we know about networks?
* How do networks form? Do the “right” networks form?
* How do networks influence behavior? (And how does behavior influence networks)

## 1.1 Introduction:

* Why study networks?
  * Many economic, political, and social interaction are shaped by the local structure of relationships
    * EX: Trades of goods and services, transmission of viruses, and choices of behavior
  * Social Networks influence human behavior
    * EX: crime, employment and voting
    * Networks display heterogeneity, but they have enough underlying structure (they are connected enough) to create models
* Why do we care about modeling things?
  * They give us perspective into why we see certain developments
  * They allow for comparative statics
    * EX: How does the structure of the model changes based on density
  * Help make predictions out of samples
    * EX: Prediction about new policy, example: new vaccine
* It allow for statistical estimation
  * Is there clustering on a local level or at random?

## 1.2 Examples and Challenges:

* Examples:
  * Example #1: Padgett and Ansell’s (1993) Data (from Kent 1978) Florentine Marriages 1430’s.
    * There are a series of different families and before the period of 1430’s there was an Oligarchy (when aristocratic families rose to power). During this time, the Medici were the ones who rose to power
    * Numbers: 
      * Medici -> .522  
      * Guadagni ->  .255 
      * Strozzi -> .104
      * Given any two points, A and B, on a network, the shortest path from point a to point be must be through point C
        * The percentages represent the amount of points that must go through point C in a network to get the shortest path to another point.
        * Point C is a centralized point
        * In this example you can take the Ridolfi’s as point A and the Salviati’s as point B. In order to get to point A to B in the shortest way, they must pass through point C, who are the Medici.
  * Example #2: Elliot, Golub, Jackson (2012) National Debt of Six major European Countries
    * Shows us how shocks (changes) in one country can affect another country: transmission of financial stress
    * Number represent the percentage of a countries debt that is held by another country determined by which way the arrow is pointing

* What do we know?
  * Networks play a role in many settings
    * Ex: Jobs, Contacts, Crime, and Trade
* Network position and structure matters
  * Example #1 Medici were not wealthy or strong politically, but they were the most central (C is the centralized point)
* “Social” Networks have special characteristics
  * Small worlds and degree distributions
* Networks are applicable in all settings

## 1.3 Definitions and Notations

* Types of Patterns in Networks:
  * Global Patterns of Networks:
    * Big Picture Networks
    * Path Lengths: How far is it from one node to the other
    * EX: How well connected are people, are some people the hubs, where they are connect to a lot of people or are some people more closed off  and not connected to many people
  * Segregation Patterns:
    * Nodes will have characteristics
      * EX: Age or Gender
      * Will nodes be separated if they are from different types
* Local Patterns
  * Are the node in a network tightly clustered
    * If I'm connected to someone and he is connected to someone else. I am connected to third person
    * zooming in on particular parts
* Positions in Networks
  * How central is a somebody (a point)
  * How influential is this person
* Representing Networks
  * N = {1,..., n}: nodes, vertices, and players
  * Basic way of representing a network is an Adjacency Matrix 
    * g in {0,1}^{n*n}
  * A matrix of zeros and ones 
  * Indicates weather 2 nodes are linked (if it is equal to 1 there is a relationship)
    * g_{xy}  = 1, where x and and y are nodes
  * Alternative Notation: xy in g -> a link between i and j
  * Network(N, g): a pair of a set of nodes
* Basic Definitions
  * Walk from i_1 to i_k: a sequence of nodes and links till K. A walk in a network from one node to another is a sequence of links that takes you from the first node till the last node.
    * It is convenient to represent as a corresponding sequence of nodes, such that the sequence is in the network
  * Path is a walk where each node is distinct (the same node does not repeat)
  * Cycle is a walk where i_1 = i_k (the first node is the same as the last one)
  * Geodesic is the shortest path between two nodes (smallest number of links between the 2 nodes)
* Counting Walks:
  * If you are given a network g, and wish to find the number of walks “w” between two points, you must take the matrix model of g and raise it to the power of w:  gw
* Component Structure
  * (N, g) is connected if there is a path between every two nodes
  * Component: Maximal connected subgraph
    * Take (N’, g’): This is a subset of (N, g)
    * If (N, g) is connected, then (N’, g’) is also connected
    * i in N’ and ij in g implies j in N’ and ij in g’

## 1.4 - 1.7 Diameter of Networks
* Diameter and Average Path Length 
  * How close nodes are to each other
  * How long does it take to reach a node
  * How fast will information spread
  * Diameter: largest geodesic (largest shortest path)
    * If not connected, of largest component
  * Average Path Length
    * Less prone to outliers
    * Average geodesic of the network
* Neighborhood and Degree
  * Neighborhood : Ni(g) = {j| ij in g}
    * ii not in g (node is not connected to itself)
  * Degree: di = #Ni(g)
    * How many neighbors are in g
* Random Graphs
  * Start with n nodes
  * Each link is formed independently with some probability p 
    * “G(n,p)”
    * Used as benchmark to compare with other networks to see if the network is random or if it is systematic
* Sequences of Networks
  * Links are dense enough so that network is connected almost surely
    * d(n) ≥ (1+ε) log(n) some ε>0
  * d(n)/n -> 0:
    * Network is not too complete
* Theorem on Network Structure
  * If d(n) ≥ (1+ε) log(n) some ε>0 and d(n)/n -> 0
    * Then for a large n, average path length and diameter are approximately proportional  to log(n)/log(d)
    * Same for diameter (reference to picture)
    * Density: Average Path Length -> as the density of the network changes, so does the average path length

## 1.8 Degree Distributions 
* Degree Distribution G(n,p)
  * The probability that a node has “d” links is binomial
    * [(n-1)!/(d!(b-d-1)!)]p^{d}(1-p)^{n-d-1}
* Large n, small p this is approximately a Poisson distribution
  * [(n-1)^{d}/d!]p^{d}e^{-(n-1)p}
* Distribution of links per node
  * More high and low degree nodes than predicted at random	
  * Fat tails: lower extreme and upper extremes are over represented
    * EX: Network of Citations: If there was a network regrading the number of citations that were used, there were many zero citations (lower extreme) and many with high number of citations (higher extreme)
* Scale Free Distributions
  * Scale Free Distribution: P(d) = cd^{-a}
* Take log of this:
  * log (p(d)) = log (c)-a log(d)

## 1.9 Clustering
* What fraction of my friends are friends with each other
* Calculating Clustering (frequency of relationship between 2 points (k and j) who are connected to a third point (i))): Cli(g) = #{kj in g | k, j in Ni(g)}/#{kj | k, j in Ni(g)}
  * Average Clustering: Clavg (g) = ΣiCli(g)/n
  * Overall Clustering: Cli(g) = Σi #{kj in g | k, j in Ni(g)}/ Σi #{kj | k, j in Ni(g)} (combined the two formulas above)
* Clustering in a Poisson Random Network
  * Average and Overall clustering tend to 0, if max degree is bounded and network becomes large:
    * Σi #{kj in g | k, j in Ni(g)}/ Σi #{kj | k, j in Ni(g)} -> is “p”
  * If degree is bounded, then p(n-1) is bounded
  * So “p” goes towards zero and “n” grows

## Summary:
* Many relationship are “networked ” and understanding network structure can help understand behavior and outcomes
* Networks are complex, but can be particle described by some  characteristics
  * Degree distributions
  * Clustering 
  * Diameter
* Tree-like structures are generated by random links lead to short paths 
* It is observed that networks are more clustered than random
