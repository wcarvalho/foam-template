# Symbols

[[symbols]] and [[objects]] seem to have a deep connection, but they seem to refer to different things. Let's assume an object is a reference to a fragment of the environment. The following relationship holds
$$
  {\tt symbol} \to {\tt object} \\
  {\tt variable} \to {\tt environment.fragment} \\
  {\tt symbol} \to {\tt variable} :: {\tt object} \to {\tt environment.fragment}
$$



I have the hypothesis that a key aspect of symbols is their ability to perform [[indirection]]. Objects are pieces of the environment which can be referenced to, e.g. a *schema* is an instance of an object. Symbols are the **typed** points of reference that include summary information about the thing to which they refer.

How do you represent a reference flexibly? How do you create a mechanism that can serve as a reference to *any* type of information? With transformers, you have a sequence of observations and you use newer observations to create references for prior observations

$$
  z_1, \ldots, z_T \\
  q_t = W^q z_t \quad \text{reference} \\
  v_t = \operatorname{Att}(Q=q_t, K=V=\{z_{\leq t}\}) \quad \text{referenced value}
$$

For this to work you'd need to spawn just some random variable as the query $q_t \sim \mathcal{N}(0,1)$ that's not tied in any way to the observed data. Some examples of where $q_t$ could be sampled:

* a sphere
* a plane

Upon spawning it, you'd need to find a mapping from that random variable $q_t$ to a desired object $v_t$, $v_t=W q_t$. So the thing that has to be made on the fly is the mapping. Since $q_t$ is completely random and has no information, the information that computes the mapping probably has to be in $W$, so something like $v_t=W(q_t, v_t) q_t$? 

**Main conclusion**: the wackiness of symbols seems to be that you can conjure a variable and assign it to data that is completely unrelated to your observations. Not sure about what that mechanism should look like.