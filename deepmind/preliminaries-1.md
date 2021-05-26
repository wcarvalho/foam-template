
* deep reinforcement learning agents are typically composed of three parts:
  * a function for obtaining representations of visual features
  * a function for maintaining some internal representation of internal agent representation of state. 
  * a function that maps this representation of state to actions

* deep RL has found a lot of success in learning this functions for a particular environment (many papers, schema networks, etc.). 
  * we use this success as an indication that neural networks combined with reinforcement learning can already learn a suitable function $f$, i.e., for a given domain we can get good features describing observations.

* However, much work has found that the learned functions do not generalize to minor variations in the environment.
* We posit that this is because we currently don't have good functions $g$ for going from environment features to high-level state representations that enable systematic generalization. Learning such a function $g$ is the focus of this paper.


* agent observes visual observations $x$ in set of possible observations $X$
* agent selects actions $a$ from set of possible actions $A$


<!-- * We posit that this is linked to lack of systematicity(cite lake's paper++) that neural networks have been shown to exhibit. -->



We hypothesize that part of the reason that deep RL agents don't 