---
tags: [hrl, schemata]
aliases: [action-schemata]
---
# Hierarchical, compositional policy on top of Perceptual Schemata


Assumes structured state given by [[perceptual-schemata]]

**Sampling goal + low-level policy parameters**
$$
\begin{align}
g_t &\sim \pi^{\tt goal}(g | s^{{\tt hi}}_t, \tau) \in \mathbb{R}^{d_g}\\
b_t &\sim \pi^{\tt params}(b | s^{{\tt hi}}_t, g_t, \tau) \in \{0,1\}^{m}
\end{align}
$$

 
**Computing low-level policy actions**
$$
\begin{align}

V(s^{\tau}_t, g_t, \tau) &= \sum_i b_{t,i} V_{\theta_i}(h^{(i)}_{t}, g_t, \tau) \\

\pi(a_t|s^{\tau}_t, g_t, \tau) &= \sum_i b_{t,i} \pi_{\theta_i}(a_t|h^{(i)}_{t}, g_t, \tau) \\

a_t &\sim \pi(a_t|s^{\tau}_t, g_t, \tau)

\end{align}
$$
 
**Flat, compositional policy**
$$
\begin{align}

b_{t+1} &\sim p(b_{t+1} | s^{\tau}_t) \in \{0,1\}^{m} \\

V(s^{\tau}_t, \tau) &= \sum_i b_{t,i} V_{\theta_i}(h^{(i)}_{t}, \tau) \\

\pi(a_t|s^{\tau}_t, \tau) &= \sum_i b_{t,i} \pi_{\theta_i}(a_t|h^{(i)}_{t}, \tau) \\

a_t &\sim \pi(a_t|s^{\tau}_t, \tau)

\end{align}
$$
  