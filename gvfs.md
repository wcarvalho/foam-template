---
tags: [gvf-schemata]
---

# GVFs on Perceptual Schemata

$$
\newcommand{\mb}[1]{\mathbb{#1}}
\newcommand{\mc}[1]{\mathcal{#1}}
\newcommand{\stategvfc}[2]{
q^{#2}_{\pi, s^{\tau}}\left( #1\right)
}
\newcommand{\qfnc}[2]{
q^{#2}_{\pi, {r}}\left( #1\right)
}
\newcommand{\gvf}[3]{ % semantics, arguments, parameters
q^{#3}_{#1}\left( #2\right)
}
\newcommand{\Exp}[1]{\mb{E} \left[ #1\right]}
\newcommand{\argmax}{\operatorname{argmax}}
$$
  

**Task learning goals**

We want a multi-task reinforcement learning architecture that can leverage learning multitask learning to enable faster learning of tasks across environments. For example, consider and agent that needs to learn 3 task \textit{types} --- slicing, heating, and filling, each which manifest in a dozen ways --- in 10 kitchens.


* First, we want multi-task learning within a single kitchen to enable the agent to more quickly learn the task types. As it learns each task type, it learns which objects are relevant for the given task type by contrasting the tasks.
* Second, by learning which objects are relevant for a task, we want the agent to learn known tasks in new environments more quickly.

  

**Architecture**

Assumes structured state given by [[perceptual-schemata]].


**Action prediction**

$$
\begin{align}
s^{\tau}_t &= [h^{(1)}_{t}, \ldots, h^{(n)}_{t}] \\
\stategvfc{s, a, {\tau}}{} &= \operatorname{MLP} (s^{\tau}_t) \\
\qfnc{s, a, {\tau}}{} &= \stategvfc{s,a, {\tau}}{}^{\top} W^{r} e^{\tau}
\end{align}
$$
  

**Learning GVF Semantics**

$$
\begin{align}
a_{t+n} &= \operatorname{argmax}_a \qfnc{s_{t+n}, a, \tau}{\theta} \\
y_t &= \sum^{n-1}_{k=0} \gamma^k s^{\tau}_{t+k} + \gamma^n \stategvfc{s_{t+n}, a_{t+n}, \tau}{\theta^-} \\
\mc{L}_{\tt pred} &= \Exp{ \left(
\stategvfc{s^{\tau}_{t}, a_{t}, \tau}{\theta} - y_t
\right)^2}
\end{align}
$$
  
 
**Factor Control**
$$
\begin{align}
	r^{{\tt fac}, (i)}_t &:= ||h^{(i)}_{t} - h^{(i)}_{t-1}||\\
	a^{(i)}_{t+n} &= \argmax_a \gvf{\pi, r^{{\tt fac}, (i)}}{s_{t+n}, a, \tau}{\theta} \\
	y_t &= \sum^{n-1}_{k=0} \gamma^k r^{{\tt fac}, (i)}_{t+k} + \gamma^n \gvf{\pi, r^{{\tt fac}, (i)}}{s_{t+n}, a, \tau}{\theta^-} \\
\end{align}
$$
## Related to Schemata

1. [The Role of Anticipation in Cognition](https://constructivist.info/riegler/pub/Riegler%20A.%20(2001)%20The%20role%20of%20anticipation%20in%20cognition.pdf#:~:text=An%20organism's%20schemata%20determine%20the,actually%20perceive%20the%20expected%20information.)