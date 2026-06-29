# Week 3 – 7-Day Execution Plan

## 🎯 Goal of Week 3

By the end of Week 3, you should be able to:

- Complete all Week 3 IITM PDSA lectures
- Understand Quicksort and Partitioning
- Understand Python Lists vs Arrays
- Learn Dynamic Arrays and Amortized Analysis
- Understand Python Dictionary Internals
- Master the Two Pointers Pattern
- Learn Prefix & Suffix Array Techniques
- Solve all P1 and P2 NeetCode problems for this week
- Push all notes and solutions to GitHub

**Estimated Total Time:** **24–30 Hours**

---

# 📅 Day 1 – Quicksort & Partitioning

**Estimated Time:** 3.5 Hours

## 🎥 Watch

- ✅ 3.1 Quicksort
- ✅ 3.2 Analysis of Quicksort

**Video Time:** ~28 min

---

## 📝 Make Notes

Write notes on:

- Divide & Conquer
- Pivot Selection
- Partition Algorithm
- Lomuto Partition
- Hoare Partition
- Best / Average / Worst Case
- Stable vs Unstable Sorting

---

## 💻 Coding Practice

Implement from scratch:

- Lomuto Partition
- Hoare Partition
- Recursive Quicksort

---

## 📚 Revision

Compare:

| Algorithm | Best | Average | Worst |
|------------|-------|----------|--------|
| Merge Sort | O(n log n) | O(n log n) | O(n log n) |
| Quick Sort | O(n log n) | O(n log n) | O(n²) |

---

# 📅 Day 2 – Lists vs Arrays

**Estimated Time:** 4 Hours

## 🎥 Watch

- ✅ 3.3 Quicksort Implementation
- ✅ 3.4 Concluding Remarks on Sorting
- ✅ 3.5 Difference Between Lists and Arrays (Theory)

**Video Time:** ~25 min

---

## 📝 Make Notes

Study:

- Dynamic Arrays
- Memory Allocation
- Contiguous Memory
- Array vs List
- Amortized Analysis
- Append Complexity
- Insert Complexity
- Delete Complexity

---

## 💻 Python Practice

Experiment with:

```python
append()
insert()
pop()
remove()
extend()
copy()
```

Measure execution time using `timeit`.

---

## 📚 Revision

Understand why:

```python
list.append()
```

is **Amortized O(1)** instead of **O(n)**.

---

# 📅 Day 3 – Two Pointers (Part 1)

**Estimated Time:** 4.5 Hours

## 🎥 Watch

- ✅ 3.6 Designing a Flexible List
- ✅ 3.7 Implementation of Lists in Python

**Video Time:** ~38 min

---

## 📝 Make Notes

Study:

- Opposite Direction Pointers
- Same Direction Pointers
- Pointer Movement
- When Two Pointers Work

---

## 💻 Solve (P1)

### LC 125 — Valid Palindrome

Pattern:
- Two Pointers

---

### LC 167 — Two Sum II

Pattern:
- Sorted Two Pointers

---

For each problem write:

- Brute Force
- Better
- Optimal
- Complexity
- Mistakes
- Pattern
- Revision Notes

---

# 📅 Day 4 – Two Pointers (Part 2)

**Estimated Time:** 5 Hours

## 💻 Solve (P1)

### LC 15 — 3Sum

Pattern:
- Sorting
- Two Pointers

---

## 💻 Solve (P2)

### LC 11 — Container With Most Water

Pattern:
- Greedy Two Pointers

---

### LC 42 — Trapping Rain Water

Pattern:
- Running Maximum
- Two Pointers

---

## 📝 Create Cheat Sheet

```
Palindrome
      ↓
Two Sum II
      ↓
3Sum
      ↓
Container With Most Water
      ↓
Trapping Rain Water
```

---

# 📅 Day 5 – Dictionary Internals & Prefix/Suffix

**Estimated Time:** 4 Hours

## 🎥 Watch

- ✅ 3.8 Implementation of Dictionaries in Python

**Video Time:** ~16 min

---

## 📝 Make Notes

Study:

- Hash Function
- Collision
- Hash Tables
- Dictionary Complexity
- Set Complexity

---

## 💻 Solve (P1)

### LC 238 — Product of Array Except Self

Pattern:

- Prefix Array
- Suffix Array

---

## 📚 Revision

Understand why division is not allowed.

---

# 📅 Day 6 – Advanced Arrays & Hashing

**Estimated Time:** 4.5 Hours

## 🎥 Watch

- ✅ 3.9 Difference Between Lists and Arrays (Implementation)

**Video Time:** ~15 min

---

## 💻 Solve (P2)

### LC 36 — Valid Sudoku

Pattern:

- Hash Set

---

### LC 128 — Longest Consecutive Sequence

Pattern:

- Hash Set

---

## 💻 Solve (Optional P3)

### LC 271 — Encode and Decode Strings

Pattern:

- String Serialization

---

## 📝 Notes

Prepare:

- Hashing Tricks
- Prefix Tricks
- Two Pointer Tricks

---

# 📅 Day 7 – Weekly Revision

**Estimated Time:** 4 Hours

## 🔁 Re-solve Without Looking

### P1

- ✅ LC 125
- ✅ LC 167
- ✅ LC 15
- ✅ LC 238

---

### P2

- ✅ LC 11
- ✅ LC 42
- ✅ LC 36
- ✅ LC 128

---

### Optional

- LC 271

---

## 🧠 Self-Test

Can you explain:

- Why Quicksort is O(n log n) on average?
- Why can Two Pointers replace HashMaps?
- Why does 3Sum require sorting?
- Why is `append()` amortized O(1)?
- Why is Product Except Self O(n)?
- Why are Python dictionaries average O(1)?
- Why is Longest Consecutive Sequence O(n)?

---

## 📂 GitHub Tasks

Commit:

- Week 3 Notes
- Quicksort Implementation
- Two Pointer Problems
- Prefix/Suffix Notes
- Hash Table Notes
- NeetCode Solutions

Suggested Commit Message:

```text
Completed IITM PDSA Week 3
```

---

# ✅ Week 3 Progress Checklist

## Lectures

- [ ] 3.1 Quicksort
- [ ] 3.2 Analysis of Quicksort
- [ ] 3.3 Quicksort Implementation
- [ ] 3.4 Concluding Remarks
- [ ] 3.5 Lists vs Arrays (Theory)
- [ ] 3.6 Flexible Lists
- [ ] 3.7 Lists in Python
- [ ] 3.8 Dictionaries in Python
- [ ] 3.9 Lists vs Arrays (Implementation)

---

## P1 Problems

- [ ] LC 125 – Valid Palindrome
- [ ] LC 167 – Two Sum II
- [ ] LC 15 – 3Sum
- [ ] LC 238 – Product of Array Except Self

---

## P2 Problems

- [ ] LC 11 – Container With Most Water
- [ ] LC 42 – Trapping Rain Water
- [ ] LC 36 – Valid Sudoku
- [ ] LC 128 – Longest Consecutive Sequence

---

## P3 Problems

- [ ] LC 271 – Encode and Decode Strings (Optional)

---

# 📦 Week 3 Deliverables

- [ ] All 9 lectures completed
- [ ] Quicksort implemented
- [ ] Partition algorithms implemented
- [ ] Dynamic Array notes completed
- [ ] Dictionary internals notes completed
- [ ] Two Pointer cheat sheet prepared
- [ ] Prefix/Suffix notes completed
- [ ] All P1 problems solved
- [ ] All P2 problems solved
- [ ] GitHub updated
- [ ] Ready for Week 4