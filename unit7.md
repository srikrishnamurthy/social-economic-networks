## 7.1 Games on Networks Intro
* Games on Networks
  * Decisions to be made
    * Not just diffusion 
    * Not just updating
  * There are complementaires: people care about other people and things
  * “Strategic” Interplay
    * Interdependencies
  * Players on a network - explicitly modeled
  * Care about the actions of its neighbors
  * Early literature: How complex is the computation of equilibrium in worse case scenario
  * Second Branch: what can we say about behavior and how it relates to network structure
* Canonical Special Case
  * Each player chooses action xi in {0,1}
  * Payoff will depend on
    * How many neighbors choose each action
    * How many neighbors a player has
* Definitions
  * Considered cases where “i’s” payoff is
    * udi(xi,,mNi)
  * Depends only on di(g) and mNi(g)- the number of neighbors “i” choosing 1
* Example: Simple Complement
  * Agent “i” is willing to choose 1 if and only if  at least t neighbors do:
    * Payoff action 0: udi(0,mNi) = 0
    * Payoff action 1: udi(1,mNi) = -t + mNi

## 7.2 Games on Networks, Strategic Complements and Substitute
* Complements/Substitutes
  * strategic complements -- for all d, m≥m
    * Increasing differences:
      * ud(1,m)-ud (0,m) ≥ ud (1,m’) - ud (0,m’)
  * strategic substitutes -- for all d, m ≥ m’
    * Decreasing differences:
      * ud(1,m)-ud (0,m) ≤ ud (1,m’) - ud (0,m’)
* Externalities
  * Others’ behaviors affect my utility/welfare
  * Others’ behaviors affect my decisions, actions, consumptions, options…
    * Others’ actions affect the relative payoffs to my
* (Strategic) Complements/Substitutes
  * Complements: Choice to take an action by my friends increases my relative payoff to taking that action 
  * Substitutes: Choice to take an action by my friends decreases my relative payoff to taking that action
* Equilibrium
  * Nash equilibrium: Every player’s action is optimal for that player given the action of others
  * Often look for pure strategy equilibria
  * May require some mixing
* Maximal Independent Set
  * Independent Set: a set S of nodes such that no two nodes in S are linked
  * Maximal: every ode in N is either in S or linked to a node S
* Useful Observation
  * Complements: there is threshold t(d), such that “i” prefers 1 if mNi > t(d) and 0 if mNi< t(d)
  * Substitutes: there is a threshold t(d), such that “i” prefers 1 id mNi < t(d) and 0 if mNi > t(d)
  * Can be indifferent at the threshold

## 7.3 Structure of Equilibria in Games on Networks
* Complete Lattice
  * Complete Lattice: for every set of equilibria X 
    * there exists an equilibrium x’ such that x’ ≥ x for all x in X 
    * There exists an equilibrium x’’ such that x’’≤ x for all x in X
  * Proposition
    * In a game of strategic complements where the individual star  test are complete lattices:
      * The set of pure strategy equilibria are a (nonempty) complete lattice
* Contrast: Compliments and Substitutes
  * In a game of complements: pure strategy equilibria are nonempty complete lattice
  * In a game of strategic substitutes:
    * Best shot game: pure strategy equilibria exist and are related to maximal independent sets
    * Others: pure strategy may not exist, but mixed will (with finite action spaces)
    * Equilibria usually do not form a lattice

## 7.4 Multiple Equilibria in Games on Networks
* When can multiple actions be sustained
  * Morris(2000) → coordination game
    * Care only about fraction of neighbors
    * Prefer to take action 1 if fraction q or more take 1
* Equilibrium Structure
  * Let S be the group that takes action 1
    * Each “i” in S must have fraction of at least  neighbors in S
    * Each “i‘ not in S must have a fraction of at least 1-q neighbors outside of S
* Cohesion 
  * A group s is r-cohesive relative to g if
    * Mini in S |{j in Ni(g) and S}|/di(g) ≥ r
  * At least a fraction r of each member of S’s neighbors are in S
  * Cohesiveness of S is mini in S |{j in Ni(g) and S}|/di(g) 
* Equilibria where both strategies are played
  * Morris (2000): there exists a pure strategy equilibrium where both actions are played if and only if there is a group S that is at least q cohesive and such that its complement is at least 1-q cohesive

## 7.8 Summary
* Behavior and network structure
  * complements provide nice lattice structure to equilibria
  * substitutes less structured (except best-shot games)
  * comparative statics: higher density
  * more activity with complements…
  * multiple behaviors related to homophily, cohesion
  * splits in network allow for different behaviors on different parts of network
  * linear-quadratic games: intensity of behavior depends on position, relates to centrality measures, tractable model 

## Summary
* Summary Games On Networks
  * Strategic Complements and Substitutes exhibit very different patterns
  * Position Matters
    * More connect take
    * higher  actions in compliments (and earlier)
    * Lower actions in substitutes
  * Structure Matters
    * Some networks lead to diffusion of behavior other do not
    * Homophilly/cohesion is a critical determinant of diversity of actions
* Whither Now?
  * Bridging random/economic models of formation 
  * New statistical models of network formation 
  * Relate Networks to outcomes
    * Applications: labor, knowledge, mobility, voting, trade, collaboration, crime, www, risk sharing, ... 
    * markets, international trade, growth... .  
  * Co-evolution networks and behavior 
  * Empirical/Experimental 
  * enrich  modeling of social  interactions from a structural perspective - fit network models to data, test network models 
  * Foundations and Tools: centrality, power, allocation rules, community structures, ... 
