# Reinforcement Learning with OpenAI Gym
#### Dennis Tran

# Problem Statement
A Robotics company is looking for ways to reduce costs in training its robots. It is wondering whether or not Reinforcement Learning in simulated environments is a viable alternative for training.

Using OpenAI Gym, we will demonstrate simple applications of established Reinforcement Learning algorithms that are used in more complex environments.


# Method
We used the Stable-Baselines3 package in order to implement our algorithms. We used 4 environments:
1. CartPole
2. Pendulum
3. Breakout
4. CarRacing

We chose the first two environments given that they are Classic Control problems in Reinforcement Learning. They both differ in action spaces: CartPole is Discrete, while Pendulum is Continuous. We used PPO (Proximal Policy Optimization) on CartPole where the policy seeks to make as large of an improvement step without collapsing performance. The maximum score where OpenAI considers it solved is 200, setting our goal. A2C (a variant of Asynchronous Advantage Actor Critic) was used in Pendulum as well as DDPG (Deep Deterministic Policy Gradient), a form of Q learning. Pendulum has no state where it is solved, therefore the goal is to get as high of a score as possible.

For Breakout and CarRacing, they are a bit more complex than the previous two. Breakout has no solvable state while CarRacing has a solvable score of 900. A2C was used in Breakout with success while CarRacing is a work in progress.

# Conclusion
Overall, we were able to solve Cartpole while our scores in Pendulum and Breakout only require more training time to increase the scores. There can be tweaking to all three models in order to not only improve the score, but to improve the rate at which it is able to achieve a good score. That needs more testing and research on our end. CarRacing still needs quite a bit of work to get positive, as our initial models have the car ride in circles. We imagine this would need some custom tuning and deeper implementations that involve more control of the car and of the reward function.

All in all, despite being simple games, one not need imagine to see where their usefulness may lie. Simulated environments are virtual environments but with more detail, thus are more complex. Although the physics may be more realistic and there may be more moving parts to the environment and agent, the fundamentals remain. The algorithms don't necessarily need to change but their implementation may be tweaked or modified to suit the practitioner's needs. 

Simulated environments are already being applied in training Tesla cars and developing nuanced motor control in robotic hands as OpenAI has shown. Reinforcement learning could be cheaper as the environments are digital. So long as the simulated agent accurately reflects the real world robot, the training should carryover. Imitation learning where a human controls the agent can be an even faster way of training. There is still much to learn and figure out. This little project is but a drop in the bucket.