# MSc AI Coursework CW1: Graph Search & Genetic Algorithms 🧠

This repository contains my coursework for ECS759P - Artificial Intelligence, part of my MSc AI program at Queen Mary University of London. The assignment consists of two parts:

1. **Route Planning on the London Underground**
2. **Password Cracking using Genetic Algorithms**

---

## 🛤️ Part 1: London Underground Route Planning

### 🔍 Objective
Model and navigate the London Underground system using classic and heuristic-based graph search algorithms.

### 📊 Dataset
`tubedata.csv`: Contains station-to-station links, line numbers, cost in minutes, and fare zones.

### 🧠 Implemented Algorithms
- **Breadth-First Search (BFS)** – finds shortest path by number of steps.
- **Depth-First Search (DFS)** – explores deeply with optional reversed branching.
- **Uniform Cost Search (UCS)** – finds lowest time-cost path, accounting for line changes.
- **BFS with Heuristic** – A*-like method using zone difference heuristics.

### 📈 Output Metrics
- Path length (depth)
- Cumulative time cost
- Number of nodes expanded
- Number of line changes
- Zones traveled

---

## 🔐 Part 2: Password Cracking via Genetic Algorithms

### 🔍 Objective
Simulate password cracking using evolutionary computation techniques.

### 🧬 Key Components
- **Password Generation:** Based on SHA-256 hash of student ID.
- **Fitness Function:** Uses normalized distance from the target password.
- **Genetic Operators:**
  - **Mutation**
  - **Crossover**
  - **Selection based on fitness**

### 🧪 Experimental Results
- Tracks number of reproductions needed to crack the password.
- Averages results over 10 runs to analyze convergence trends.

---

## 🧠 What I Learned
- Practical graph theory through transportation networks.
- Trade-offs between BFS, DFS, UCS, and heuristic searches.
- Data cleaning and graph construction from real-world datasets.
- How genetic algorithms mimic evolution to solve search problems.
- How to design and evaluate fitness landscapes for string matching.

---

## 🛠️ Tools Used
- Python
- Jupyter Notebook
- Libraries: `pandas`, `collections`, `heapq`, `random`, `hashlib`, `numpy`

---

## 👨‍🎓 About Me
I'm Henry Khor, a passionate MSc AI student at QMUL. This coursework strengthens my understanding of algorithmic thinking and computational intelligence — both core to AI research and applications.

---
