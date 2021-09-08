---
tags: [schemata, dynamics, adaptation, planning, model-complexity]
aliases: [Perceptual Schemata, Schemata, perceptual_schemata]
---

## Perceptual Schemata

Perceptual schemata refer to temporally extended Perceptual. Perceptual schemata describe how state-components evolve over time. Assume a factored state with $N$ components $\mathcal{S}= \{\mathcal{S}_{t,i}\}_{i=1}^{N}$. A Perceptual Schema $D_i = (p_i, \mathcal{I}_i, \beta_i)$ is composed of

* A subset of state-components $\mathcal{C}_{i} \subseteq \mathcal{S}$: $\mathcal{C}_{i} = \{\mathcal{S}_{t,j}\}_{j=1}^{n_i}$
* a transition function $p_i: \mathcal{C}_{t,i} \times \mathcal{A}_t \rightarrow \mathcal{C}_{t+1, i}$
* an initiation set $\mathcal{I}_i$ that defines the states where the transition function occurs
* a termination condition $\beta_i : \mathcal{S}_t \rightarrow [0,1]$,
* Uncertain: $s$ lives $\mathbb{R}^d$. Each factor lies in a subspace of $s$?


## Deep RL Equations



### Why are Perceptual-schemata useful?

1. Perceptual-schemata are useful for modeling the environment and recognizing temporal [[fragments]] of features? These temporal fragments can be recomposed to enable [[systematic-generalization]]. Examples of composing temporal fragments:
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

### Examples in literature:

- Google Search: "learning to represent state with perceptual schemata"
- Arbib textbook: [Computing the Brain: A Guide to Neuroinformatics](https://books.google.com/books?id=EOQG_2Q4lUQC&pg=PA65&lpg=PA65&dq=learning+to+represent+state+with+perceptual+schemata&source=bl&ots=5Yht8cY2ok&sig=ACfU3U3je0dkGrAx-_TEcfaCvGiTDvxfEQ&hl=en&sa=X&sqi=2&ved=2ahUKEwi-8NWQuLbyAhUoG6YKHQp-CHAQ6AF6BAgaEAM#v=onepage&q=learning%20to%20represent%20state%20with%20perceptual%20schemata&f=false)
- From Natural to Artificial Neural Computation: [Schema Based Learning Underpinnings](https://books.google.com/books?id=v62U-XJ4QioC&pg=PA414&lpg=PA414&dq=learning+to+represent+state+with+perceptual+schemata&source=bl&ots=wOWuy7pv5D&sig=ACfU3U0ZUpVLu0ld8WH-JEyV2b_6jYOeRQ&hl=en&sa=X&sqi=2&ved=2ahUKEwi-8NWQuLbyAhUoG6YKHQp-CHAQ6AF6BAgbEAM#v=onepage&q=learning%20to%20represent%20state%20with%20perceptual%20schemata&f=false)
- [Towards a Perceptual Symbol System](https://www.researchgate.net/publication/228670823_Towards_a_Perceptual_Symbol_System) - has {motor + perceptual} schema
- [The Schema Paradigm in Perception](https://www.jstor.org/stable/43853460?seq=11#metadata_info_tab_contents)

