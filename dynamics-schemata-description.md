# dynamics-schemata-description

## Why is dynamics schemata is reasonable assumption?

In reinforcement learning, [[dynamics]] refers to the probability of an agent transitioning between two states $s$ and $s'$ given an action $a$. Let us assume that states have some underlying structure such that aspects of those transitions are ``consistent'' across different portions of the MDP. Consider using a factored-state representation such that action $a$ transition an agent from $s_1\to s'_1$ or from $s_2\to s'_2$ but $s_1 \neq s_2$ and $s'_1 \neq s'_2$. Assume both have a state factor $c \subset s_1, c \subset s_2$. One can say the two "share" dynamics if given an action sequence $(a_1, \ldots, a_k)$, the factor $c$ takes on the same progression of values $(c, a_1, c', a_2, c'', \ldots)$ for that action sequence. When the agent learns a model for this factor that it can reapply across states with varying factors, we call this a dynamics schema.
<!-- When can describe the dynamics of this factor as a "stereotyped". When an agent learns a model for -->
 