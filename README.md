# 🧭 Solving a Maze using Deep Q-Learning (DQN)

This project demonstrates how to apply **Deep Q-Learning (DQN)** to solve a custom maze environment. Reinforcement Learning is used to train an agent that learns to navigate from the start to the goal through a grid-based maze by maximizing cumulative rewards.

---

## 🎯 Objective

To build an agent that can successfully solve a maze using **Deep Q-Networks**, by learning from interactions with the environment and improving its policy over time without supervision.

---

## 🧠 What is Deep Q-Learning?

**Deep Q-Learning (DQN)** is a reinforcement learning algorithm that combines Q-Learning with deep neural networks. Instead of storing Q-values in a table, it uses a neural network to approximate the Q-function:  
\[
Q(s, a) \approx Q_{\theta}(s, a)
\]

Where:
- `s` is the state (e.g., agent's position in the maze)
- `a` is the action (up, down, left, right)
- `Q(s, a)` is the estimated reward for taking action `a` in state `s`

---

## 🧩 Maze Environment

The maze is represented as a 2D grid where:
- `0` = empty path
- `1` = wall
- `S` = starting point
- `G` = goal

The agent moves in four possible directions: **up, down, left, right**, and receives:
- `+1` reward when reaching the goal
- `-1` penalty for hitting a wall
- `0` for any other step

---

## ⚙️ Project Workflow

1. **Initialize Maze Environment**
   - Create a custom environment with walls, start, and goal positions.

2. **Build Deep Q-Network**
   - Input: current state (flattened grid or agent's coordinates)
   - Output: Q-values for each possible action
   - Architecture: Fully connected neural network (MLP)

3. **Define DQN Agent**
   - Uses an ε-greedy strategy for exploration
   - Experience replay buffer to stabilize learning
   - Target network to reduce oscillations

4. **Train the Agent**
   - Interact with the environment over episodes
   - Update Q-values using the Bellman equation:
     \[
     Q(s, a) = r + \gamma \cdot \max Q(s', a')
     \]
   - Reduce epsilon over time (exploration → exploitation)

5. **Visualize Path**
   - After training, visualize the path the agent takes from start to goal
   - Display episode rewards and learning curves

---

## 🛠️ Libraries Used

- Python
- NumPy
- Matplotlib
- TensorFlow / PyTorch (depending on implementation)
- OpenAI Gym *(if used)* or custom environment

---

## 📈 Sample Outputs

- Agent learns to avoid walls and reach the goal.
- Plots of:
  - Episode rewards over time
  - Moving average of rewards
  - Final policy visualization

---

## 🚀 How to Run

1. Clone this repository.
2. Open the notebook `Solving_a_Maze_using_Deep_Q_Learning_(DQN).ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.
3. Run all cells sequentially.
4. Tune parameters like:
   - `epsilon`, `gamma`, `learning_rate`, `batch_size`
   - Network architecture and training episodes

---

## 🔍 Future Improvements

- Add support for larger or dynamic mazes
- Train using Double DQN or Dueling DQN
- Add animation of agent movements
- Integrate with Gym-like interface

---

## 👨‍💻 Author

**Alaa Shorbaji**  
Artificial Intelligence Instructor – Armed Forces  
Master’s Researcher in Deep Learning & Reinforcement Learning  
GitHub: [your_username]  
LinkedIn: [your_link]

---

## 📜 License

This project is open for educational and research use.
