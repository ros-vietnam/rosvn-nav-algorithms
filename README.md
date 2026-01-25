# ROS Vietnam – Navigation & Motion Planning Algorithms  
`rosvn-nav-algorithms`

> **A research-grade, simulation-first repository for mobile robot navigation and motion planning algorithms in ROS 2.**

---

## 1. Overview

**ROS Vietnam Navigation & Motion Planning Algorithms** is the official algorithmic repository of the **ROS Vietnam** community dedicated to **robot navigation research, evaluation, and open collaboration**.

This repository focuses on:
- Classical navigation algorithms
- Modern optimization-based planners
- Learning-assisted navigation (where applicable)
- Fair comparison under standardized simulation conditions

All algorithms in this repository are developed and evaluated using the **ROS Vietnam Simulation Foundation**.

---

## 2. Philosophy

This repository is built on four core principles:

### 2.1 Algorithm First
- No hardware dependency
- No vendor lock-in
- Clean algorithmic abstractions

### 2.2 Reproducibility
- Deterministic experiments
- Controlled randomness
- Explicit metrics

### 2.3 Comparability
- Same robots
- Same worlds
- Same sensor models
- Same evaluation pipeline

### 2.4 Academic Integrity
- Proper citation
- Transparent assumptions
- No hidden heuristics

> *A navigation algorithm is only as good as the benchmark that evaluates it.*


---

## 3. Scope & Focus

### In Scope
- Global planners
- Local planners
- Trajectory optimization
- Sampling-based planning
- Graph-based planning
- Reactive obstacle avoidance
- Learning-assisted planners (research-oriented)

### Out of Scope
- Full Nav2 stack re-implementation
- Robot bring-up
- Application-specific navigation
- Proprietary algorithms

This repository **complements** Nav2.  
It does **not replace** it.

---

## 4. Algorithm Categories

### 4.1 Classical Planning
- Dijkstra
- A*
- D* / D* Lite
- Theta*
- Hybrid A*

### 4.2 Sampling-Based Planning
- RRT / RRT*
- PRM / PRM*
- BIT*
- Informed RRT*

### 4.3 Optimization-Based Planning
- CHOMP
- STOMP
- Trajectory Rollout
- MPC-based local planners

### 4.4 Reactive & Local Planning
- Dynamic Window Approach (DWA)
- Elastic Band
- Potential Fields (for analysis only)

### 4.5 Learning-Assisted Navigation
- Costmap learning
- Policy refinement
- Hybrid classical + learning planners

---

## 5. Repository Structure

```bash
rosv-navigation-algorithms/
├── README.md 
├── docs/
│ ├── navigation-architecture.md
│ ├── evaluation-metrics.md
│ ├── benchmark-protocol.md
│ └── contribution-guidelines.md
├── planners/
│ ├── global/
│ │ ├── graph_based/
│ │ ├── sampling_based/
│ │ └── optimization_based/
│ ├── local/
│ └── learning_assisted/
├── benchmarks/
│ ├── indoor/
│ ├── outdoor/
│ └── dynamic/
├── evaluation/
│ ├── metrics/
│ ├── scripts/
│ └── visualization/
├── launch/
├── config/
├── tools/
└── .github/

```

---

## 6. Architecture Overview

Each algorithm must be implemented as a **ROS 2–compliant planning module** with:

- Well-defined interfaces
- Parameterized configuration
- Clear input/output contracts
- Deterministic behavior

Algorithms must **not depend on specific robots or maps**.

---

## 7. Simulation Dependency

This repository **depends on**: rosvn-sim-foundation



All experiments must use:
- Identical robot models
- Identical sensor noise profiles
- Identical world definitions

This ensures **fair comparison**.

---

## 8. Evaluation & Metrics

All planners are evaluated using standardized metrics:

### Core Metrics
- Path length
- Time to goal
- Success rate
- Collision count
- Clearance

### Advanced Metrics
- Smoothness
- Energy proxy
- Replanning frequency
- Robustness under noise
