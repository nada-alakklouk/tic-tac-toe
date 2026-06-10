# 🎮 Tic-Tac-Toe with Alpha-Beta Pruning Tree Search AI

An advanced command-line Tic-Tac-Toe game engine powered by an adversarial search artificial intelligence. The game utilizes the optimized **Minimax Algorithm with Alpha-Beta Pruning** to ensure perfect, strategic play. This engine simulates future state-trees to compute optimal moves instantly, making the AI mathematically unbeatable.

---

## 📂 Project Assets & Structure

* 💻 **[View Core Game Notebook](./main.ipynb)** – Interactive Jupyter Notebook containing the full Python layout, recursive evaluation trees, and interactive game loops.
* 🛠️ **Custom Structural Enhancements Added:**
  * **Human-Centric Mapping:** Converted index coordinates into an intuitive 1–9 keypad mapping grid.
  * **Custom Match-Ups:** Integrated options to choose flexible starting turn orders and token configurations ($X$ or $O$).
  * **AI vs. AI Simulation Mode:** Automated algorithmic testing arena where the optimal tree models compete against each other.

---

## 🛠️ The Core AI Algorithm (Technical Breakdown)

Instead of relying on hardcoded heuristics, the AI scans ahead dynamically up to 9 turns ($N \times N$ matrix depth) using a game-tree search representation:

* **Minimax Concept:** Player $X$ acts as the *Maximizer* (seeking a score of +1), while Player $O$ acts as the *Minimizer* (seeking a score of -1).
* **Alpha-Beta Pruning Optimization:** Rather than traversing every possible branch in the game tree, the engine uses two tracking variables:
  * $\alpha$ (Alpha): The best alternative found so far for the maximizer.
  * $\beta$ (Beta): The best alternative found so far for the minimizer.
* **The Cutoff Trigger:** Whenever $\beta \le \alpha$, the algorithm safely discards the remaining sub-branches (Pruning), eliminating unnecessary computations and drastically optimizing recursion speed.

---

## 🚀 Game Architecture & Workflow

1. **Board Representation:** A 2D Python list tracking state attributes: `1` for $X$, `-1` for $O$, and `0` for empty spaces.
2. **Move Coordinate Translation:**
   $$\text{Row} = \frac{\text{Move} - 1}{N}, \quad \text{Column} = (\text{Move} - 1) \pmod N$$
3. **Recursive Scoring Engine (`alpha_beta_search`):** Evaluates recursive future simulation matrices, passing down dynamic threshold arrays to prune unpromising node trajectories.
4. **Execution Interface:** A neat user environment supporting user input validations, clear board updates, and custom victory notification hooks.

---

## 📊 Gameplay Feature Matrix

| Game Mode | Turn Customization | Token Assignment | AI Depth |
| :--- | :--- | :--- | :--- |
| **AI vs. Human** | Choose First / Second | Select $X$ or $O$ | Deep State Scanning (Max 9 Layers) |
| **AI vs. AI** | Fully Automated | Static System Simulation | Zero-Overhead Instant Response |

---

## 👤 Developed by:
* **Nada Alaklook**
* 🔗 [Connect with me on LinkedIn](https://linkedin.com/in/nada-alaklook-725049252)
