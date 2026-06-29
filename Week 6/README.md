# Week 6 – Union-Find, Priority Queues, Heaps & Search Trees
## 7-Day Execution Plan

---

# 🎯 Goal of Week 6

By the end of Week 6, you should be able to:

- Understand Disjoint Set Union (Union-Find)
- Master Union by Rank & Path Compression
- Understand Priority Queues
- Master Heap Data Structure
- Learn Heap Applications
- Understand Binary Search Trees (BST)
- Solve Heap, Union-Find and BST interview problems
- Recognize when to use Heap vs BST vs Union-Find
- Push all implementations and solutions to GitHub

**Estimated Total Time:** **28–34 Hours**

---

# 📚 IITM Lectures Covered

- ✅ 6.1 Union-Find Data Structure
- ✅ 6.2 Priority Queues
- ✅ 6.3 Heaps
- ✅ 6.4 Using Heaps in Algorithms
- ✅ 6.5 Search Trees

---

# 🎯 NeetCode Problems

## Priority 1 (Must Solve)

### Union-Find

- LC 684 — Redundant Connection
- LC 323 — Number of Connected Components in an Undirected Graph
- LC 261 — Graph Valid Tree

### Heap

- LC 703 — Kth Largest Element in a Stream
- LC 1046 — Last Stone Weight
- LC 973 — K Closest Points to Origin
- LC 295 — Find Median from Data Stream

---

## Priority 2

- LC 621 — Task Scheduler
- LC 355 — Design Twitter

---

## Priority 3

None

---

# 📅 Day 1 – Union-Find (Disjoint Set Union)

**Estimated Time:** **4.5 Hours**

---

## 🎥 Watch

### ✅ Lecture 6.1 – Union-Find Data Structure

**Video Time:** ~30 min

---

## 📝 Make Notes

Study

- Disjoint Sets
- Parent Array
- Find Operation
- Union Operation
- Union by Rank
- Union by Size
- Path Compression
- Connected Components

---

## 💻 Coding Practice

Implement from scratch

```python
find()

union()

connected()

union by rank

union by size

path compression
```

---

## 📚 Complexity Notes

Know

| Operation | Complexity |
|------------|------------|
| Find | O(α(n)) |
| Union | O(α(n)) |

---

## 🎯 Solve (P1)

### LC 684 — Redundant Connection

Pattern

- Union Find

---

### LC 323 — Number of Connected Components

Pattern

- Union Find

---

## 📝 Notes

For every problem write

- Brute Force
- DFS Solution
- Union Find Solution
- Complexity
- Common Mistakes

---

## 📚 Revision

Understand

```
Initially

1 2 3 4 5

↓

Union

↓

Find Parent

↓

Compress Path

↓

Almost Constant Time
```

---

# 📅 Day 2 – Advanced Union-Find

**Estimated Time:** **4 Hours**

---

## 🎯 Solve (P1)

### LC 261 — Graph Valid Tree

Pattern

- Union Find
- Cycle Detection

---

## 📝 Learn

Difference between

- DFS
- BFS
- Union Find

for

- Cycle Detection
- Connected Components

---

## 💻 Coding Practice

Implement

- Detect Cycle
- Connected Components
- Dynamic Connectivity

---

## 🧠 Self Test

Can you explain

- Why Path Compression works?
- Why Rank is needed?
- Difference between Rank & Size?
- Why Union Find is almost O(1)?

---

## 📚 Revision

Compare

| DFS | Union Find |
|------|------------|
| Traversal | Set Merging |
| Recursive | Parent Array |
| Connected Components | Dynamic Connectivity |

---

# 📅 Day 3 – Priority Queue & Heap Basics

**Estimated Time:** **4.5 Hours**

---

## 🎥 Watch

### ✅ Lecture 6.2 – Priority Queues

### ✅ Lecture 6.3 – Heaps

**Video Time:** ~58 min

---

## 📝 Make Notes

Study

- Priority Queue
- Binary Heap
- Complete Binary Tree
- Max Heap
- Min Heap
- Heap Property
- Parent
- Left Child
- Right Child

---

## 💻 Coding Practice

Implement

```python
heappush()

heappop()

heapify()

peek()

extract min

extract max
```

---

## 📚 Python

Practice

```python
heapq
```

---

## 🎯 Solve (P1)

### LC 703 — Kth Largest Element in a Stream

Pattern

- Min Heap

---

### LC 1046 — Last Stone Weight

Pattern

- Max Heap

---

## 📚 Revision

Know

Heap Operations

| Operation | Complexity |
|------------|------------|
| Insert | O(log n) |
| Delete | O(log n) |
| Peek | O(1) |
| Heapify | O(n) |

---

# 📅 Day 4 – Heap Applications

**Estimated Time:** **5 Hours**

---

## 🎥 Watch

### ✅ Lecture 6.4 – Using Heaps in Algorithms

**Video Time:** ~28 min

---

## 📝 Make Notes

Study

- Top K Problems
- Streaming Problems
- K-way Merge
- Running Median
- Priority Scheduling

---

## 🎯 Solve (P1)

### LC 973 — K Closest Points to Origin

Pattern

- Heap

---

### LC 295 — Find Median from Data Stream

Pattern

- Two Heaps

---

## 🎯 Solve (P2)

### LC 621 — Task Scheduler

Pattern

- Heap
- Greedy

---

## 📝 Pattern Recognition

```
Need Top K

↓

Heap

↓

Need Streaming

↓

Heap

↓

Need Running Median

↓

Two Heaps

↓

Need Highest Priority

↓

Priority Queue
```

---

## 💻 Coding Practice

Without notes implement

- Min Heap
- Max Heap
- Running Median
- K Largest Elements

---

# 📅 Day 5 – Binary Search Trees (BST)

**Estimated Time:** **4.5 Hours**

---

## 🎥 Watch

### ✅ Lecture 6.5 – Search Trees

**Video Time:** ~38 min

---

## 📝 Make Notes

Study

- Binary Search Tree (BST)
- BST Property
- Insertion
- Deletion
- Searching
- Successor
- Predecessor
- Balanced vs Unbalanced Trees

---

## 💻 Coding Practice

Implement

- BST Node
- Insert
- Search
- Delete
- Inorder Traversal
- Preorder Traversal
- Postorder Traversal

---

## 📚 Complexity

| Operation | Average | Worst |
|-----------|---------|--------|
| Search | O(log n) | O(n) |
| Insert | O(log n) | O(n) |
| Delete | O(log n) | O(n) |

---

## 🎯 Solve (P2)

### LC 355 — Design Twitter

Pattern

- Design
- Heap
- HashMap

---

## 📖 Extra Practice (Recommended)

Although officially covered later in NeetCode roadmap, revise these BST problems if already familiar:

- LC 98 — Validate BST
- LC 230 — Kth Smallest Element in BST
- LC 235 — Lowest Common Ancestor of BST

> **Note:** These are preview problems. Their primary study week will come later.

---

# 📅 Day 6 – Mixed Practice & Interview Patterns

**Estimated Time:** **5 Hours**

---

## 🎯 Re-solve Without Looking

### Union Find

- ✅ LC 684
- ✅ LC 323
- ✅ LC 261

---

### Heap

- ✅ LC 703
- ✅ LC 1046
- ✅ LC 973
- ✅ LC 295

---

### Design

- ✅ LC 621
- ✅ LC 355

---

## 📝 Create Cheat Sheets

Prepare one-page notes for

### Union Find

- Find
- Union
- Path Compression
- Union by Rank
- Complexity

---

### Heap

- Min Heap
- Max Heap
- Heapify
- Top-K Pattern
- Running Median

---

### BST

- Properties
- Search
- Insert
- Delete
- Traversals

---

## 💻 Coding Challenge

Without referring to notes implement

- Union Find
- Min Heap
- Max Heap
- BST Insert
- BST Search

---

## 📚 Pattern Recognition

```
Need Dynamic Connectivity

↓

Union Find

↓

Need Top K

↓

Heap

↓

Need Running Median

↓

Two Heaps

↓

Need Ordered Search

↓

Binary Search Tree
```

---

# 📅 Day 7 – Weekly Revision & Mock Interview

**Estimated Time:** **4.5 Hours**

---

## 🔁 Re-solve Without Looking

### Priority 1

- [ ] LC 684 — Redundant Connection
- [ ] LC 323 — Number of Connected Components
- [ ] LC 261 — Graph Valid Tree
- [ ] LC 703 — Kth Largest Element in a Stream
- [ ] LC 1046 — Last Stone Weight
- [ ] LC 973 — K Closest Points to Origin
- [ ] LC 295 — Find Median from Data Stream

---

### Priority 2

- [ ] LC 621 — Task Scheduler
- [ ] LC 355 — Design Twitter

---

# 🧠 Self-Test

Without looking at notes answer:

### Union Find

- Why is Path Compression important?
- Difference between Rank and Size?
- Why is Union Find almost O(1)?
- Where is Union Find used?

---

### Heap

- Difference between Heap and BST?
- Why Heap for Top-K?
- Heapify Complexity?
- Running Median?

---

### BST

- BST Property?
- Average vs Worst Complexity?
- Balanced vs Unbalanced BST?
- Difference between BST and Binary Tree?

---

# 📊 Complexity Cheat Sheet

| Data Structure / Algorithm | Time Complexity |
|----------------------------|-----------------|
| Union Find | O(α(n)) |
| Heap Insert | O(log n) |
| Heap Delete | O(log n) |
| Heap Peek | O(1) |
| Heapify | O(n) |
| BST Search | O(log n) Avg |
| BST Insert | O(log n) Avg |
| BST Delete | O(log n) Avg |

---

# ⚠ Common Interview Mistakes

## Union Find

- [ ] Forgetting Path Compression
- [ ] Incorrect Parent Updates
- [ ] Ignoring Union by Rank
- [ ] Infinite Recursion in Find()

---

## Heap

- [ ] Confusing Min Heap and Max Heap
- [ ] Forgetting Heapify
- [ ] Wrong Heap Size
- [ ] Using Sorting Instead of Heap

---

## BST

- [ ] Violating BST Property
- [ ] Wrong Delete Logic
- [ ] Forgetting Base Case
- [ ] Confusing Binary Tree with BST

---

# 💡 Interview Tips

Ask yourself:

1. Do I need connectivity?
2. Do I need Top-K elements?
3. Do I need dynamic ordering?
4. Do I need minimum/maximum repeatedly?
5. Do I need ordered searching?
6. Is the structure changing frequently?

---

# 📂 GitHub Tasks

Commit

- Week 6 Notes
- Union Find Implementation
- Heap Implementation
- BST Implementation
- Heap Cheat Sheet
- Union Find Cheat Sheet
- BST Cheat Sheet
- NeetCode Solutions

Suggested Commit Message

```text
Completed IITM PDSA Week 6
```

---

# 📁 Suggested Folder Structure

```
Week 06/
│
├── Notes.md
├── UnionFind.md
├── PriorityQueue.md
├── Heap.md
├── BST.md
│
├── Implementations/
│   ├── union_find.py
│   ├── heap.py
│   ├── priority_queue.py
│   ├── bst.py
│   └── traversals.py
│
├── NeetCode/
│   ├── LC684.md
│   ├── LC323.md
│   ├── LC261.md
│   ├── LC703.md
│   ├── LC1046.md
│   ├── LC973.md
│   ├── LC295.md
│   ├── LC621.md
│   └── LC355.md
│
└── CheatSheets/
    ├── UnionFind.pdf
    ├── Heap.pdf
    └── BST.pdf
```

---

# 📦 Week 6 Deliverables

By the end of Week 6, you should have:

- [ ] Completed all 5 IITM lectures
- [ ] Implemented Union Find
- [ ] Implemented Path Compression
- [ ] Implemented Union by Rank
- [ ] Implemented Min Heap
- [ ] Implemented Max Heap
- [ ] Implemented Binary Search Tree
- [ ] Solved all 7 P1 problems
- [ ] Solved all 2 P2 problems
- [ ] Created Union Find Cheat Sheet
- [ ] Created Heap Cheat Sheet
- [ ] Created BST Cheat Sheet
- [ ] Updated GitHub Repository

---

# 🎓 Outcome After Week 6

By the end of Week 6, you will have mastered:

- ✅ Union-Find (Disjoint Set Union)
- ✅ Path Compression
- ✅ Union by Rank
- ✅ Priority Queues
- ✅ Binary Heaps
- ✅ Heap Applications
- ✅ Binary Search Trees
- ✅ Top-K Interview Patterns
- ✅ Streaming Data Problems
- ✅ Dynamic Connectivity Problems

You will also have solved **9 interview-focused NeetCode problems**, covering three of the most frequently tested data structures in coding interviews.

---

# 🚀 Ready for Week 7

## Next Topics

- Balanced Search Trees
- Greedy Algorithms
- Interval Scheduling
- Huffman Coding
- Greedy Strategy Design

## Upcoming NeetCode Problems

- LC 55 — Jump Game
- LC 45 — Jump Game II
- LC 134 — Gas Station
- LC 56 — Merge Intervals
- LC 435 — Non-Overlapping Intervals
- LC 252 — Meeting Rooms
- LC 253 — Meeting Rooms II
- LC 57 — Insert Interval

> **Week 7 Focus:** Learn how to recognize greedy-choice properties and interval scheduling patterns, which are extremely common in technical interviews and optimization problems.