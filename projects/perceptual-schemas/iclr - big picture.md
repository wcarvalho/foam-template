Task-driven discovery of composable perception schemas for heterogenous generalization in reinforcement learning

### Intro
- humans generalize broadly by learning diverse schemas over regularly occurring structures in their experience. schemas can be composed for generalization.
- AI doesn't generalize broadly. May generalize broadly if learns schema-like representations
- study generalization across 3 environments with own regularly occurring structures 
- Propose composable perception schemas, an architecture for discovering task-relevant regularly occurring structures
- compare to recurrent architectures with competing spatial attention and find that we better generalize

### Related Work
- **Generalization in Deep RL**: most work focused on one type of generalization.
- **Generalization w/ training regime**: we follow these practices
- **Generalization w/ feature attention**: prior work was single-head and static. we are dynamic and multihead. we also show wider generalization.
- **Generalization w/ spatial attention**: More recent work follows more in line with dynamic attention over observation (RIMs + Mott). RIMs was particularly inspirational for this work as we both use a set of recurrent modules as basis for top-down attention on observation. However, both RIMs and Mott used spatial attention, which we believe is limited in its ability to facilitate recognizing objects spread across an agent's observation. We show evidence that this form of attention for our tasks, where objects appear in or move between a set of positions.

### Methods
- Composable Perception Schemas  
- perception schemas can capture diverse aspects of the environment.  
- perception schemas coordinate what they represent.

### Experiments

- perception schemas enable generalizing to novel spatial and temporal compositions of object-motions  
- perception schemas enable generalizing to novel compositions of navigation to and active perception of 3D objects  
- perception schemas enable generalizing memory retention to (2x, 3x) longer time-horizons than trained on

### Analysis
- some perception schemas **show selectivity for perception of goal-objects** 
	- higher L2 norm of RNN-state activations
- **different subsets of perception schemas respond to different categories** of observation-action sequences

### Discussion

experiments indicate perception schemas 
- **capture diverse regularly occurring structures in percetion**
	*  Ballet task: shape-color object-motion
	*  Place X on Y: active perception of 3D objects (e.g. across angles + shapes)
	*  KeyBox task is composed of reguarly occurring object-configurations. experiments on abstract MDP task indicate perception schmas can capture shape-color agnostic object-configurations
- **can coordinate what they represent to mitigate interference** during generalization.
	- might help with mitigating interference of active-perception of task- and distractor-objects for place X on Y
	- might help with generalizing memory-retention to (2x, 3x) more distractors to navigate around in envirionment

- we may get richer perception schemas by combining spatially-broadcast feature-attention and spatially-invariant spatial-attention 
	- feature-attention seems to be better for state that requires composing multiple things
	- spatial-attention seems to better when need to ignore aspects of the environment.
		- In results for ignoring unseen number of distractors, RIMs, outpformed CPS (A.1)
- perception schemas are limited to in ability to capture patterns over long time-horizons: transformers

- end: let's look to schemas for more inspiration on what capabilities AI should have.
	- we have developed a method that begins to capture perception schemas cover a narrow range of the kind of structures that human's to capture. Beyond learning schemas for recognition, they also learn schemas for how to behave (e.g. ) and for modelling the dynamics of portions of their environment. We hope researchers will draw more inspiration from the broad modelling and generalization capabilities of schemas to further advance AI.


## Appendix

## Additional Results
- RIMs with spatial attention is better for generalizing to unseen number distractors
- perception schemas can latch onto spatial relationships between objects.