# World Wumpus Problem Solver

This repository contains implementations of reinforcement learning algorithms to solve the classic World Wumpus problem. The World Wumpus problem involves navigating a grid-based environment where an agent must find gold while avoiding hazards such as pits and the Wumpus creature.
![image](https://github.com/user-attachments/assets/9f897c50-dc29-484a-ba6d-a277a60d7a98)


## Problem Overview
The agent operates in a 4x4 grid environment where each cell can be empty, contain a pit, the Wumpus creature, or gold. The agent can move up, down, left, or right and can shoot an arrow in one of these directions to eliminate the Wumpus threat (optional action).

### Objectives:
1. **Traversal in the Grid:** Efficiently navigate the grid environment.
2. **Avoid Hazards:** Learn to avoid pits and the Wumpus creature.
3. **Collect Gold:** Locate and collect the gold.
4. **Eliminate Wumpus:** Optionally shoot an arrow to eliminate the Wumpus.

### Environment Setup:
- **State Space:** 16 states corresponding to a 4x4 grid configuration.
- **Actions:** Move up, down, left, right; optionally shoot arrow in one of these directions.

### Rewards:
- +100 for collecting gold.
- -1000 for falling into a pit or being eaten by the Wumpus.
- +50 for killing the Wumpus (optional action).
- -1 for each move.

## Implemented Algorithms:
1. **Q-Learning (learning-Q):** Classic Q-learning algorithm.
2. **Deep Q-Network (DQN):** Deep Q-learning with a neural network as the Q-function approximator.

## Parameters:
- **Learning Rate:** 0.1
- **Discount Factor (Gamma):** 0.9
- **Exploration Rate (Epsilon):** Starts from 0.1 and decays over time.

## Project Structure:
- **Learning-Q Algorithm:** Implementation and training of Q-learning algorithm.
- **DQN Algorithm:** Implementation and training of Deep Q-Network algorithm.

## Results and Analysis:
- **Policy Performance:** Plot cumulative rewards over episodes for both learning-Q and DQN. Discuss the improvement in agent performance over time.
- **Average Rewards:** Compare average rewards per episode after 1000 episodes for learning-Q and DQN. Analyze which algorithm performs better.
- **Impact of Exploration (Epsilon):** Discuss how the exploration rate epsilon affects the learning process. Compare learning effectiveness when epsilon is high versus when it is low.
- **Learning Efficiency:** Measure how many episodes it took for the learning-Q agent to consistently find gold without falling into pits or being eaten by the Wumpus. Compare learning efficiency between learning-Q and DQN.

## Neural Network Architecture for DQN:
The DQN agent uses a neural network with the following architecture:
- **Input Layer:** Flatten 4x4 grid state into a vector.
- **Hidden Layers:** Dense layers with ReLU activation.
- **Output Layer:** Dense layer with linear activation (Q-values for each action).

This architecture was chosen for its ability to handle complex state-action mappings efficiently, crucial for learning in grid-based environments like the World Wumpus problem.

## Conclusion:
This project provides a comprehensive study of applying reinforcement learning algorithms to solve the World Wumpus problem. It compares the performance of learning-Q and DQN algorithms, explores the impact of exploration on learning, and evaluates their learning efficiency. The neural network architecture used in DQN demonstrates its effectiveness in learning complex behaviors required for navigating and solving grid-based environments.

For detailed implementation and results, refer to the respective directories for learning-Q and DQN implementations.

---

Feel free to fork and modify this repository for your own experimentation and learning with reinforcement learning algorithms!
