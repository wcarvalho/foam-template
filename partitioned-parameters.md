
# Utilities

1. Helps with #catastrophic-forgetting. By only calling subsets of parameters for different data/portions of environment, you can mitigate catastrophic forgetting in a [[continual-learning]] setting. 
	1. Want to do so in *distributed* way where subsets (not 1 set) is used for data/portion
	2. Examples:
		1. [[Brain]]: The brain partitions its paramters so that subsets are responsible for music, grammar, etc.
			1. [Connecting concepts in the brain by mapping cortical representations of semantic relations](https://www.nature.com/articles/s41467-020-15804-w)
