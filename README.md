# Wumpus World Variant — Lava Cells and the Heat Percept

## Project Overview

This project implements a logic-based AI agent for a modified version of the classic Wumpus World problem. The agent navigates a 5×5 partially observable grid containing three independent hazard types, reasons about its environment using propositional logic, and attempts to retrieve gold and return safely to the starting location.

The primary extension introduced to the standard Wumpus World is the addition of **Lava Cells**, which emit a new percept called **Heat** to orthogonally adjacent cells.

This requires the agent to maintain three independent inference chains simultaneously:

- **Pits** → Breeze percept
- **Wumpus** → Stench percept
- **Lava** → Heat percept

The system remains fully deterministic, explainable, and based on symbolic reasoning principles.

---

# Features

- Propositional logic knowledge base
- Deterministic inference system
- Partial observability
- Custom Lava hazard extension
- Heat percept implementation
- Explainable decision-making
- Safe-cell inference
- Breadth-First Search (BFS) navigation
- Wumpus elimination using a single arrow
- Structured test cases and edge-case handling

---

# Environment Design

## Hazard Types

| Hazard | Percept |
|---|---|
| Wumpus | Stench |
| Pit | Breeze |
| Lava | Heat |

Percepts are generated only in orthogonally adjacent cells.

---

# Agent Objectives

The agent must:

1. Explore the grid safely
2. Infer hazardous locations
3. Retrieve the gold
4. Return to the starting cell
5. Climb out successfully

The agent operates under incomplete knowledge and must reason symbolically about unseen cells.

---

# Technologies Used

- Python
- Google Colab / Jupyter Notebook
- Standard Python libraries only

No external dependencies or installations are required.

---

# How to Run

## Option 1 — Google Colab (Recommended)

1. Open Google Colab:

https://colab.research.google.com

2. Upload the notebook:

```text
WUMPUS_WORLD_VARIANT_LAVA_CELLS_AND_THE_HEAT_PERCEPT.ipynb
```

3. Click:

```text
Runtime → Run all
```

All test cases will execute automatically.

---

## Option 2 — Jupyter Notebook

1. Open the notebook locally using Jupyter
2. Run all cells sequentially from top to bottom

---

# Test Cases

Five labelled test cases are included.

| # | Test Name | Demonstrates | Expected |
|---|---|---|---|
| 1 | Standard Win | Gold retrieval and BFS return | ✅ WIN |
| 2 | Heat Avoidance | Lava inference and safe routing | ✅ WIN |
| 3 | Wumpus Shooting | Wumpus inference and arrow usage | ✅ WIN |
| 4 | Overlapping Percepts | Independent hazard reasoning chains | ✅ WIN |
| 5 | Fallback Strategy | Risk-minimum recovery behavior | ✅ WIN |

---

# System Architecture

The implementation includes:

- Environment representation
- Knowledge Base (KB)
- Inference Engine
- Action Selection Logic
- Test Suite

The agent continuously:
1. Senses percepts
2. Updates the knowledge base
3. Infers safe cells
4. Selects the safest valid action

---

# Ethical Reflection

This project contrasts symbolic AI systems with modern deep reinforcement learning approaches such as DQN and PPO.

The reflection evaluates:
- Transparency
- Explainability
- Accountability
- Predictability
- Bias and fairness
- Ethical trade-offs between symbolic and learned systems

---

# Repository Structure

```text
README.md
WUMPUS_WORLD_VARIANT_LAVA_CELLS_AND_THE_HEAT_PERCEPT.ipynb
MartinsObi_COA207_Portfolio.pdf
```

---

# AI Usage Declaration

ChatGPT was used to assist with:
- debugging Python logic
- refining pseudocode
- improving report clarity and grammar
- reviewing implementation quality

All final implementation decisions and written explanations were reviewed and edited by the author.

---

# Author

Chisom Ashley Obi  
COA207 – Foundations of Artificial Intelligence  
Loughborough University
