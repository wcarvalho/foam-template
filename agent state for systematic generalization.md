---
tags: [agent-state, systematic-generalization]
---

# How do learn agent state that enables systematic generalization?


What are some of the cognitive faculties that enable generalization? Perhaps because it is reminiscent of ourselves, one interesting context to study generalization in is in that of an agent interacting with the world. When the agent is rewarded for some actions and not others, a need for generalization naturally arises, as the agent seeks to generalize prior experience in order to maximize future reward. In this work, we explore the following question: how do we learn a representation for state that supports generalization?

There is a long-standing tradition dating back to "good-old fashioned AI" that at the core of generalization was the ability to carve up the world into flexible and reusable pieces. Perhaps most commonly, these pieces have come in the form of [[symbols]] or [[objects]]. While this approach dominated early cognitive science and artificial intelligence with figures (fields?) like noam chomsky and marvin minsky (correct?), it soon became apparent that while tools like symbols and objects were reusable in theory, building them to be so was another story. Unfortunately, when researchers tried to build them into tools for AI, the resulting systems were brittle outside a narrow band of problems they were created for. 

Recently, Richard Sutton published a blog post recounting the bitter lesson that the AI community has had to learn, time and time again, that sophisticated algorithms with lots of built structure are always beat out by simple algorithms with good learning strategies coupled with large amounts of data.


