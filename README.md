# Q-Learning Maze Solver with Dynamic Fire Obstacles

A Python-based project that implements a reinforcement learning agent to navigate a procedurally generated maze with dynamic fire hazards using Q-Learning. This simulation demonstrates how an intelligent agent can learn to reach a goal state from a start state through trial and error, optimizing rewards while avoiding danger.

---

## 🌐 Overview
This project builds a maze environment and applies the Q-Learning algorithm to teach an agent how to efficiently find a path to the goal while avoiding randomly placed fire hazards.

Key features:
- Dynamic maze generation with adjustable size and wall density.
- Random placement of fire hazards with configurable spacing.
- Q-Learning agent with adjustable learning rate, discount factor, and exploration strategies.
- Visualizations for maze generation, Q-values, and the learned path.

---

## ⚙️ Technologies Used
- Python
- NumPy
- Matplotlib
- Google Colab (for running notebooks)

---

## 🧠 Main Components

### 1. **Maze Generation**
A depth-first search (DFS)-based algorithm creates a perfect maze (no loops) with:
- Clear start `(0,0)` and goal `(size-1, size-1)`.
- Customizable wall density and size.

### 2. **Dynamic Fire Placement**
- Fires (cells with danger) are added randomly, ensuring a minimum distance between fire cells.
- Fire cells affect agent rewards negatively and offer opportunities for jump actions over them.

### 3. **Q-Learning Agent**
Implements standard Q-Learning with:
- Exploration function using an optimistic value with visit counts.
- Action selection with ε-greedy strategy.
- Dynamic update of Q-values.
- Regret tracking per episode.

Rewards:
- Goal = +100
- Fire = -5
- Wall = -10
- Normal move = -1

### 4. **Training & Evaluation**
- Agent trains for configurable episodes.
- Visualization tools show Q-values (arrows & values) and the final optimal path.
- Path testing from start to goal using learned policy.

---

## 📊 Sample Results
- Trained agent successfully navigates from start to goal avoiding fires.
- Regret and reward graphs reflect learning improvements.
- Q-Value visualizations demonstrate exploration.

---

## 📅 Usage
1. Clone or run the notebook via [Google Colab](https://colab.research.google.com/drive/1Qrcq2QpjqAYVUWcR4lsesjnQYrCuSxhc)
2. Execute cells sequentially to:
   - Generate the maze
   - Place dynamic fire
   - Train and test the Q-Learning agent
   - Visualize results

---

## 💡 Future Improvements
- Implement Deep Q-Network (DQN) for larger state spaces.
- Add real-time animation of the agent navigating the maze.
- Introduce stochastic fire spreading behavior for dynamic environments.

---

## 🚀 Authors
This project was developed for AI coursework exploring reinforcement learning principles in complex environments.

---

## 💼 License
This project is open-source under the MIT License.
