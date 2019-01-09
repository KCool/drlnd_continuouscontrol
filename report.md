### Algorithm
We implemented a DDPQ as proposed by [[Lillicrap, Hunt, et. al.](http://arxiv.org/abs/1509.02971). DDQP is extends the [famous DQN algorithm](http://www.nature.com/articles/nature14236) s.t. it is able to train agents with continuous action spaces.
Compared to DQN, an additional neural network (the actor) is introduced, which is trained to approximate the optimal policy directly. The Q-Network (the critic) still exists and serves as a judge to the actor.

In order to speed up convergence we implemented two additions compared to the originally proposed implementation:
* Batch normalization as proposed in [Ioffe and Szegedy](http://arxiv.org/abs/1502.03167)
* Set local and target network weights to equal values at initialization (for both actor and critic)

### Learning Curve

Score plot of our best attempt: An agent that solved the environment in XXX episodes.

![scores](images/scores.png)

The score (cumulated reward per episode) is increasing over time - the agent learns to play.

### Hyperparameters
We took a rather heuristic approach for finding the right configuration of our agent. The main ingredients of our model are:

 - Neural network: ...
 - Learning rate: ...


### Improvements / Ideas for Future Work
Further improvements could be:
 - Leverage parallel / distributed training using the 20 agent environment
 - Do a more systematic hyperparameter search/tuning
 - Try solving other environments using a similar DDPQ implementation
