# Artificial Intelligence Fundamentals 🧠

![AI Banner](https://img.shields.io/badge/Status-Academic_Project-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

This repository contains practical implementations of fundamental concepts in Artificial Intelligence, developed during my Computer Science degree at UNESP. It covers **Search Algorithms** and **Rational Agents**.

---

## 📂 Project 1: Romania Route Optimization (Search)

Solving the classic "Romania Map Problem" (Russell & Norvig) to find the most efficient path between cities (Arad to Bucharest) using heuristic search strategies.

### 🚀 Algorithms Implemented
* **A* Search (A-Star):** Combines the cost to reach the node $g(n)$ and the estimated cost to the goal $h(n)$. Optimal and complete.
* **Greedy Best-First Search:** Selects the path that appears to be closest to the goal based only on the heuristic $h(n)$. Faster but not guaranteed to be optimal.

### 🛠️ Tech Structure
* `graphs.py`: Definitions of the state space (cities and distances).
* `heuristics.py`: Straight-line distance values to Bucharest.
* `a_star.py` & `greedy.py`: Core logic of the search agents.

---

## 📂 Project 2: Vacuum Cleaner Agent (Rational Agents)

A simulation of a Rational Agent in a partially observable environment, based on the **PEAS** framework (Performance, Environment, Actuators, Sensors).

### 🧠 Agent Logic
* **Environment:** Two rooms (Left/Right) that can be either Dirty (1) or Clean (0). Total of 8 possible states.
* **Reflex Agent:** Acts based solely on the current percept (location + dirt status).
* **Memory-Based Improvement:** Implementation of a simple state memory (1 bit) to prevent the agent from looping or wasting energy in fully clean environments.

### 📊 Simulation & Metrics
The notebook simulates the agent's performance over $H$ steps, calculating rewards based on cleanliness ($+\lambda$) and energy costs (movement penalties).

---

## 💻 How to Run

### Running the Search Algorithms
```bash
cd romania-search-algorithms
python main.py
