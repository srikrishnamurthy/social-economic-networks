
## 5.1 Diffusion
* Networks and Behavior
  * How does network structure impact behavior?
  * Simple infections, contagion - diffusion
  * Opinions, information - learning
  * Choices, decisions - games on networks
* Diffusion
  * Ex: Disease
  * Ideas basic information (know or not know)
    * Buy a product or not (come back to complementaries later)
* S-Shape Adoptions
  * Diffusion over time and space
    * Griliches economic stor: variation in cost effectiveness by geography
  * Initial adopters
    * Who are they?
    * High degree?
    * Innovators?
  * Increase in speed
    * Word of mouth, observations of neighbors
  * Eventual slowdown
    * Saturation
* Questions:
  * Extent of diffusion?
  * How does it depend on the particulars of the process as well as the network?
  * Time patterns?  
    * S-shape?
  * Welfare analysis?

## 5.2 Bass Model
* Bass Model
  * A benchmark model with no explicit social structure
  * Two actions/states/behaviors 0 and 1
  * F(t) fraction of the population who have adopted action 1 at time t
  * p rate of spontaneous innovation/adoption
  * q rate of imitation of adoption
    * dF(t)/dt = (p+qF(t))(1-F(t)) → F(t) = (1-e-(p+q)t/q)
* Getting the S-Shape
  * Gives S-shape (if q>p) and tends to 1 in the limit
  * Initially only p matter, then q takes over
  * Eventually change slows as F(t) approaches 1
  * dF(t)/dt = (p+qF(t))(1-F(t))
    * When F(t) nears 1, dF(t)/dt = 0
    * When F(t) = 0, dF(t)/dt = p
    * When F(t) = ε, dF(t)/dt = (p + qε)(1-ε)
    * To get initial convexity: need (p + qε)(1-ε) > p
    * q (1-ε) > p so → q > p
* Beyond Bass: Component Structure
  * Reach of diffusion is bounded by the component structure
  * Some player or nodes are immune
  * Some links will fail to transmit
  * Answers question sof when get diffusion, and its extend/ neither answers by simple Bass

## 5.3 Diffusion on Random Networks
* Random Networks and Diffusion
  * Idea, disease, computer virus spread via connections of networks
  * Nodes are linked if one would “infect” the other
  * Will an infection take hold?
  * How many nodes/people will it reach?
* Questions:
  * When do we get diffusion?
  * What is the extent of diffusion?
  * How does it depend on the particulars of the princess as well as the network?
  * Who is likely to be infected earliest?
* Component Structure
  * Reach of contagion is determined by the component structure 
  * Some players or nodes are immune, Some links fail to transmit
    * What do components look alike of those who are susceptible and given links that work
* Extent of Diffusion
  * Get nontrivial diffusion if someone in the giant component is infected/adopts
  * Size of the giant component determined likelihood of diffusion and its extent
  * Random network models allow for giant component calculations
    * Simple example of such a calculation 
    * Work with E-R random network
    * How big is the giant component?

## 5.4 Giant Component Poisson Case
* Calculating the Size of the Giant Component
  * q is fraction of nodes in largest component
  * Look at any node: chance it is in the giant component is q
  * Chance that this node is outside of the giant component is the chance that all of its neighbors are outside of the giant component
  * Probability that a node is outside of the giant component = 1-q
  * This is equal to the probability that all of its neighbors are outside
  * This finally leads to (1-q)d where d is the node’s degree
* Giant Component Size
  * So, probability 1-q that a node is  outside of that giant component is
    * 1-q = Σ(1-q)d P(d)
  * Where P(d) is the chance that the node has “d” neighbors
  * Then solve for q
  * SOLVE: 1-q = Σ(1-q)d P(d)
  * WHEN: P(d) = [(n-1)d/d!] pde-(n-1)p
  * SO: 1-q = e-(n-1)p Σ [(1-q)(n-1)p]d /d!
* Who is infected?
  * Probability of being in the giant component is” 1-(1-q)d ; increasing in “d”
  * More connected, more likely to be infected (at any point in time)
* Extensions
  * Immunity: delete a fraction of the nodes and study the giant component on remaining nodes
  * Probabilistic Infection: Random infection → have some links fail, just to lower “p”
* Contagion with Immunity and Link Failure
  * Some node is initially exposed to infection 
  * π of the nodes are immune naturally 
  * only some links result in contagion - fraction f
  * What is the extent of the infection?
  * Consider a random network on “n” nodes
  * Delete fraction of π of the nodes
  * Delete fraction f of the links
  * If starts at a node in giant component of the remaining network is the extent of the infection; otherwise negligible
  * Let q be the fraction of nodes of the remaining network in its giant component
  * q(1-π) is the probability of a nontrivial contagion
  * Conditional on a contagion it infects q(1-π) of the original nodes
    * q solves -log(1-q)/q = (n-1)p(1-π)f
* Implications
  * Infection can fail if π is high enough or “f” or “p” are low enough
  * High π - immunization, low virulence
  * Low f - lowe contagiousness
  * Low p - low contact among population

## 5.5 - 5.8 SIS Model
* SIS Model
  * An extensively studied model in epidemiology
  * Allows nodes to change behaviors back and forth over time
  * Model of catching some recurring diseases (who vote for ect.)
  * Nodes are infected or susceptible 
  * Probability that get infected iss proportional to number of infected neighbors with rate v>0, plus spontaneous ε
  * Get well randomly in any period at rate δ >0
  * Let p be the present infected
  * Start with benchmark where all player mix with even probability
  * Randomly meet an individual each period
  * Large Markov chain
  * Steady state mean field: dp/dt = 0
* Mean Field
  * dp/dt = (1-p)(vp+ε) -pδ = 0 → p = [(v-δ-ε) + ((v-δ-ε)2 + 4 εv)1/2]/2v
  * “Mean-Field” drop ε
    * dp/dt = (1-p)vp - pδ → (1-p)vp - pδ = 0
    * Two solutions:
      * p = 1-δ/v (if > 0)
      * p = 0
    * Implications
      * p = 1-δ/v
      * If δ > v then recover faster than get sick, no infection stays
      * Otherwise, infection stays at some level for low recovery  rates can lead to large infections
    * Where is the network?
      * So far uniformly random interaction
      * Mission heterogeneity in degree
      * missing local patterns
      * We can at least address the first concern…
  * Explore Degree Distribution Influence
    * Random matching with di matched for node i
    * p(d) fraction of nodes for degree d infected 
    * θ fraction of randomly chosen neighbors infected
  * Chance that meet an infected node
    * P(d) of nodes that have “d” meetings
    * More likely to meet someone who has high “d”
    * Likelihood of meeting node of degree “d” is → P(d)d/E[d]
    * So likelihood of meeting infected node is → θ = Σ p(d) P(d)d/E[d]
  * Mean Field: Pastor-Satorras and Vespignani
    * θ = Σ p(d) P(d)d/E[d] fraction of infected neighbors/random partners
    * Steady State: for each “d”
      * 0 = dp(d)/dt = (1-p(d))vθd - p(d)δ
    * Solving:
      * Steady state: for each “d”
        * 0 = dp(d)/dt = (1-p(d))vθd - p(d)δ
      * p(d) = λθd/(λθd +1), where λ = v/δ
      * θ = Σ p(d)P(d)d/E[d] → Σ p(d)λθd2/[(λθd +1) E[d]]
      * Steady state inflation rate of people you meet is the solution to:
        * Θ = H(θ) = Σ p(d)λθd2/[(λθd +1) E[d]]

## 5.9 Diffusion Summary
* Lessons
  * Thresholds/”Phase Transitions”:
    * Low density no contagion
    * middle density some probability of infection, part of population infected - reach most of population even with average degree around 3
    * High density sure infection and all infected
    * Degree affects who is infected and when
  * General Points
    * Diffusion modeling
      * Important to model both information and peer effects:
        * Not simply an infection model: nonparticipants communicate - distinguish such models from epidemiology
    * Need more studies that identify the details of what matter in interactions: information, learning, complementarities/substitution, and peer pressure 
* Diffusion
  * Network structure matters
  * Tractable, and  simulations can go a long way to offering predictions
    * Experiment with changes in network structure

## Summary
* Adoption curves: s-shapes of diffusion 
  * S-shape: combination of imitation/complementaries and eventual saturation
* Initial contagion:
  * Depends on density and variance: high degree nodes serve as hubs and enable diffusion
* Extent of diffusion
  * Relates to component structure, density - beyond one friend (homophily)
* Diffusion modeling
  * Can help dissect peer effects
  * Underlies many relation : shed light on financial contagions
