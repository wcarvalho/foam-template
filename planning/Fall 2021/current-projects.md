# Todo
- [x] Fellowships [9/20]
- [x] Paper: Perceptual schemata [10/6]
- [x] Environment: Babyai kitchen reinforcement learning environment
- [x] Environment: Thor reinforcement learning environment
- [x] Paper: GVF project (satinder + rick + honglak)
- [x] Paper: compositional policy (honglak + LG)
- [x] Brainstorming: why schemata enable generalization?
- [x] Collaboration: Nameer (new project)
- [x] Collaboration: Lajan (his project)f
- [x] Collaboration: Yichi (dialogue)

# Research
## Mine

1. babyai kitchen reinforcement learning environment
	1.  create tasks = {easy, medium} x {v1, v2, v3} = 6 tasks
		1.  Design (folder of) curricula for each task setting
	2.  benchmark DQN on tasks
	3.  benchmark Impala on tasks
	4.  benchmark Perceptual Schemata + Impala on tasks
		1.  Implement Impala + ConvLSTM (simple baseline)
		2.  Implement Perceptual Schemata
		3.  benchmark Perceptual Schemata + Impala on tasks
1. thor reinforcement learning environment
	1.  create environment
		1.  create task library (with loadable tasks)
			1.  Design classes for tasks
			2.  Benchmark baseline in basic single-task setting
			3.  Create way of checking sampleable tasks are possible
			4.  Create method for automatically checking if tasks can be done in (floorplan, task) combination
		2.  Design multi-task loading class (w/ seperate train/test)
		3.  create procedurally generated-level class (based on "length"?)
		4.  create generalization settings
			1.  generalize within 1 floorplan w/ randomized locations
			2. generalize across floorplans w/ randomized locations
	1.  Design (folder of) curricula for various generalization settings
	1.  benchmark {Impala, Perceptual Schemata} on tasks
2. GVF project (satinder + rick + honglak)
	1. read about theory to understand
		1. option-keyboard
		2. pnas paper
	2. experiment 1 (babyai):
		1. SF vs. Us on Length = 2
		2. SF vs. Us on Length = 3
		3. SF vs. Us on Length = 4
	3. workshop paper
	4. experiment 2 (thor + 1 floorplan)
		1. SF vs. Us on Length = 2
		2. SF vs. Us on Length = 3
	4. experiment 3 (thor + generalize across floorplans)
		1. SF vs. Us on Length = 2
		2. SF vs. Us on Length = 3
	5. Analysis
	6. archive paper
		- draft
		- website
			- generate videos of agent
		- tweet
	7. rebuttal
	8. create poster
	9. create 10-20 minute video

1. compositional policy (honglak + LG)
	1. read {2-4} most cited/recent on option-discovery
	2. read {2-4} most cited/recent on structured policy
	3. experiment 1 (babyai):
		2. Perceptual Schemata vs. Us on Length = 3
		3. Perceptual Schemata vs. Us on Length = 4
	4. workshop paper
	5. experiment 2 (thor + 1 floorplan)
		2. Perceptual Schemata vs. Us on Length = 3
	6. experiment 3 (thor + generalize across floorplans)
		2. Perceptual Schemata vs. Us on Length = 3
	7. Analysis
	8. archive paper
		- draft
		- website
			- generate videos of agent
		- tweet
	9. rebuttal
	10. create poster
	11. create 10-20 minute video

5. why schemata enable generalization?
	  1. RL (Abel) [1 day biweekly?]
	  2. Psychology (Rick) [1 day biweekly?]

## Collaborations
5. sean (bonobo project): [1 hr/week(?) including 30 min meeting]
6. nameer (new project): [3 hr/week(?) including 1hr meeting]
	1. summarize research ideas in {todoist, onenote}
7. lajan (his project)
	1. [1 hr/week(?) including 30 min meeting]
	2. give him benchmarked DQN/Impala code for testing
	4. help w/ writing on paper: [3 days]
	4. rebuttal: [1 day]
8. yichi (dialogue)
	1. [1 hr/week(?) including 30 min meeting]
	2. give him benchmarked DQN/Impala code for testing (no timeframe)
	4. help w/ writing on paper: [3 days]
	4. rebuttal: [1 day]
9. deepmind:
    - perceptual schemata ICLR paper [Due 10/6]
		- paper
			- draft 1
			- draft 2
		- website + tweet
		- rebuttal
		- create poster
		- create 10-20 minute video

---

# Other
10. [fellowship applications](https://docs.google.com/spreadsheets/d/1d-LIJDKTcggyIVdNCVeDbmGAKqGagVvVW6lLn-XQaVM/edit#gid=0)
	1. Apple [Due 9/20]
		-   Write abstract
		-   Research statement
	2. Facebook
		1. 500 word summary [9/20]


## Other things that need dedicated time
- responding to messages on slack (e.g. important for Yichi)


# Lurkers

1. working with Josie on her Theory
2. Deep RL 1 page opinion abstract
    --> use my related work
1. Create research slides from all ideas
