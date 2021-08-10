
Why is it useful to define schemata over state factors? State-inference that allows your policy to adapt in a zero-shot manner, you can do planning in novel environments, and you get a really compact model for a really large complex environment. Consider sequences of states $(s^1_{1}, \ldots, s^1_{n})$ and $(s^2_{1}, \ldots, s^2_{n})$. Assume they both have factors $C_1=\{c_i\}$, then the same model $p(c_i'|\{c_i\},a)$ can be used to model transitions across both of these. How do you learn $p(s|s,a)$? First, the model *complexity* can be a function of the size of the state-space, otherwise you're doomed (similar to the result found by Van Roy). You can just function approximation with a massive function approximator and hope for the best, but that isn't panning out when it comes to learning models for the environment. However, you come combine these approaches. Use a function approximator, but have it be specialized for some broad class of data defined by $C_1=\{c_i\}$. When states have other factors evolving with their own dynamics, you can compose these transition models to describe the overall state. Importantly, this let's you use your model in novel settings if you have experienced the components before (e.g. using your laptop in the woods). Additionally, if you can search for the correct schema quickly, this let's you do belief state inference into that schema's state and apply your policy for really fast adaptation.

#schemata
#dynamics
#adaptation
#planning
#model-complexity
