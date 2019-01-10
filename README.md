# drlnd_continuouscontrol

## Introduction
Train a robot arm to move to target locations using a DDPQ algorithm similar to the one introduced at [Lillicrap, Hunt, et. al.](http://arxiv.org/abs/1509.02971).

## How it works 

![Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/images/reacher.png)
Picture taken from [official site](https://github.com/Unity-Technologies/ml-agents).

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

In order to solve the environment, the agent must get an average score above +30 over 100 consecutive episodes. Note that we are solving the single agent environment (compared to the multi agent environment depicted in the picture above).  

### Getting Started / Setup

1. Set up a python environment including python 3.6+, numpy, matplotlib, torch.

2. Follow the steps in [here](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md) to install the Unity ML-Agents Toolkit.

3. Clone this repository via `git clone https://github.com/KCool/drlnd_continuouscontrol.git`

4. Download the Banana Navigation environment from one of the links below.  Select the environment which matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
    
5. Place the file in the folder of the repository


### Instructions

Follow the instructions in `Continuous_Control_Solution.ipynb` to train your own agent!

You can also use the pretrained agents (actor and critic) `checkpoint_actor_success.pth` + `checkpoint_critic_success.pth` (= pytorch models) which successfully solved the environment (in ~XXX steps).

### Notes
We make extensive use of code that was provided within previous exercises of the Udacity Deep RL Nanodegree (especially the plain DDPQ implementation).
