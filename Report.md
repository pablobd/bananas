# Report

## Solution

The agent is build following the [nature paper](https://web.stanford.edu/class/psych209/Readings/MnihEtAlHassibis15NatureControlDeepRL.pdf) *Human-level control through deep reinforcement learning*. 

Specifically, the agent learns how to play the game through experience. By playing randomly the game, the agent stores experiences (state, action taken, reward and next state). The agent uses these stored experiences to estimate the q-value function, i.e. for each state and action the expected discounted reward. To estimate it, the agent makes use of a feed forward deep network, with the following architecture: 
* input layer of 37 units (dimension of state space),
* hidden layer of 64 units,
* hidden layer of 32 units,
* output layer of 4 units (one for each action)

## Results

This solution solves the game in 462 episodes, which is much faster than the proposed solution at Udacity.

![alt text](https://github.com/pablobd/bananas/blob/master/bananas_result.png)


## Improvements

In the next release, we want to add three parameters to the agent class to enable several functions that would theoretically improve the performance of the agent:
* Double DQN, [paper](https://arxiv.org/abs/1509.06461)
* Prioritized experience replay, [paper](https://arxiv.org/abs/1511.05952)
* Dueling Q Network, [paper] (https://arxiv.org/abs/1511.06581)
