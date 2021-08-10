# What's a schema?

#schemata

What are [[schemata]] or [[schema]]? 

## Perceptual Schemata

[[Perceptual-schemata]] refer to temporally extended Perceptual. Perceptual schemata describe how state-components evolve over time. Assume a factored state with $N$ components $\mathcal{S}= \{\mathcal{S}_{t,i}\}_{i=1}^{N}$. A Perceptual Schema $D_i = (p_i, \mathcal{I}_i, \beta_i)$ is composed of

* A subset of state-components $\mathcal{C}_{i} \subseteq \mathcal{S}$: $\mathcal{C}_{i} = \{\mathcal{S}_{t,j}\}_{j=1}^{n_i}$
* a transition function $p_i: \mathcal{C}_{t,i} \times \mathcal{A}_t \rightarrow \mathcal{C}_{t+1, i}$
* an initiation set $\mathcal{I}_i$ that defines the states where the transition function occurs
* a termination condition $\beta_i : \mathcal{S}_t \rightarrow [0,1]$,
* Uncertain: $s$ lives $\mathbb{R}^d$. Each factor lies in a subspace of $s$?

[[Perceptual-schemata-description]]




### Why are Perceptual-schemata useful?

1. Perceptual-schemata are useful for modeling the environment and recognizing temporal [[fragments]] of features? These temporal fragments can be recomposed to enable [[systematic-generalization]]. Examples of comp\osing temporal fragments:
   1. Can compose in sequence. Possible examples: keybox task, levels in game, etc.
   2. Can compose in space-time. Consider seeing multiple ballerinas dancing in their own stereotyped pattern. You can see them as a composition of Perceptual-schemata. [[representation-learning-utility]]

1. Enable evolves pieces of state-independently
2. Enables learning a smaller model of the environment
1. Allows us to reduce the kolgorov complexity (use a much smaller, much more compact model to describe the world)




### Open questions
#open-questions:
1. When are Perceptual-schemata useful for modeling the environment?
2. When are Perceptual-schemata useful for recognizing temporal fragments of features?
   1. When is it useful to recognize a temporal fragment of features? 
3. can schemata have their own value function? Where do rewards come into play? They have to if they have their own model, right?
---






## Relevant Literature
### Brain Science
1. [Clearly shows relation of schemata to options](https://www.cnbc.cmu.edu/~plaut/papers/pdf/BotvinickPlaut04PR.seq-action.pdf)
2. [Compares associative vs non-associative](https://link.springer.com/content/pdf/10.3758/BF03329880.pdf)
3. [Show that if "schema" present, enables one-trial learning in rats](https://pubmed.ncbi.nlm.nih.gov/17412951/), i.e. partial explanation to rapid adaptation
4. [Much of Arbib's references indicate the formalism I use](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.470.6492&rep=rep1&type=pdf)
5. [Good paper to plan writing the paper](https://psyarxiv.com/uz5wp/): Understanding exploration in humans and machines by formalizing the function of curiosity
6. [Survey of role of schemata in cognitive neuroscience of action](https://psycnet.apa.org/record/1997-97298-000) - The cognitive neuroscience of action
7. [Notes on Schema Theory from MIT class](http://web.mit.edu/pankin/www/Schema_Theory_and_Concept_Formation.pdf)
8. Look up "Review on schemata"
9. Look up schemata + bayesian networks


### AI
2. Seems very related to object-oriented MDPS... need to figure this out.
3. A lot of people in robotics have adapted the "schema" terminology. e.g. "Integrating behavioral, perceptual, and world knowledge in reactive navigation"

---

## Todo

[ ] read through literature and see when schema/Perceptual are used
[ ] in literature, schemata include both a transition function **and** a policy
