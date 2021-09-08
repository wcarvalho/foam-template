# Notes
* jax + tf version of everything

# Code
* distributed agents in jax
    * [launchpad github](https://github.com/deepmind/launchpad)

* examples of distributed agents:
    * simple example unit test: [Testing a distributed agent with launchpad fails](https://github.com/deepmind/acme/issues/122)
    * [skeleton of DistributedAgent](https://github.com/deepmind/acme/issues/136)
    * D4PG:
        * [training script 1](https://github.com/deepmind/acme/blob/master/examples/control/lp_local_d4pg.py)
        * [training script 2](https://github.com/deepmind/acme/blob/master/examples/gym/lp_local_d4pg.py)
        * [Agent](https://github.com/deepmind/acme/blob/3bc0426bb17797f066a6afe223b563385a2fe839/acme/agents/tf/d4pg/agent_distributed.py)
        * NEGATIVE example:
            [R2D2 single process](https://github.com/deepmind/acme/blob/3bc0426bb17797f066a6afe223b563385a2fe839/acme/agents/tf/r2d2/agent.py)
    * [PWIL + SAC](https://github.com/deepmind/acme/blob/0b9bb1e2c515578ce0e5114ad663474d7db60658/examples/gym/lp_local_pwil_jax.py)

* Useful Jax Code:
    * Training:
        * [Behavioral Cloning](https://github.com/deepmind/acme/blob/master/examples/offline/run_bc_jax.py)
        * [Negative (TF)](https://github.com/deepmind/acme/blob/master/examples/offline/run_bc.py)
    * Agents:
        * [DQN Agent](https://github.com/deepmind/acme/blob/d55be95d5e10f8d8c6ef9f5c16d5197daab83e5d/acme/agents/jax/dqn/agent.py)
        * [Recurrent Actor](https://github.com/deepmind/acme/blob/d55be95d5e10f8d8c6ef9f5c16d5197daab83e5d/acme/agents/jax/actors.py#L177)
    * Networks:
        * [R2D2](https://github.com/deepmind/acme/blob/d55be95d5e10f8d8c6ef9f5c16d5197daab83e5d/acme/jax/networks/atari.py#L170)