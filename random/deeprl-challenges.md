# Challenges for Deep RL

* Removing task boundaries?
* Can you come up with your own tasks? 

### Object-centric models

* Planning with subset of factors in model
* learning to implictly model objects
  * [Object files](https://arxiv.org/pdf/2006.16225.pdf)
  * [RIMs, BiRIMS]()

### Overfitting in RL

* Generalizing to new environments
* Generalizing to changes in visual appearance
  * Changes in background
  * Changes in apperance on objects (task is exactly the same)
    * [Coinrun](), [Carla](), Atari ([Witty](https://arxiv.org/pdf/1812.02868.pdf), [Machado](https://arxiv.org/pdf/1810.00123.pdf))
      * Perspective: Underlying MDP is *exact* same ([Network Randomization](https://arxiv.org/abs/1910.05396), [Bisimulation](https://arxiv.org/pdf/2006.10742.pdf))
  * Learning it ignore distractor objects (especially in random locations)
    * [metacure](https://arxiv.org/pdf/2006.08170.pdf)
* Generalizing to new map layouts/**learning to search** a map
* Generalizing to new reward functions
* Object-centric Option discovery
  * figuring out goals for options using objects

### Generalization

* Once you learn things, how can you leverage this to inform exploration henceforth?

### Exploration

* ~~directed exploration. use knowledge of environment to target exploration. **search**~~
* uncertainty quantification hasn't helped us with exploration in large problems yet
* Fin: exploration when you have examples of good states/demonstrations
  * pretty practical
* reward-free exploration
* How do you learn good representations **for** exploration?

### Language

* Language for inference
  * infer "model" via language
  * inferring reward function from language/using language to specify goals
  * infer "plan" from language
* Why is language **generation** useful during a task?

  * how to use language to represent MDP, Model, Reward function
    * humans seem to use "language" to store MDP information [language seems necessary for human spatial reorientation](https://pubmed.ncbi.nlm.nih.gov/17663986/)







# Random Ideas

* meta-learn a predictive state representation?