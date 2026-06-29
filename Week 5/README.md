# Week 5 – Weighted Graphs & Shortest Path Algorithms
## 7-Day Execution Plan

---

# 🎯 Goal of Week 5

By the end of Week 5, you should be able to:

- Understand weighted graphs
- Understand shortest path problems
- Master Dijkstra's Algorithm
- Learn Bellman-Ford Algorithm
- Understand Floyd-Warshall Algorithm
- Learn Minimum Spanning Trees (MST)
- Implement Prim's Algorithm
- Implement Kruskal's Algorithm
- Understand when to use each shortest path algorithm
- Solve graph optimization problems confidently
- Push all implementations and notes to GitHub

**Estimated Total Time:** **24–30 Hours**

---

# 📚 IITM Lectures Covered

- ✅ 5.1 Shortest Paths in Weighted Graphs
- ✅ 5.2 Dijkstra's Algorithm
- ✅ 5.3 Bellman-Ford Algorithm
- ✅ 5.4 Floyd-Warshall Algorithm
- ✅ 5.5 Minimum Cost Spanning Trees
- ✅ 5.6 Prim's Algorithm
- ✅ 5.7 Kruskal's Algorithm

---

# 🎯 NeetCode Problems

## Priority 1 (Must Solve)

- LC 743 — Network Delay Time
- LC 1584 — Min Cost to Connect All Points

---

## Priority 2

- LC 778 — Swim in Rising Water
- LC 787 — Cheapest Flights Within K Stops

---

# 📅 Day 1 – Weighted Graphs & Dijkstra Introduction

**Estimated Time:** **4 Hours**

## 🎥 Watch

- ✅ Lecture 5.1 – Shortest Paths in Weighted Graphs
- ✅ Lecture 5.2 – Dijkstra's Algorithm

**Video Time:** ~33 min

---

## 📝 Make Notes

Study:

- Weighted Graph
- Edge Weight
- Path Cost
- Relaxation
- Greedy Choice
- Priority Queue
- Min Heap
- Distance Array

---

## 💻 Coding Practice

Implement from scratch:

- Weighted Graph using Adjacency List
- Min Heap using `heapq`
- Priority Queue Operations

---

## 📚 Understand

Difference between:

| Unweighted Graph | Weighted Graph |
|------------------|----------------|
| BFS | Dijkstra |
| Queue | Min Heap |
| Equal Edge Cost | Variable Edge Cost |

---

## 🔁 Revision

Answer:

- Why can't BFS solve weighted shortest path?
- Why does Dijkstra need a Min Heap?
- What is Relaxation?

---

# 📅 Day 2 – Dijkstra Algorithm

**Estimated Time:** **4.5 Hours**

## 💻 Implement

Without looking at notes:

- Dijkstra Algorithm
- Distance Array
- Parent Array
- Path Reconstruction

---

## 🎯 Solve (P1)

### LC 743 — Network Delay Time

Pattern:

- Dijkstra
- Priority Queue

---

## 📝 Notes

Write:

- Brute Force
- Dijkstra Approach
- Complexity
- Common Mistakes
- Pattern Recognition

---

## 📚 Revision

Understand

```
Source

↓

Priority Queue

↓

Nearest Node

↓

Relax Edges

↓

Repeat
```

---

# 📅 Day 3 – Bellman-Ford Algorithm

**Estimated Time:** **3.5 Hours**

## 🎥 Watch

- ✅ Lecture 5.3 – Bellman-Ford Algorithm

**Video Time:** ~18 min

---

## 📝 Make Notes

Study:

- Negative Edge Weights
- Relaxation
- Edge List
- Negative Cycle
- V−1 Iterations

---

## 💻 Coding Practice

Implement:

- Bellman-Ford Algorithm
- Negative Cycle Detection

---

## 📚 Compare

| Dijkstra | Bellman-Ford |
|-----------|--------------|
| Greedy | Dynamic Relaxation |
| No Negative Edges | Supports Negative Edges |
| Faster | Slower |
| Heap | Edge List |

---

## 🧠 Self-Test

Can you explain:

- Why Dijkstra fails on negative weights?
- Why Bellman-Ford runs V−1 times?
- How to detect a negative cycle?

---

# 📅 Day 4 – Floyd-Warshall & All-Pairs Shortest Path

**Estimated Time:** **4 Hours**

## 🎥 Watch

- ✅ Lecture 5.4 – Floyd-Warshall Algorithm

**Video Time:** ~24 min

---

## 📝 Make Notes

Study:

- Dynamic Programming on Graphs
- Intermediate Vertex
- Distance Matrix
- All-Pairs Shortest Path

---

## 💻 Coding Practice

Implement:

- Floyd-Warshall Algorithm
- Distance Matrix Initialization

---

## 📚 Compare Shortest Path Algorithms

| Algorithm | Single Source | All Pairs | Negative Edges |
|------------|---------------|-----------|----------------|
| BFS | ✅ | ❌ | ❌ |
| Dijkstra | ✅ | ❌ | ❌ |
| Bellman-Ford | ✅ | ❌ | ✅ |
| Floyd-Warshall | ❌ | ✅ | ✅ |

---

## 🎯 Solve (P2)

### LC 787 — Cheapest Flights Within K Stops

Pattern:

- Bellman-Ford
- Relaxation

---

## 📝 Pattern Recognition

```
Need Shortest Path

↓

Weighted?

↓

Yes

↓

Negative Weights?

↓

Yes → Bellman-Ford

↓

No

↓

Single Source?

↓

Yes → Dijkstra

↓

All Pairs?

↓

Floyd-Warshall
```

---
# 📅 Day 5 – Minimum Spanning Tree (MST)

**Estimated Time:** **4 Hours**

---

## 🎥 Watch

- ✅ Lecture 5.5 – Minimum Cost Spanning Trees
- ✅ Lecture 5.6 – Prim's Algorithm

**Video Time:** ~33 min

---

## 📝 Make Notes

Study:

- Minimum Spanning Tree (MST)
- Tree vs Graph
- Connected Graph
- Spanning Tree
- Cost of MST
- Greedy Choice
- Cut Property

---

## 💻 Coding Practice

Implement:

- Prim's Algorithm
- Priority Queue
- Visited Array

---

## 🎯 Solve (P1)

### LC 1584 — Min Cost to Connect All Points

**Pattern**

- Minimum Spanning Tree
- Prim's Algorithm

---

## 📝 Notes

Write

- Brute Force
- Prim's Approach
- Complexity
- Common Mistakes
- Pattern Recognition

---

## 📚 Compare

| BFS | Dijkstra | Prim |
|------|-----------|------|
| Traversal | Shortest Path | MST |
| Queue | Min Heap | Min Heap |
| Visit Nodes | Min Distance | Min Cost Edge |

---

# 📅 Day 6 – Kruskal Algorithm & Advanced Graph Practice

**Estimated Time:** **5 Hours**

---

## 🎥 Watch

- ✅ Lecture 5.7 – Kruskal's Algorithm

**Video Time:** ~24 min

---

## 📝 Make Notes

Study:

- Edge Sorting
- Greedy Algorithm
- Cycle Detection
- Union-Find (Preview)
- Connected Components
- MST using Kruskal

---

## 💻 Coding Practice

Implement:

- Kruskal's Algorithm
- Edge Sorting
- Basic Disjoint Set (Preview)

---

## 🎯 Solve (P2)

### LC 778 — Swim in Rising Water

**Pattern**

- Dijkstra
- Priority Queue

---

## 📚 Compare MST Algorithms

| Prim | Kruskal |
|------|----------|
| Vertex Based | Edge Based |
| Min Heap | Sorting |
| Dense Graphs | Sparse Graphs |

---

## 📝 Pattern Recognition

```
Need Minimum Cost?

↓

Need Shortest Path?

↓

Yes

↓

Dijkstra

↓

Need Connect Every Node?

↓

Minimum Spanning Tree

↓

Prim / Kruskal
```

---

## 📚 Interview Questions

Can you explain:

- Difference between Shortest Path and MST?
- Prim vs Kruskal?
- Why does Prim use a Priority Queue?
- Why does Kruskal sort edges?
- Why can't Dijkstra build an MST?

---

# 📅 Day 7 – Weekly Revision & Mock Interview

**Estimated Time:** **4.5 Hours**

---

## 🔁 Re-solve Without Looking

### Priority 1

- [ ] LC 743 — Network Delay Time
- [ ] LC 1584 — Min Cost to Connect All Points

---

### Priority 2

- [ ] LC 778 — Swim in Rising Water
- [ ] LC 787 — Cheapest Flights Within K Stops

---

## 🧠 Self-Test

Without looking at notes answer:

### Dijkstra

- Why Greedy?
- Why Priority Queue?
- Complexity?
- Limitations?

---

### Bellman-Ford

- Why V−1 iterations?
- How to detect a negative cycle?
- Complexity?
- Applications?

---

### Floyd-Warshall

- Why Dynamic Programming?
- Time Complexity?
- Space Complexity?
- Applications?

---

### Prim

- Goal?
- Complexity?
- Dense vs Sparse Graph?

---

### Kruskal

- Why sort edges?
- Why Union-Find?
- Complexity?

---

# 📊 Complexity Cheat Sheet

| Algorithm | Time | Space |
|-----------|------|-------|
| Dijkstra (Heap) | O((V+E) log V) | O(V) |
| Bellman-Ford | O(VE) | O(V) |
| Floyd-Warshall | O(V³) | O(V²) |
| Prim | O(E log V) | O(V) |
| Kruskal | O(E log E) | O(V) |

---

# 📑 Pattern Recognition Cheat Sheet

## Use Dijkstra when

- Weighted Graph
- Positive Weights
- Single Source
- Shortest Path

---

## Use Bellman-Ford when

- Negative Weights
- Need Negative Cycle Detection

---

## Use Floyd-Warshall when

- All-Pairs Shortest Path
- Small Graph
- Dynamic Programming

---

## Use Prim when

- Need Minimum Spanning Tree
- Dense Graph

---

## Use Kruskal when

- Need Minimum Spanning Tree
- Sparse Graph
- Edge List Available

---

# ⚠ Common Interview Mistakes

## Dijkstra

- [ ] Using Queue instead of Priority Queue
- [ ] Forgetting Relaxation
- [ ] Ignoring Outdated Heap Entries
- [ ] Applying on Negative Weights

---

## Bellman-Ford

- [ ] Wrong Number of Iterations
- [ ] Forgetting Negative Cycle Check
- [ ] Incorrect Edge Relaxation

---

## Floyd-Warshall

- [ ] Wrong DP Transition
- [ ] Incorrect Matrix Initialization

---

## Prim

- [ ] Adding Already Visited Nodes
- [ ] Forgetting Visited Array

---

## Kruskal

- [ ] Forgetting Edge Sorting
- [ ] Incorrect Cycle Detection

---

# 📂 GitHub Tasks

Commit

- Week 5 Notes
- Dijkstra Implementation
- Bellman-Ford Implementation
- Floyd-Warshall Implementation
- Prim's Algorithm
- Kruskal's Algorithm
- Graph Optimization Cheat Sheet
- NeetCode Solutions

Suggested Commit Message

```text
Completed IITM PDSA Week 5
```

---

# 📁 Suggested Folder Structure

```
Week 05/
│
├── Notes.md
├── Dijkstra.md
├── BellmanFord.md
├── FloydWarshall.md
├── Prim.md
├── Kruskal.md
│
├── Implementations/
│   ├── weighted_graph.py
│   ├── dijkstra.py
│   ├── bellman_ford.py
│   ├── floyd_warshall.py
│   ├── prim.py
│   └── kruskal.py
│
├── NeetCode/
│   ├── LC743.md
│   ├── LC1584.md
│   ├── LC778.md
│   └── LC787.md
│
└── CheatSheets/
    ├── ShortestPath.pdf
    ├── MST.pdf
    └── GraphOptimization.pdf
```

---

# 📦 Week 5 Deliverables

By the end of Week 5, you should have:

- [ ] Completed all 7 IITM lectures
- [ ] Implemented Dijkstra's Algorithm
- [ ] Implemented Bellman-Ford Algorithm
- [ ] Implemented Floyd-Warshall Algorithm
- [ ] Implemented Prim's Algorithm
- [ ] Implemented Kruskal's Algorithm
- [ ] Solved both P1 problems
- [ ] Solved both P2 problems
- [ ] Created Shortest Path Cheat Sheet
- [ ] Created MST Cheat Sheet
- [ ] Created Graph Optimization Notes
- [ ] Updated GitHub Repository

---

# 🎓 Outcome After Week 5

By the end of Week 5, you will have mastered:

- ✅ Weighted Graphs
- ✅ Shortest Path Problems
- ✅ Dijkstra's Algorithm
- ✅ Bellman-Ford Algorithm
- ✅ Floyd-Warshall Algorithm
- ✅ Minimum Spanning Trees
- ✅ Prim's Algorithm
- ✅ Kruskal's Algorithm
- ✅ Graph Optimization Patterns
- ✅ Priority Queue Applications

You will also have solved **4 graph optimization problems**, building a strong foundation for advanced graph interviews and competitive programming.

---

# 🚀 Ready for Week 6

## Next Topics

- Union-Find (Disjoint Set Union)
- Priority Queues
- Heaps
- Binary Search Trees
- Tree Traversals

## Upcoming NeetCode Problems

- LC 684 — Redundant Connection
- LC 323 — Number of Connected Components
- LC 261 — Graph Valid Tree
- LC 703 — Kth Largest Element in a Stream
- LC 1046 — Last Stone Weight
- LC 973 — K Closest Points to Origin
- LC 295 — Find Median from Data Stream

> **Week 6 Focus:** You'll transition from graph optimization to **fundamental interview data structures** like Heaps, Priority Queues, Union-Find, and Binary Search Trees, which are among the most frequently tested topics in coding interviews.