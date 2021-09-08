---
tags: [schemata, dynamics, adaptation, planning, model-complexity]
aliases: [Dynamics Schemata, Schemata]
---

# Why is it useful to define schemata over state factors?
State-inference that allows your policy to adapt in a zero-shot manner, you can do planning in novel environments, and you get a really compact model for a really large complex environment. Consider sequences of states $(s^1_{1}, \ldots, s^1_{n})$ and $(s^2_{1}, \ldots, s^2_{n})$. Assume they both have factors $C_1=\{c_i\}$, then the same model $p(c_i'|\{c_i\},a)$ can be used to model transitions across both of these. How do you learn $p(s|s,a)$? First, the model *complexity* can't be a function of the size of the state-space, otherwise you're doomed (similar to the result found by Van Roy). You can just function approximation with a massive function approximator and hope for the best, but that isn't panning out when it comes to learning models for the environment. However, you come combine these approaches. Use a function approximator, but have it be specialized for some broad class of data defined by $C_1=\{c_i\}$. When states have other factors evolving with their own dynamics, you can compose these transition models to describe the overall state. Importantly, this let's you use your model in novel settings if you have experienced the components before (e.g. using your laptop in the woods). Additionally, if you can search for the correct schema quickly, this let's you do belief state inference into that schema's state and apply your policy for really fast adaptation.


# Why are dynamics schemata a reasonable assumption?

In reinforcement learning, [[dynamics]] refers to the probability of an agent transitioning between two states $s$ and $s'$ given an action $a$. Let us assume that states have some underlying structure such that aspects of those transitions are "consistent" across different portions of the MDP. Consider using a factored-state representation such that action $a$ transition an agent from $s_1\to s'_1$ or from $s_2\to s'_2$ but $s_1 \neq s_2$ and $s'_1 \neq s'_2$. Assume both have a state factor $c \subset s_1, c \subset s_2$. One can say the two "share" dynamics if given an action sequence $(a_1, \ldots, a_k)$, the factor $c$ takes on the same progression of values $(c, a_1, c', a_2, c'', \ldots)$ for that action sequence. When the agent learns a model for this factor that it can reapply across states with varying factors, we call this a dynamics schema.
<!-- When can describe the dynamics of this factor as a "stereotyped". When an agent learns a model for -->
 