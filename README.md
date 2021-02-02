# AI611 Deep Reinforcement Learninng - KAIST academic year 2019/20 spring semester

This PhD level course included several basic, intermediate and advanced topics regarding state of the art deep reinforcement learning.
The course was scheduled in two main parts, the first part covering the basic theory and concepts behind reinforcement learning and deep reinforcement learning, and discussion of basic algorithms, and the second part consisting in a group paper presentation and a final group project consisting in training a deep RL model of choice on the Bubble Bobble game, investigating the generalization and transfer learning capabilities of the trained model on the 100 levels of the game.

Some covered theoretical topics:
  - MDPs
  - dynamic programming in RL
  - model free prediction. MC learning, TD learning, lambda-TD
  - model free control. on-policy MC control, on-policy TD learning, off-policy learning
  - value function approximation. LSPI, DQN
  - actor-critic, policy gradient. MC policy gradient, AC policy gradient
  - intergate planning and learning in RL. DYNA-Q
  - bandits
  - POMDPs

# Repository contents

  - group paper presentation slides sbout IQN paper. Will Dabney, et al. "Implicit Quantile Networks for Distributional Reinforcement Learning"
  - final group project presenentation about training the IQN agent on the bubble bobble env game. Including code, ideas and basic experimental results
  - videos about the trained DQN and IQN agents (up to level 10).
  Youtube link for the DQN video: https://www.youtube.com/watch?v=QDXTZ2bXii8
  Youtube link for the IQN video: https://www.youtube.com/watch?v=BEen9P1n-r0&t=3s

[![watch the video](bubblebobble_iqn.gif)](https://www.youtube.com/watch?v=BEen9P1n-r0&t=3s)

## Final project by Ttobot Team - IQN + Bubble Bobble
For the final group project we used the dopamine RL framework developed by Google. The codes developed to train the agent can be found in the GitHub repository https://github.com/cp105/ai611_project.git in the bubble folder.
For training we uses 2 geforce gtx1080 GPUs.
Key contents of the ai611_project repository:
  - .gin configuration files with the adopted various training configurations and hyperparameters. For generating the shown videos the bubble_iqn8.gin config was used, while in the final exam the bubble_iqn9.gin was used for training
  - the retro_lib.py file containing the RetroPreprocessing class. wrapper of the Bubble Bobble env game, also featuring a selected action space, image manipulation, custom reward function, etc..
  - bubble_runner.py file containing the BubbleRunner class to run experiments on our configurations
  - train.py file used for training, as well a the .ipynb files in the ./notebooks folder used for training and visualization.

We have been able to succesfully train the IQN agent on the first 10 levels (out of 100) of the bubble bobble env, while proving the difficulties in generalizing and succesfully training (with the given configurations and neural network architecture) the trained agent on more levels. The game is proven to be a difficult task to solve for most DRL algorithms, as also shown by the other teams (due probably to the complexity of the game environment, multi-enemy, complexity and substantial differences between levels). As a result further improvements and new framework configurations are needed, as well as longer training times, to hopefully successfully train the IQN agent on the whole game.
This course has been an interesting, fun and satisfying achievement and a good opportunity to learn, code and collaborate in a multicultural env.

