**humans generalize broadly by composing schemas over diverse aspects of their experience**
	- cognitive scientists believe human's discover "schemas" to represent regularly occurring structures in their experience
	- For example, a human that has learned to drive will have learned a diverse set of schemas for representing various aspects of their environment. 
	- They might have schemas for representing types of cars (such as sedans), common car-motions (such as speeding or stopping), and even car arrangements (such as a row of cars in traffic).
	- Part of what enables humans to generalize broadly is their ability to discover a diverse range of schemas and to re-combine them in novel ways.
	- Once somebody has learned various driving schemas, they can recombine them in novel ways to navigate a new city filled with novel cars and unknown pedestrians.

**AI may generalize broadly if learns schema-like representations**
	- AI currently doesn't generalize broadly.
	- Typically has 1 kind of generalization.  
	- hypothesis: we can get AI to generalize broadly if we can get them to learn schema-like representations.
	- As a first step, we study learning schemas for perception (i.e. \newterm{perception schemas}) that support generalization within a diverse set of tasks and environments.

**study generalization across 3 environments with own regularly occurring structures**
 - We create a mini-suite consisting of three diverse environments and task structures, each with their own regularly occurring structures that occur during task-completion. 
  
  
- We propose Composable Perception Schemas (CPS), a state representation learning architecture that learns composable perception schema representations. 
- Perception schemas are distributed across a set of recurrent perception subschema modules that employ a novel and expressive feature attention mechanism.
- Each subschema dynamically applies its feature attention mechanism to attend to important features present across all positions in the agent's observation.
- In order to coordinate what each subchema represents, they share information with transformer-style attention.
- When combined with spatio-temporal features, we show evidence that the perception schemas CPS discovers capture diverse structures including object-motions, 3D objects, spatial-relationships between objects.
- Importantly, each subschema module has significantly fewer parameters than a single monolithic module. 
- We hypothesize that learning multiple, smaller subschemas creates a representation learning bottleneck that reduces overfitting to the training environment and encourages the discovery of regularly occurring structures.


	


 experiments indicate perception schemas can capture diverse regularly occurring structures in percetion
	*  {object-motions, active perception of 3D objects (e.g. across angles + shaped), object-configurations}
experiments indicate that CPS and the dynamic spatially-invariant feature-attention that powers it better generalize than other recurrent architectures based on spatial attention.



Contributions:
* novel composable state-representation learning architecture
* novel temporally-dynamic and spatially-invariant feature attention mechanism
* we show that our architecture, attention mechanism, and task-driven approach enables generalizing across three disparate environments and task structures (5)
* we show that feature-attention over spatio-temporal features enables recall of sequentially observed object-motions.
* we show that feature-attention facilitates discovering and composing perception representations for recalling object-motions (5.1), for active-perception of 3D objects (5.2), and for navigation through object-relationships (5.3).
* composable perception schemas enable learning a state rep that generalizes mitigates interference between the information held in different schemas. we find this enables generalizing memory-retention of goal-oriented behavior to environments with (2x, 3x) the number of distractors as in training.  
	* we show that leaning composable state representation enables learning memory retention which generalizes mitigating interference between an agent's new experiences and its retention of old experiences. 




# Thrown out
**cog sci**
, For example, humans have schemas for representing individual the regular traffic patterns that cars exhibit cars and for representing regular walking patterns exhibited by pedestrians.
for example, driving manifests with rows of cars moving together with regular motions; walking manifests with navigating through common movements of groups of pedestrians.
	- cars with with regular traffic patterns, people walk togther with regular motions
- eating
, and even different traffic laws.
- they can then generalize and navigate within a new city with novel cars and unknown pedestrians by combining these schemas in novel ways.
- Schemas allow people to recognize and re-combine diverse structures they've experienced to broadly generalize across a broad range of environments

**ai can't generalize**
- In this work, we develop an architecture for discovering schemas for perception (i.e. perception schemas) for regularly occurring structures that appear during goal-directed behavior. 
- We hypothesize that an agent which represents state with perception schemas will better generalize within diverse environments and tasks.  



 - We believe that given a large and complex environment, reward is a powerful signal for developing AI that can discover regularly occurring structures within the world
	 - Thus, we take a task-driven approach to the discovery of perception schemas.
