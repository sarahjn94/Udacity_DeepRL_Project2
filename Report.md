# Udacity_DeepRL_Project2

# Project 2: Continuous Control

### Learning Algorithm

For this Continuous Control project, the implementation used a deep deterministic policy gradient (DDPG) learning algorithm.

	- Actor-Critic architecture
		- Both had local and target network with soft updates on target network
		- Input layer of size 33
		- First hidden layer of size 400 with ReLU activation and batch normalization
		- Second hidden layer of size 300 with ReLU activation
		- Output layer of size 4
	- Used a replay buffer to store past experiences
	- Ornstein-Uhlenbeck noise process with noise decay to explore action space

	- Hyperparameters:
		- Replay buffer size: 1e6
		- Batch size: 128
		- Gamma (discount factor): 0.99
		- Tau: 1e-3
		- LR_Actor: 1e-4
		- LR_Critic: 1e-3
		- Weight decay: 0
		- Training episodes: 1000
		- max_timesteps: 1000
		- Noise:
			- theta: 0.15
			- sigma: 0.3
			- decay_rate: 0.998

### Plot of Rewards

![Graph](/outputGraph.png)

Environment solved in 209 episodes!	Average Score: 30.19


### Ideas for Future Work

	- Try other noise parameter configurations and options
	- Delayed policy updates
	- Gradient clipping
	- Implement prioritized experience replay for more efficiency
	- More hyperparameter tuning
	- Try other learning algorithms or combinations
