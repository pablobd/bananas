# Bananas
Deep reinforcement learning nanodegree project from Udacity. Train a DQN agent to navigate (and collect bananas!) in a large, square world.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

## State space description

The 37 dimensional state space represent a physical model, which consists of:

* 7 rays projecting from the agent at the following angles: [20, 45, 70, 90, 110, 160, 135] # 90 is directly in front of the agent
* Each ray is projected into the scene. If it encounters one of four detectable objects the value at that position in the array is set to 1. Finally there is a distance measure which is a fraction of the ray length: [Banana, Wall, BadBanana, Agent, Distance]
* the agent's velocity: Left/right velocity (usually near 0) and Forward/backward velocity (0-11.2)

## Actions description

 Four discrete actions are available, corresponding to:

* 0 - move forward
* 1 - move backward
* 2 - turn left
* 3 - turn right




