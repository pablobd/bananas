# Bananas
Deep reinforcement learning nanodegree project from Udacity. Train a DQN agent to navigate (and collect bananas!) in a large, square world.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

## State space description

The 37 dimensional state space represent a physical model, which consists of:

* 7 rays projecting from the agent at the following angles, 90 being directly in front of the agent: [20, 45, 70, 90, 110, 160, 135]
* Each ray is projected into the scene. If it encounters one of four detectable objects the value at that position in the array is set to 1. Finally there is a distance measure which is a fraction of the ray length: [Banana, Wall, BadBanana, Agent, Distance]
* The agent's velocity: Left/right velocity (usually near 0) and Forward/backward velocity (0-11.2)

## Actions description

 Four discrete actions are available, corresponding to:

* 0 - move forward
* 1 - move backward
* 2 - turn left
* 3 - turn right

## Installion

First of all, you need python 3 and conda. We suggest to use the [Anaconda distribution](https://www.anaconda.com/download/#linux), although other options are available. Follow the instructions at the github [repository dlrn](https://github.com/udacity/deep-reinforcement-learning) to create an environment for the project, install dependencies and create a kernel. You will not need to install Unity, because Udacity provides an already built environment. Download the right version from here  [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip), [MAC OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip), [Windows 32 bit](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip) or [Windows 64 bit](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip). Then, place the file in the p1_navigation/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.

## How it works

After cloning or downloading the repository, open the file  jupyter notebook bananas.ipynb and execute it reading carefully the instructions. Notice that when creating an environemnt for the game we have force the option no_graphics=True. You can change it to False to see a graphic representation of the game.
