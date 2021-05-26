# broad comments + examples
* we are interested in problem of how an agent can discover dynamics schemata
* what is a dynamics schema?
    * it is a stereotyped situation
    * it corresponds to some of the objects or entities in the environment
    * it describes their dynamics over multiple timesteps
    * we are not trying to find this object does this dynamics
    * we are looking for abstract dynamics that objects of any appearance can take on
    * for example if it is a triangle *or* a circle, their dynamics describe their motion
    * we also see navigating through distractors in the same position but different shapes as the same dynamics
      * this one can be thought of similar to texture with hands 
      * while the exact features you see is different, they visual pattern they induce is the same
      * consider playing soccer
        * regardless of the players, there might be one person in front of you, and two people behind on both side
        * the way their relative positions change as you move, along with the effect these positions have on the actions you can take is the same regardless of the player

# brief saying that I want something general
* okay - there are some dynamics I expect, but there are other dynamics I can't expect.
  * a fundamental philosophy of this work is that for an inductive bias to produce schema that are general, it's hard to plan the kinds of things that will be learned. 
    * We can plan for some in relatively simple and contrived domains
    * but we don't know what notions of dynamics can be usefully discovered in more complex domains
    * with this in mind, we simply want mechanisms that are flexible in their ability to capture dynamics

# Given that want something general, here is desireratta Desideratta

* given then we have flexibility in mind, we design dynamics schemata with the following flexibility
  * a schema will will need the ability to activate in response to any type of data
    * we want flexible computations that enable either coarse or granular decomposition of perception
      * objects
      * sets of objects
      * decentralized objects (such as a flock of birds)
  * schema might overlap in space, time, or features
    * i.e. at one time-point, multiple schema might describe different components of some portion of an observation
      * example?
  * we want the task signal to drive schema discovery. this manifests as having the reward-signal drive decomposition of perception into seperable dynamics
  * in order to work with arbitrary data types, we ideally only utilize basic computations such as projections, top-down modulation, convolutions, and gating mechnanisms.

Hypothesis 0: a convolutional LSTM enables us to obtain an representation that describes the dynamics of present objects in an *entangled* manner
* convolutional tensor $F \in R^{H \times W \times D_f}$ describes the expression of features $f \in R^D_f$ over a spatial grid $H \times W$.
  * for simple environments, it can learn to associate individual high-level objects with individual features $f_i$ (CSWM)
  * for more complex environments, it may not be less optimal to use a single feature for a single object. Here, $f$ may act more like a vocabulary of attributes used to describe perception over a spatial grid (objects paper)
  * if we want $f$ to contain features which describe dynamics, then we should use a convolutional LSTM at least at the fina layer
**result**: Convolutional LSTM that produces $H^{\tt spatial}_t$

Hypothesis 1: given that cognitive scientists view agents as having multiple schemata for the environment, we want different schemata to latch on to encoding and explaining different aspects of an agent's sensory perception
  * this means that the mechanism used to select fragments of perceptual information to be modeled by a schema should be fairly flexible
    * ideally, the task and corresponding reward signal drives the agent's learning of how to use different schemata to represent different components $c$ of the environment
      * components of the environment might be objects, sets of objects, or other task-relevant fragments of the agent's sensory perception
        * decentralized objects (such as a flock of birds)
    * we hypothesize that an architecture can learn to disentangle components of its sensory percept by learning the subspace of $f$, $f_c \subseteq f$ over which the component is expressed
      * importantly, this allows schema to overlap in space, time, or features if useful for the task
**result**: want to associate schema with different subspaces of $H^{\tt spatial}_t$
<!-- * a schema is flexible if it can integrate information for any fragment of the environment -->
<!-- * a schema needs to be able to flexibly interpret and integrate information about arbitrary fragments of the environment -->

Hypothesis 1.5: given that cognitive scientists describe schemata as interpreting and integrating information into a model of the environment, like object-files, we can use a recurrent neural network to decribe this model.
  * In order to have schema coordinate and share information, we can leverage transformer-style attention when performing update

Hypothesis 2: a schema will enable generalization if it can recognize relevant perceptual fragments in novel situations and integrate them into the agent's perception of state consistently with how it did during learning 
**result**: state + policy
<!-- Hypothesis 1: the mechanism for learning a schema is flexible if it can learn to    -->
  <!-- * depending on the task, an agent may want to represent an object, a set of objects, or some other task-relevant component of the environment $c$. -->

  <!-- * in order to disentangle objects/sets of objects important for the task, we want to look at the expression of a subset of features over a convolutional tensor that describes how those features  -->
<!-- Hypothesis 1: we assume that some environment will be sufficiently complicated that an agent will need to use multiple convolutional channels to represent an object -->
  <!-- * these channels can thus be thought of as a vocabulary to describe components of the scene -->

<!-- Hypothesis 2: a neural network can learn to track task-relevant dynamics by focusing on feature subspaces -->
  <!-- * nn can decompose dynamics into multiple seperable dynamics by focusing on (potentially overlapping) feature subspaces -->

<!-- Hypothesis 3: 
* can use a projection of final CNN features to look at feature-relations
* can use top-down modulation to focus on certain feature-relations
* can use second  convolutions can be used to find when  -->

Discussion:
* comparison to more baselines
* ablate our form of attention with the more popular transformer attention




Example:
* when might you have alternating dynamics
  * for example a light that alternates colors according to some periodic function