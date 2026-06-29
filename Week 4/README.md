# Week 4 – Graph Traversal (BFS, DFS, DAG & Topological Sort)
## 7-Day Execution Plan

---

# 🎯 Goal of Week 4

By the end of Week 4, you should be able to:

- Understand Graph Terminology
- Represent Graphs using Adjacency List and Matrix
- Master Depth First Search (DFS)
- Master Breadth First Search (BFS)
- Understand Connected Components
- Learn Topological Sorting
- Understand Directed Acyclic Graphs (DAG)
- Solve Graph-based NeetCode problems confidently
- Recognize DFS vs BFS patterns
- Push all implementations and solutions to GitHub

**Estimated Total Time:** **26–32 Hours**

---

# 📚 Topics Covered

## IITM Lectures

- ✅ 4.1 Introduction to Graphs
- ✅ 4.2 Representing Graphs
- ✅ 4.3 Breadth First Search (BFS)
- ✅ 4.4 Depth First Search (DFS)
- ✅ 4.5 Applications of BFS and DFS
- ✅ 4.6 Directed Acyclic Graphs (DAG)
- ✅ 4.7 Topological Sorting
- ✅ 4.8 Longest Path in DAG

---

# 🎯 NeetCode Problems

## Priority 1 (Must Solve)

- LC 200 — Number of Islands
- LC 133 — Clone Graph
- LC 695 — Max Area of Island
- LC 207 — Course Schedule
- LC 210 — Course Schedule II

---

## Priority 2

- LC 417 — Pacific Atlantic Water Flow
- LC 130 — Surrounded Regions
- LC 994 — Rotting Oranges
- LC 286 — Walls and Gates
- LC 127 — Word Ladder
- LC 269 — Alien Dictionary

---

## Priority 3

- LC 332 — Reconstruct Itinerary

---

# 📅 Day 1 – Introduction to Graphs

**Estimated Time:** **4 Hours**

---

## 🎥 Watch

### Lecture 4.1

Introduction to Graphs

### Lecture 4.2

Representing Graphs

**Video Time:** ~43 min

---

## 📝 Make Notes

Study

- Graph
- Vertex
- Edge
- Degree
- Directed Graph
- Undirected Graph
- Weighted Graph
- Unweighted Graph
- Cyclic Graph
- Acyclic Graph
- Connected Components

---

## 📖 Learn

Different Graph Representations

### Adjacency Matrix

Advantages

Disadvantages

Complexity

---

### Adjacency List

Advantages

Disadvantages

Complexity

---

## 💻 Coding Practice

Implement

```python
Graph using Adjacency Matrix
```

Implement

```python
Graph using Adjacency List
```

Implement

```python
Add Vertex

Add Edge

Remove Edge
```

---

## 🧠 Complexity Notes

Know

| Operation | Matrix | List |
|------------|--------|------|
| Add Edge | O(1) | O(1) |
| Remove Edge | O(1) | O(E) |
| Check Edge | O(1) | O(V) |
| Space | O(V²) | O(V+E) |

---

## 📚 Revision

Understand

When should you choose

- Matrix

vs

- Adjacency List

---

# 📅 Day 2 – Breadth First Search (BFS)

**Estimated Time:** **4.5 Hours**

---

## 🎥 Watch

### Lecture 4.3

Breadth First Search

**Video Time:** ~34 min

---

## 📝 Make Notes

Understand

- Queue
- Level Order Traversal
- Visited Array
- Connected Components
- Shortest Path in Unweighted Graph

---

## 💻 Implement

From Scratch

```python
BFS using Queue
```

---

## 🎯 Solve (P1)

### LC 200 — Number of Islands

Pattern

- BFS
- Grid Traversal

---

## 🎯 Solve (P2)

### LC 994 — Rotting Oranges

Pattern

- Multi Source BFS

---

## 📝 Notes

For every problem

Write

- Brute Force
- Better
- Optimal
- Complexity
- Pattern
- Common Mistakes

---

## 📚 Revision

Know

Difference between

Tree BFS

and

Graph BFS

---

# 📅 Day 3 – Depth First Search (DFS)

**Estimated Time:** **4.5 Hours**

---

## 🎥 Watch

### Lecture 4.4

Depth First Search

### Lecture 4.5

Applications of BFS and DFS

**Video Time:** ~49 min

---

## 📝 Make Notes

Understand

Recursive DFS

Iterative DFS

Visited Array

Connected Components

Flood Fill

Cycle Detection

---

## 💻 Implement

Recursive DFS

Iterative DFS

DFS using Stack

---

## 🎯 Solve (P1)

### LC 695 — Max Area of Island

Pattern

- DFS

---

### LC 133 — Clone Graph

Pattern

- Graph DFS

---

## 🎯 Solve (P2)

### LC 130 — Surrounded Regions

Pattern

- DFS on Grid

---

### LC 417 — Pacific Atlantic Water Flow

Pattern

- Reverse DFS

---

## 📝 Pattern Recognition

```
Connected Components

↓

Flood Fill

↓

Islands

↓

Area Calculation

↓

Boundary Problems

↓

Multi DFS
```

---

## 🧠 Self Check

Can you explain

- Why DFS uses recursion?
- Why BFS uses Queue?
- Why Visited Array is necessary?
- Difference between Tree DFS and Graph DFS?
- Why Number of Islands is DFS/BFS?
- Difference between Recursive and Iterative DFS?

---
# 📅 Day 4 – Directed Acyclic Graphs (DAG)

**Estimated Time:** **4 Hours**

---

## 🎥 Watch

### ✅ Lecture 4.6 – Introduction to Directed Acyclic Graph (DAG)

**Video Time:** ~8 min

---

## 📝 Make Notes

Study the following concepts:

- Directed Graph
- Directed Cycle
- Directed Acyclic Graph (DAG)
- Source Vertex
- Sink Vertex
- Dependency Graph
- Partial Ordering
- Topological Ordering
- Why DAGs are useful

---

## 📖 Learn

Understand where DAGs are used:

- Task Scheduling
- Course Prerequisites
- Build Systems
- Dependency Resolution
- Package Managers
- CI/CD Pipelines
- Compiler Optimization

---

## 💻 Coding Practice

Implement:

- Detect Cycle in Directed Graph
- Detect Cycle using DFS
- Detect Cycle using Visited + Path Visited Arrays

---

## 🎯 Solve (P1)

### LC 207 — Course Schedule

**Pattern**

- DFS
- Cycle Detection
- DAG

---

## 📝 Notes

For the problem write:

- Problem Statement
- Intuition
- Brute Force
- DFS Solution
- Cycle Detection Logic
- Complexity
- Common Mistakes

---

## 📚 Revision

Understand

```
Directed Graph

↓

Cycle?

↓

Yes → Cannot Finish

↓

No

↓

Topological Ordering Exists
```

---

# 📅 Day 5 – Topological Sorting

**Estimated Time:** **4.5 Hours**

---

## 🎥 Watch

### ✅ Lecture 4.7 – Topological Sorting

### ✅ Lecture 4.8 – Longest Path in DAG

**Video Time:** ~31 min

---

## 📝 Make Notes

Study

- Topological Sort
- DFS Topological Sort
- Kahn's Algorithm
- In-degree
- Out-degree
- Dependency Graph
- Longest Path in DAG

---

## 💻 Coding Practice

Implement from scratch

- DFS Topological Sort
- Kahn's Algorithm (BFS)
- Calculate In-degree Array

---

## 🎯 Solve (P1)

### LC 210 — Course Schedule II

Pattern

- Topological Sorting

---

## 🎯 Solve (P2)

### LC 269 — Alien Dictionary

Pattern

- Graph Construction
- Topological Sort

---

## 📝 Pattern Notes

Understand

```
Dependencies

↓

Graph

↓

In-degree

↓

Queue

↓

Topological Order
```

---

## 📚 Revision

Compare

| DFS Topological Sort | Kahn's Algorithm |
|----------------------|------------------|
| Uses recursion | Uses queue |
| Reverse postorder | In-degree based |
| Easy to implement | Easy to detect cycle |

---

# 📅 Day 6 – Graph Pattern Practice

**Estimated Time:** **5 Hours**

---

## 🎯 Solve Remaining Problems

### ✅ LC 286 — Walls and Gates

Pattern

- Multi Source BFS

---

### ✅ LC 127 — Word Ladder

Pattern

- BFS
- Shortest Path

---

### ✅ LC 332 — Reconstruct Itinerary (P3)

Pattern

- Eulerian Path
- DFS

---

## 📝 Create Graph Cheat Sheet

Prepare notes for

### BFS Recognition

When should you use BFS?

- Shortest Path
- Minimum Moves
- Level Order
- Multi Source Problems
- Unweighted Graph

---

### DFS Recognition

When should you use DFS?

- Connected Components
- Cycle Detection
- Backtracking
- Flood Fill
- Island Problems

---

### Topological Sort Recognition

Use when

- Dependencies
- Scheduling
- Course Problems
- Build Order

---

## 💻 Coding Practice

Without looking at notes implement

- BFS Template
- DFS Recursive
- DFS Iterative
- Graph Class
- Queue-based Traversal

---

## 📚 Interview Practice

For every solved graph problem answer:

- Why BFS?
- Why DFS?
- Can BFS solve it?
- Can DFS solve it?
- Time Complexity?
- Space Complexity?

---

# 📅 Day 7 – Weekly Revision & Mock Interview

**Estimated Time:** **4.5 Hours**

---

## 🔁 Re-solve Without Looking

### Priority 1

- [ ] LC 200 — Number of Islands
- [ ] LC 133 — Clone Graph
- [ ] LC 695 — Max Area of Island
- [ ] LC 207 — Course Schedule
- [ ] LC 210 — Course Schedule II

---

### Priority 2

- [ ] LC 417 — Pacific Atlantic Water Flow
- [ ] LC 130 — Surrounded Regions
- [ ] LC 994 — Rotting Oranges
- [ ] LC 286 — Walls and Gates
- [ ] LC 127 — Word Ladder
- [ ] LC 269 — Alien Dictionary

---

### Priority 3

- [ ] LC 332 — Reconstruct Itinerary

---

# 🧠 Self-Test

Without looking at notes answer:

### Graph Basics

- What is a graph?
- Difference between directed and undirected graph?
- What is a DAG?
- What is a connected component?

---

### BFS

- Why Queue?
- Complexity?
- When should BFS be preferred?
- Multi Source BFS?

---

### DFS

- Recursive vs Iterative?
- Why Visited Array?
- How is Cycle Detection performed?

---

### Topological Sort

- When does it exist?
- Why only DAG?
- DFS vs Kahn's Algorithm?
- Real-world applications?

---

### Complexity

Know complexity of

| Algorithm | Time | Space |
|-----------|------|-------|
| BFS | O(V+E) | O(V) |
| DFS | O(V+E) | O(V) |
| Topological Sort | O(V+E) | O(V) |

---

# 📂 GitHub Tasks

Commit

- Week 4 Notes
- Graph Implementations
- BFS Template
- DFS Template
- Topological Sort Template
- NeetCode Solutions
- Graph Cheat Sheet

Suggested Commit Message

```text
Completed IITM PDSA Week 4
```

---

# 📖 Additional Reading (Optional)

If time permits, briefly explore:

- Union Find (Preview for Week 6)
- Dijkstra's Algorithm (Preview for Week 5)
- Graph Coloring
- Bipartite Graphs

Do **not** spend more than 30–45 minutes. These topics will be covered in later weeks.

---

# 📊 Week 4 Progress Checklist

## 🎥 IITM Lectures

- [ ] 4.1 Introduction to Graphs
- [ ] 4.2 Representing Graphs
- [ ] 4.3 Breadth First Search (BFS)
- [ ] 4.4 Depth First Search (DFS)
- [ ] 4.5 Applications of BFS & DFS
- [ ] 4.6 Directed Acyclic Graphs (DAG)
- [ ] 4.7 Topological Sorting
- [ ] 4.8 Longest Path in DAG

---

# 💻 Graph Implementations

## Graph Representation

- [ ] Adjacency Matrix
- [ ] Adjacency List

---

## Traversal Algorithms

- [ ] BFS
- [ ] DFS (Recursive)
- [ ] DFS (Iterative)

---

## Graph Algorithms

- [ ] Connected Components
- [ ] Cycle Detection (Directed)
- [ ] Topological Sort (DFS)
- [ ] Topological Sort (Kahn's Algorithm)

---

# 🎯 P1 Problems (Must Solve)

- [ ] LC 200 — Number of Islands
- [ ] LC 133 — Clone Graph
- [ ] LC 695 — Max Area of Island
- [ ] LC 207 — Course Schedule
- [ ] LC 210 — Course Schedule II

---

# ⭐ P2 Problems

- [ ] LC 417 — Pacific Atlantic Water Flow
- [ ] LC 130 — Surrounded Regions
- [ ] LC 994 — Rotting Oranges
- [ ] LC 286 — Walls and Gates
- [ ] LC 127 — Word Ladder
- [ ] LC 269 — Alien Dictionary

---

# 📚 P3 Problems

- [ ] LC 332 — Reconstruct Itinerary

---

# 📝 Notes Checklist

Create notes for:

- [ ] Graph Terminology
- [ ] Adjacency Matrix
- [ ] Adjacency List
- [ ] BFS
- [ ] DFS
- [ ] Connected Components
- [ ] Flood Fill
- [ ] DAG
- [ ] Cycle Detection
- [ ] Topological Sorting
- [ ] Longest Path in DAG

---

# 📑 Cheat Sheets

Prepare one-page cheat sheets for:

- [ ] Graph Representation
- [ ] BFS Template
- [ ] DFS Template
- [ ] Graph Traversal Complexity
- [ ] Topological Sort
- [ ] Cycle Detection

---

# 🧠 Graph Pattern Recognition

## Use BFS when...

- Need the shortest path in an **unweighted** graph
- Need level-order traversal
- Problem asks for **minimum number of moves**
- Multi-source expansion is required
- Distance from a source is required

### Typical Keywords

- Minimum Steps
- Shortest Path
- Fewest Moves
- Multi-source
- Level Order

---

## Use DFS when...

- Need to explore every path
- Need connected components
- Need flood fill
- Need cycle detection
- Need recursion/backtracking

### Typical Keywords

- Connected Components
- Islands
- Area
- Reachability
- Explore All

---

## Use Topological Sort when...

- There are dependencies
- Tasks must be completed in order
- Courses have prerequisites
- Build order matters
- DAG is involved

### Typical Keywords

- Dependency
- Before
- After
- Prerequisite
- Schedule
- Ordering

---

# 🌳 Graph Decision Tree

```text
Graph Problem

│

├── Need Shortest Path?

│       │

│       ├── Unweighted

│       │      ↓

│       │     BFS

│       │

│       └── Weighted

│              ↓

│        Week 5 (Dijkstra)

│

├── Need Connected Components?

│        ↓

│      DFS / BFS

│

├── Need Area / Flood Fill?

│        ↓

│       DFS

│

├── Need Dependency Order?

│        ↓

│ Topological Sort

│

├── Need Cycle Detection?

│        ↓

│ DFS / Kahn's Algorithm

│

└── Need Explore Everything?

        ↓

       DFS
```

---

# ⚠ Common Interview Mistakes

## BFS

❌ Forgetting Visited Array

❌ Marking Visited after Pop instead of Push

❌ Using Stack instead of Queue

❌ Revisiting Nodes

---

## DFS

❌ Infinite Recursion

❌ Missing Base Case

❌ Forgetting Visited Array

❌ Stack Overflow on Deep Graphs

---

## Topological Sort

❌ Running on Cyclic Graph

❌ Forgetting In-degree Calculation

❌ Incorrect Queue Initialization

---

# 💡 Interview Tips

For every graph problem ask yourself:

1. Is this a Graph or Grid problem?
2. Can I model it as a graph?
3. Is BFS better?
4. Is DFS better?
5. Is it a DAG?
6. Is Topological Sort required?
7. Is there a shortest path?
8. Is the graph weighted?

---

# 📂 GitHub Folder Structure

```
Week 04/
│
├── Notes.md
├── BFS.md
├── DFS.md
├── DAG.md
├── TopologicalSort.md
│
├── Implementations/
│   ├── adjacency_matrix.py
│   ├── adjacency_list.py
│   ├── bfs.py
│   ├── dfs_recursive.py
│   ├── dfs_iterative.py
│   ├── cycle_detection.py
│   ├── topo_sort_dfs.py
│   └── kahn_algorithm.py
│
├── NeetCode/
│   ├── LC200.md
│   ├── LC133.md
│   ├── LC695.md
│   ├── LC207.md
│   ├── LC210.md
│   ├── LC417.md
│   ├── LC130.md
│   ├── LC994.md
│   ├── LC286.md
│   ├── LC127.md
│   ├── LC269.md
│   └── LC332.md
│
└── CheatSheets/
    ├── BFS.pdf
    ├── DFS.pdf
    └── GraphPatterns.pdf
```

---

# 📦 Week 4 Deliverables

By the end of Week 4, you should have:

- [ ] Completed all 8 IITM lectures
- [ ] Implemented Graph using Adjacency Matrix
- [ ] Implemented Graph using Adjacency List
- [ ] Implemented BFS
- [ ] Implemented DFS (Recursive)
- [ ] Implemented DFS (Iterative)
- [ ] Implemented Cycle Detection
- [ ] Implemented DFS Topological Sort
- [ ] Implemented Kahn's Algorithm
- [ ] Solved all 5 P1 problems
- [ ] Solved all 6 P2 problems
- [ ] Solved the optional P3 problem
- [ ] Created Graph Notes
- [ ] Created BFS Cheat Sheet
- [ ] Created DFS Cheat Sheet
- [ ] Created Topological Sort Cheat Sheet
- [ ] Updated GitHub Repository

---

# 🎓 Outcome After Week 4

By the end of Week 4, you will have mastered:

- ✅ Graph Representation
- ✅ Graph Traversal
- ✅ BFS Pattern
- ✅ DFS Pattern
- ✅ Flood Fill Pattern
- ✅ Connected Components
- ✅ Directed Graphs
- ✅ DAG Concepts
- ✅ Cycle Detection
- ✅ Topological Sorting
- ✅ Dependency Resolution
- ✅ Graph Interview Patterns

You will also have solved **12 graph-focused NeetCode problems**, giving you a solid foundation before moving to **Week 5 (Weighted Graphs, Dijkstra's Algorithm, Bellman-Ford, Floyd-Warshall, and Minimum Spanning Trees)**.

---

# 🚀 Ready for Week 5

### Next Topics

- Shortest Path in Weighted Graphs
- Dijkstra's Algorithm
- Bellman-Ford Algorithm
- Floyd-Warshall Algorithm
- Minimum Spanning Tree
- Prim's Algorithm
- Kruskal's Algorithm

### Upcoming NeetCode Problems

- LC 743 — Network Delay Time
- LC 778 — Swim in Rising Water
- LC 787 — Cheapest Flights Within K Stops
- LC 1584 — Min Cost to Connect All Points

> **Week 5 Focus:** Transition from **graph traversal** to **graph optimization**, where you'll learn how to find optimal paths and build minimum-cost networks—core concepts used in routing systems, maps, networking, and many technical interviews.