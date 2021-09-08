# Schemata during camping example

Recently, I went camping with friends. Somebody brought a Bluetooth speaker to play music by the fire. When the time came, the DJ had to pair with the speaker. When it came time to use the speakers, they were able to quickly learn how to navigate the speaker's state space as useful to us. I argue that in this situation, a person is using a "[[schemata]]" of speakers to quickly learn to use a novel speaker. The schema probably manifested as an expectation for what traversal through the state space might look like based on "speakers". This made it easy to quickly choose actions with a relatively high success rate given the goals (e.g. playing songs for people). The schema manifested with (a) a mechanism for recognizing the state in the speaker state space, (b) a model for how the state space would evolve, (c) and a policy for how to navigate this state space. When using the speaker schema, it is probably composed with a schema for acting in mature.

**clarification**: policy is over goals, not low-level actions. similar to vision, low-level vision + low-level policy are all shared. "schema" contribute subgoals/compete to provide subgoals for low-level policy.
#schema-example
#schema

# Language + Schemata

Language describes the evolution of schema's over time. How does this help learning?

1. Language may be used to determine the latent code which is used for (a) reconstruction (b) the estimate of [[state]] at some moment (c) the description of some part of the environment to another agent as [[language]]?

``` mermaid
graph TD;
  t-->schema_1
  t+k-->schema_1
  schema_1-->language_1

  t+k+1-->schema_2
  t+k+n-->schema_2
  schema_2-->language_2

  language_1-->reconstruction
  language_2-->reconstruction

  language_1-->expression
  language_2-->expression
```


# Literature
### Brain Science
1. [Clearly shows relation of schemata to options](https://www.cnbc.cmu.edu/~plaut/papers/pdf/BotvinickPlaut04PR.seq-action.pdf)
2. [Compares associative vs non-associative](https://link.springer.com/content/pdf/10.3758/BF03329880.pdf)
3. [Show that if "schema" present, enables one-trial learning in rats](https://pubmed.ncbi.nlm.nih.gov/17412951/), i.e. partial explanation to rapid adaptation
4. [Much of Arbib's references indicate the formalism I use](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.470.6492&rep=rep1&type=pdf)
5. [Good paper to plan writing the paper](https://psyarxiv.com/uz5wp/): Understanding exploration in humans and machines by formalizing the function of curiosity
6. [Survey of role of schemata in cognitive neuroscience of action](https://psycnet.apa.org/record/1997-97298-000) - The cognitive neuroscience of action
7. [Notes on Schema Theory from MIT class](http://web.mit.edu/pankin/www/Schema_Theory_and_Concept_Formation.pdf)
8. Look up "Review on schemata"
9. Look up schemata + bayesian networks


### AI
2. Seems very related to object-oriented MDPS... need to figure this out.
3. A lot of people in robotics have adapted the "schema" terminology. e.g. "Integrating behavioral, perceptual, and world knowledge in reactive navigation"

---

## Todo

- [ ] read through literature and see when schema/Perceptual are used
- [ ] in literature, schemata include both a transition function **and** a policy
