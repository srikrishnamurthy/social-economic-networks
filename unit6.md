## 6.1 Learning
* Bayesian Learning
  * Will society converge 
  * Will they aggregate information properly?
* [Bala Goyal 98]
  * N players in an undirected component “g”
  * Choose action A or B each period
  * A pays 1 for sure, B pays 2 with probability p and 0 with probability 1-p.
* Learning
  * Each period gets a payoff based on choice 
  * Also observe neighbors’ choices
  * Maximize discounder stream of payoffs
    * E[Σtδtπit]
  * p is unknown take on finite set of values
* Proposition:
  * If o is not exactly ½, then with probability 1 there is a time such that all agents in a given component play just one action (and all play the same action)
* In continuation of [Bala Goyal 98]
  * If B is the right action then play the right action if converge to it, bu it might not
  * If A is the right action, then must converge to the right action
* Probability of Converging to “correct” action
  * Arbitrary high if each action has some agen who initially has arbitrarily high prior that the action is the best one
* Conclusions
  * Consensus action chosen
  * Not necessarily consensus belief
* Limitations 
  * Homogeneity of action and payoffs across players 
  * Repacted actions over time
  * Sationarity
  * Networks are not playing a major role here!

## 6.2 DeGroot Model
* Network Structure and Learning
  * Repeated communication
  * Information come only one
  * See house information disseminates
  * Who has influence, convergence speed, network structure impact
* Bounded Rationality Model
  * Repeatedly average belief of self with neighbors
  * Non _bayesian if wrights do not adjust over time
  * Can under wight neighbors (just as in experiments)
* DeGroot (1974) Social Interaction Model
  * Individuals {1,...., n}
  * T weighted directed network, stochastic matrix
  * Start with belief, attitude, ect bi(0) in [0,1]
    * Can also have these be vectors
  * Updating: bi(t) = Σj tijbj(t-1)
* Other interpretations
  * Social influence on actions
  * Random action (Markov process)
  * Ex: Page ranks networks

## 6.3 - 6.4 Convergence in DeGroot Model 1342
* Convergence
  * T converges if lim Tt b exists for all b
  * T is aperiodic if the greatest common divisor of its cycle length is one
* Theorem
  * Suppose T is strongly connected,
  * T is convergent if and only if it is aperiodic
  * T is convergent if and only if : lim Tt = (1,1,.....,1)Ts eigenvalue 1

## 6.5 - 6.6 Influence
* Consensus
  * Converge to (normalized) eigenvector weight sum of original beliefs
* What are Limiting Beliefs?
  * When a group reaches consensus, what is it?
  * Who are the influential agent in term sof setting the limiting belief
  * Must be that rows of Tt converge to same thing since belief coverage to same thing or all initial vectors
* Influence Measure
  * What so rows of Tt converge to?
  * Look for a row vector s indicating the relative influence each agent has - limit belief is “s” “b”
  * So, s = s*T : s is the left unit eigenvector
* Who has influence
  * Si = ΣjTjisj
  * High influence from being paid attention to by people with high influence
  * Power measures → google page ranks
  * Related to eigenvector centrality

## 6.7 Information Aggregation
* Uncertainty Structure
  * Suppose tru state is μ
  * Agent i sees bi(0) = μ + εi
  * Εi has 0 mean and finite variance, bounded below and above
  * Signal distributions may differ across agents, but are independent conditional on μ
* Wise Crowds
  * Consider large societies
  * If they pooled their information they would have an accurate estimation of μ
  * For what sequence of society does Prob lim [| bn(t)- μ| > δ] → n 0 for all δ?
* A weak Law of Large Numbers
  * Let εi’s be independent,zero mean, and each have finite variance (bounded below) Then:
    * plim Σ sin εi = 0 iff maxi sin → 0
  * Wise crowds iff max influence vanishes
* Reciprocal Attention 
  * Suppose that T is column crochastic (so each agent receives weight one). Then s = (1/n, ...1/n) is a unit lhs eigenvector, and so “T” is wise
  * So reciprocal trust implies wisdom
  * But this a very strong connection
* No Opinion Leaders
  * Si = ΣjTjisj
  * If there is some “i” with Tji > a > 0 for all “j”, then si > a
  * So clearly cannot have too strong an “opinion leader”

## Summary 
* Convergence/Consensus if and only if aperiodicity 
* Limiting influence related to eigenvectors and weights from influential neighbors
* Wise Crowds: nobody retains too much influence
* Learning Models
  * Bayesian is computationally demanding in network settings
  * Restricted Bayesian give consensus network not much of a role
  * DeGroot and other myopic models bring network into play
  * Can reach consensus, can be wise
  * Influence and speed are tractable….

## Wrap Up
* Rational/Bayesian learning: complex but lead  to consensu action if: homogeneous, repeated observations, stationary
* Network Structure: DeGroot Model
* tractable repeated discussions
  * Eventual consensus for many structure (speed depends on homophily)
  * Influence depends on how much listened to rationalize eigenvector-style centrality measures
  * Accurate brief depend on balance
