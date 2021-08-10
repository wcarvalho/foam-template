# Main Research Theme + why grant is good

- main themes of research: cognitive faculties that enable discovering structure and leveraging this for generalization
- why important
    - enables rapaid adaptation to new situations
    - understanding mechanisms that subserve this will help us understand why people follow the behavior they do when they generalize
        - this could help us understand why things like social stereotyping occur
- what skills I use to attack problems
    - to understand these mechanisms, I plan to use a mixture of experimental work developing machine learning for artificial intelligence to be generally competent in complex 3D environments
    - I plan to collaborate with people that do experimental work in cognitive science and neuroscience to corroborate these theories with human data
    - At the same time, plan to collaborate with theorists in machine learning to study if there are certain kinds of optimality guarentees
    - this grant would enable meet with potential collaborators

# Examples of problems I have already solved
examples of problems that I have already solved
- to make progress, I developed LOAD for Thor
- Thor is interesting because 3D kitchen environment with dozens of objects that are stateful and can interact with each other
    - for example, you cook a potato by placing it on a pot on the stove and turning the corresponding stove-burner on
    - this is challenging because the agent needs to learn to recognize changing object-state and object-relations in order to successfully learn the task
- in this work, I explored the utility during learning of having a built-in object-detector, a capacity theorized to be available to infants by 4 months of age
- with LOAD, focused on what kinds of biases were needed to learn object representations that could capture category, state, and relationships
    - found that posing learning object-centric dynamics model as a classification problem where incorrect labels were derived from other examples provided rich learning signal that was able to cpature...
    - I published this work in the IJCAI conference. Additionally, I was invited to give a talk on it at the Neural Information Processing object centric learning workshop, and I was invited to discuss it on the podcast "This Week In Machine Learning".

# Discussion of future research

There is a debate in cognitive science about "innateness" of human ability to detect objects
    - Like prior work here, I quickly found that building in a capacity to break up the world with a built-in object-detector as opposed to endowing the agent with the ability to learn to decompose the world in whatever way was useful for the learning problem
    - 