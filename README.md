# IITM PDSA × NeetCode 150 Complete Roadmap

*A week-by-week study system mapping the IIT Madras BS Data Science "Programming, Data Structures and Algorithms using Python" (PDSA) course to all 150 NeetCode interview problems.*

---

## Legend

| Symbol / Term | Meaning |
|---|---|
| **P1** | Must solve immediately after the relevant lecture/week. Core, non-negotiable. |
| **P2** | Should solve soon after P1s are done. Reinforces the same pattern. |
| **P3** | Revision / later / optional / extra. Useful but not urgent. |
| **Must Solve** | Directly tests the week's core idea — skipping it leaves a real gap. |
| **Good to Solve** | Strengthens the pattern, slightly different angle or twist. |
| **Later / Optional** | Valid practice, but can be deferred without risk. |
| **Revision Only** | Best used as a quick re-check before interviews, not first-pass learning. |
| **Direct Fit** | The problem's core technique is explicitly taught in that IITM lecture. |
| **Secondary Fit** | The problem touches the topic but leans on an idea taught elsewhere too. |
| **Extra** | Not naturally derived from IITM theory; included for interview completeness. |
| ⚠️ **Common Trap** | A mistake pattern that repeatedly costs marks/time. |
| 💡 **Pattern Recognition** | The signal in the problem statement that should trigger this technique. |
| 📌 **Revision Tip** | What to specifically re-derive (not just re-read) before an interview. |
| ☑️ | Checkbox for progress tracking — usable directly in Markdown editors/Obsidian/Notion. |

**Difficulty** follows LeetCode's own labels (Easy / Medium / Hard).
**Interview Value** is independent of difficulty — some Easy problems (e.g. LC 1, LC 121) have very high interview value because they appear constantly; some Hard problems (e.g. LC 312 Burst Balloons) have lower real-world interview value despite their difficulty.

---

## How to Use This Handbook

1. **Go week by week, not topic by topic.** The handbook is sequenced to match IITM PDSA's lecture order. Don't jump ahead to Dynamic Programming in Week 2 just because it's exciting — the earlier weeks build the muscle (recursion discipline, complexity analysis, list/array internals) that DP depends on.
2. **After each lecture, solve only the P1 problems mapped to it first.** Do not move to P2 until every P1 for that lecture is solved *without* looking at the solution.
3. **P2 problems are same-day or next-day reinforcement.** They exist so the pattern doesn't fade after one exposure.
4. **P3 problems are explicitly deferred.** Do not feel behind for skipping them on first pass — revisit them during the dedicated revision phase (see Appendix D).
5. **Every problem entry tells you *why* it is placed where it is.** If a mapping looks unusual (e.g. a DP problem appearing under Week 4 Graphs), read the "Why here" field — it is intentional, not a misclassification.
6. **Use the checkboxes in Appendix C as your master tracker.** Tick a box only when you can solve the problem cleanly in under the expected time, from scratch, without hints.
7. **Treat the "Extra / Later / Revision" sections honestly.** Some NeetCode problems (most Design questions, some advanced DP, some specialized structures) do not map cleanly onto IITM's theory sequence. They are still valuable — they are placed in Appendix E and cross-referenced, with an explanit of what they add even though they're "extra."
8. **Before any mock interview or real interview**, run through Appendix D's "Fast Revision Map" rather than re-reading the whole handbook.

---

# Week 1 — Python Foundations & Why Efficiency Matters

**Lectures covered:** 1.1 – 1.12
**Main topic:** Python language mechanics (not DSA patterns yet) — syntax recap, OOP, exceptions, timing code, and the conceptual motivation for studying efficiency.
**DSA pattern introduced:** None directly. This week is **prerequisite infrastructure**, not pattern-teaching.

> **Important:** Week 1 of IITM PDSA does not teach a DSA pattern — it builds the Python fluency (data types, control flow, classes, exception handling, timing) that every later week assumes you already have. Because of this, **no NeetCode problem is "must solve" against Week 1 specifically.** Forcing a mapping here would violate the instruction not to force unnatural fits. Instead, Week 1's job is to make sure you *can* write clean Python fast enough that pattern-learning in Weeks 2–11 isn't slowed down by syntax friction.

## Lecture 1.1 — Introduction to Jupyter Notebooks and Google Colab
### What this lecture teaches
Tooling setup: running Python in a notebook environment, cell execution order, markdown cells for notes.
### Core DSA ideas
None. Pure tooling.
### Relevant NeetCode problems
None. Use this lecture only to set up your own LeetCode/local Python environment (VS Code, or LeetCode's online editor) so you're not fighting tooling later.

## Lecture 1.2 — Implementation of Python Codes (Part 01)
### What this lecture teaches
Translating simple logic into runnable Python: variables, basic I/O, simple loops.
### Core DSA ideas
None directly — this is where you should make sure `for`, `while`, `range`, and basic list indexing are second nature.
### Relevant NeetCode problems
None mapped directly. **Optional self-check (not a NeetCode 150 problem):** write a function that sums a list and one that reverses a string manually, just to confirm comfort with loops/indexing before Week 2 begins.

## Lecture 1.3 — Python Recap I
### What this lecture teaches
Core data types: integers, floats, strings, booleans, basic operators, type coercion rules.
### Core DSA ideas
None directly, but string immutability (covered here) becomes directly relevant the moment you hit string-heavy problems in Week 3 (Encode and Decode Strings) and onward.
### Relevant NeetCode problems
None yet — flagged for later.

## Lecture 1.4 — Python Recap II
### What this lecture teaches
Lists, tuples, dictionaries, sets — Python's built-in container types and their basic operations.
### Core DSA ideas
This is the single most important lecture in Week 1 for NeetCode readiness. Dictionaries and sets here are the literal implementation vehicles for **every Hashing pattern problem in Week 3's NeetCode mapping.**
### Relevant NeetCode problems
**None solved yet** (the pattern work starts properly in Week 3 once IITM formally covers list/dict internals), but this lecture is the conceptual prerequisite for:
- LC 217 — Contains Duplicate
- LC 242 — Valid Anagram
- LC 1 — Two Sum

📌 **Revision Tip:** Before starting Week 3's hashing problems, re-confirm you know Python dict/set time complexity (O(1) average for get/set/contains) — IITM proves this later in Week 2–3, but you should *use* it correctly here first.

## Lecture 1.5 — Python Recap III
### What this lecture teaches
Functions, default arguments, `*args`/`**kwargs`, scope rules, basic functional patterns (map/filter/lambda).
### Core DSA ideas
None directly DSA-specific, but recursion (used constantly from Week 2 onward — Merge Sort, Quicksort, DFS, DP) depends on a clean understanding of function call semantics taught here.
### Relevant NeetCode problems
None mapped directly.

## Lecture 1.6 — Exception Handling
### What this lecture teaches
`try` / `except` / `finally`, raising custom exceptions, defensive coding.
### Core DSA ideas
None directly. Useful for production code; rarely tested explicitly in interview DSA problems (interviewers usually want you to *avoid* needing exceptions via correct bounds-checking instead).
### Relevant NeetCode problems
None.

## Lecture 1.7 — Classes and Objects
### What this lecture teaches
OOP fundamentals: `class`, `__init__`, instance methods, attributes, basic encapsulation.
### Core DSA ideas
**Directly relevant later.** Every linked-list, tree, and trie problem in this handbook requires you to define a `Node`/`TreeNode`/`ListNode` class exactly as taught here. This lecture is a quiet prerequisite for all of Weeks 4–6's structural problems even though no NeetCode problem is solved yet.
### Relevant NeetCode problems
None solved now, but conceptually required before:
- LC 206 — Reverse Linked List
- LC 226 — Invert Binary Tree
- LC 208 — Implement Trie (Prefix Tree)

## Lecture 1.8 — Implementation of Python Codes (Part 02)
### What this lecture teaches
More applied coding practice combining recap topics into small programs.
### Core DSA ideas
None new.
### Relevant NeetCode problems
None.

## Lecture 1.9 — Timing Our Code
### What this lecture teaches
Using `time` module / `timeit` to empirically measure runtime of code — the practical companion to Week 2's theoretical Big-O.
### Core DSA ideas
Empirical performance measurement — directly motivates *why* asymptotic analysis (Week 2) matters.
### Relevant NeetCode problems
None directly, but this is good practice to apply once you start comparing brute-force vs optimized solutions later (e.g., timing your O(n²) Two Sum brute force vs the O(n) hashmap version).

## Lecture 1.10 — Implementation of Python Codes (Part 03)
### What this lecture teaches
Continued applied practice.
### Core DSA ideas
None new.
### Relevant NeetCode problems
None.

## Lecture 1.11 — Why Efficiency Matters?
### What this lecture teaches
The conceptual motivation for the entire course: why a "working" solution isn't good enough, and why scale exposes bad algorithms.
### Core DSA ideas
This is the philosophical anchor for every "Time Complexity" field you will see in every problem entry from Week 2 onward.
### Relevant NeetCode problems
None directly, but **conceptually this is the lecture that justifies why this entire handbook insists on stating Big-O for every single problem.**

## Lecture 1.12 — Implementation of Python Codes (Part 04)
### What this lecture teaches
Final applied Python practice before algorithmic content begins in Week 2.
### Core DSA ideas
None new.
### Relevant NeetCode problems
None.

### What should be solved immediately after Week 1
Nothing from NeetCode 150 — Week 1 has no P1/P2/P3 problems. Use Week 1 only to firm up Python fluency.

### What should be solved during revision
N/A for Week 1.

### What should be left for later
All hashing-pattern problems (LC 217, 242, 1, 49, 347, 238, 36, 271, 128) are intentionally deferred to **Week 3**, where IITM formally covers dictionaries/lists as data structures with stated complexity guarantees — solving them earlier is possible but loses the "why it's O(1)" grounding this handbook is built around.

---

# Week 2 — Algorithm Analysis, Searching & Sorting

**Lectures covered:** 2.1 – 2.9
**Main topic:** Big-O analysis, linear search, and the first three sorting algorithms (Selection, Insertion, Merge).
**DSA pattern introduced:** Complexity analysis as a formal tool; Hashing (enabled by Week 1's dict/set, now given complexity backing); Merge Sort as the gateway to Divide & Conquer (revisited in Week 8).

## Lecture 2.1 — Analysis of Algorithms
### What this lecture teaches
Formal definition of time complexity, worst-case vs average-case, why we count "basic operations."
### Core DSA ideas
Big-O notation, asymptotic growth.
### Relevant NeetCode problems
This is the lecture where you should *justify* — not just state — every complexity field that follows in this handbook. No new problems here; apply the lens going forward.

## Lecture 2.2 — Comparing Orders of Magnitude
### What this lecture teaches
Relative growth rates: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ).
### Core DSA ideas
This hierarchy is exactly what you use to decide, for every problem below, whether brute force is "good enough" or needs optimizing.
### Relevant NeetCode problems
None new, but directly informs interpretation of all problems from here on.

## Lecture 2.3 — Calculating Complexity: Examples
### What this lecture teaches
Worked examples of deriving Big-O from code (nested loops, sequential statements).
### Core DSA ideas
Practical complexity derivation — the skill tested whenever an interviewer asks "what's the time complexity of your solution?"

### Relevant NeetCode problems

#### LC 217 — Contains Duplicate
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 2 → Lecture 2.3/2.4 → Hashing → Frequency/Existence Check
- **Pattern:** Hash Set membership check
- **Why here:** The canonical "compare brute force O(n²) vs hash set O(n)" teaching example — directly exercises the complexity-comparison lens from 2.2/2.3.
- **Prerequisites:** Python `set` from Lecture 1.4; complexity comparison from 2.2.
- **Best approach:** Insert each element into a set; if an element is already present, return True.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:**
  - Using nested loops (O(n²)) without realizing a set solves it in one pass.
  - Forgetting that sorting first (O(n log n)) is also valid but strictly worse than hashing here.
- **Interview Value:** Medium (too simple to be the main question, but a common warm-up).
- **Related Problems:** LC 1, LC 49, LC 242.
- **Notes:** First problem where you should explicitly state both the brute-force and optimal complexity out loud — this habit is rewarded in interviews.

#### LC 1 — Two Sum
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 2 → Lecture 2.3/2.4 → Hashing → Single-pass lookup
- **Pattern:** Hash Map (value → index)
- **Why here:** The single most-referenced interview problem; demonstrates trading O(n²) brute force for O(n) using a hashmap, the core lesson of this lecture block.
- **Prerequisites:** Dict basics (1.4), complexity comparison (2.2).
- **Best approach:** One pass, store `value: index` in a dict; for each number check if `target - num` already exists.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:**
  - Checking `target - num` against the dict *before* inserting current/duplicates correctly (off-by-one logic errors with duplicate values).
  - Returning indices in the wrong order.
- **Interview Value:** High — often the literal first question in screening rounds.
- **Related Problems:** LC 167 (sorted variant), LC 15 (3Sum extension), LC 217.
- **Notes:** 💡 **Pattern Recognition:** "two numbers that sum to target" in an unsorted array → hashmap. If sorted, prefer two pointers (see LC 167 in Week 3).

#### LC 242 — Valid Anagram
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 2 → Lecture 2.3/2.4 → Hashing → Frequency Counting
- **Pattern:** Hash Map frequency counter
- **Why here:** Reinforces frequency-counting immediately after Two Sum's lookup-counting; both rely on the same dict mechanics taught conceptually in 1.4 and complexity-justified in 2.3.
- **Prerequisites:** Dict basics, string iteration.
- **Best approach:** Build a frequency dict for each string, compare; or sort both strings and compare (less optimal).
- **Time Complexity:** O(n) with hashmap; O(n log n) if sorting.
- **Space Complexity:** O(1) effectively (bounded alphabet) or O(n) generally.
- ⚠️ **Common Mistakes:**
  - Forgetting to check string length equality first as a fast fail.
  - Off-by-one in decrementing counts (forgetting to handle a count going negative as "false").
- **Interview Value:** Medium.
- **Related Problems:** LC 49 (Group Anagrams), LC 217.
- **Notes:** 📌 **Revision Tip:** Re-derive both the hashmap and sort-based approach from memory; interviewers sometimes ask for the alternative.

#### LC 49 — Group Anagrams
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 2 → Lecture 2.3/2.4 → Hashing → Grouping by Canonical Key
- **Pattern:** Hash Map with composite/sorted key
- **Why here:** Direct generalization of LC 242 — instead of comparing two strings, you group N strings by a canonical signature.
- **Prerequisites:** LC 242 solved first; tuple/string hashing as dict keys.
- **Best approach:** For each string, compute a key (sorted string, or 26-length count tuple), append to `defaultdict(list)[key]`.
- **Time Complexity:** O(n · k log k) with sorting (n strings, k = avg length); O(n · k) with count-based key.
- **Space Complexity:** O(n · k)
- ⚠️ **Common Mistakes:**
  - Using a list as a dict key (unhashable) instead of a tuple or string.
  - Choosing sorted-string keys when count-tuples would be asymptotically faster for long strings.
- **Interview Value:** High — a very common "next step" after Two Sum/Valid Anagram in interviews.
- **Related Problems:** LC 242, LC 347.
- **Notes:** Good problem to practice `collections.defaultdict`.

#### LC 347 — Top K Frequent Elements
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 2 → Lecture 2.3 (complexity tradeoffs) → Hashing + Bucket Sort
- **Pattern:** Hash Map frequency count + Bucket Sort (or Heap, see Week 6 alternative)
- **Why here:** Forces an explicit complexity comparison: heap-based O(n log k) vs bucket-sort O(n) — exactly the kind of tradeoff Lecture 2.2/2.3 trains you to reason about.
- **Prerequisites:** Frequency counting (LC 242), basic understanding that array-index buckets can replace a heap when frequency is bounded by n.
- **Best approach:** Count frequencies, then place each element into a bucket array indexed by frequency (0..n), and read off the top k from the end.
- **Time Complexity:** O(n) with bucket sort.
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:**
  - Defaulting straight to a heap (O(n log k)) and missing the optimal O(n) bucket approach — fine for first pass, but revisit.
  - Off-by-one in bucket index sizing.
- **Interview Value:** High.
- **Related Problems:** LC 215 (Kth Largest via Quick Select, Week 8), LC 973 (Heap, Week 6).
- **Notes:** 📌 **Revision Tip:** Re-solve this once more after Week 6 (Heaps) and once more after Week 8 (Quick Select) — it has three valid optimal-ish approaches and seeing all three is high-value.

## Lecture 2.4 — Searching in a List
### What this lecture teaches
Linear search and its O(n) complexity; sets up the contrast for Binary Search (deferred to Week 7's Search Trees / later binary search problems).
### Core DSA ideas
Linear scan as a baseline; the seed of "can we do better than O(n)?" that gets answered properly in Binary Search problems (placed under Week 3, see below, since IITM's own binary search treatment is folded into list/array internals).
### Relevant NeetCode problems

#### LC 704 — Binary Search
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 2 → Lecture 2.4 → Searching → Binary Search (secondary fit: foundational, placed here for pedagogical sequencing even though IITM's explicit binary search depth comes later via sorted structures)
- **Pattern:** Binary Search on sorted array
- **Why here:** The lecture explicitly contrasts linear vs faster search; this is the direct "faster way" answer and should be solved the same week to lock in the O(log n) intuition while linear search is fresh.
- **Prerequisites:** Sorted array property; loop invariants.
- **Best approach:** Two pointers `lo`, `hi`; compute `mid`; narrow the search space by comparing `nums[mid]` to target.
- **Time Complexity:** O(log n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Infinite loops from incorrect pointer updates (`lo = mid` instead of `lo = mid + 1`).
  - Off-by-one in `hi = len(nums) - 1` vs `hi = len(nums)`.
- **Interview Value:** Medium (rarely asked standalone, but the base case for many harder binary-search problems below).
- **Related Problems:** LC 74, LC 875, LC 33, LC 153, LC 4 (all in Week 3/7).
- **Notes:** 📌 **Revision Tip:** Be able to write this with zero bugs in under 2 minutes — it is the building block for ~6 other problems in this handbook.

## Lecture 2.5 — Selection Sort
### What this lecture teaches
Selection Sort algorithm and its O(n²) complexity, in-place sorting concept.
### Core DSA ideas
In-place comparison sorting; foundational vocabulary (stable/unstable, in-place) used to discuss every later sort.
### Relevant NeetCode problems
None directly — NeetCode doesn't test "implement Selection Sort" itself, but understanding it is necessary to appreciate why Merge Sort (2.7) and Quicksort (3.1) are improvements.

## Lecture 2.6 — Insertion Sort
### What this lecture teaches
Insertion Sort algorithm, good performance on nearly-sorted data, O(n²) worst case.
### Core DSA ideas
Same as above — comparison sort vocabulary; insertion-based thinking reappears conceptually in some interval/greedy problems (Week 7).
### Relevant NeetCode problems
None directly.

## Lecture 2.7 — Merge Sort
### What this lecture teaches
Divide-and-conquer sorting: split, recursively sort, merge.
### Core DSA ideas
This is the conceptual root of: (a) the "merge" operation reused directly in linked-list merging, and (b) Divide & Conquer formally taught in Week 8.
### Relevant NeetCode problems

#### LC 21 — Merge Two Sorted Lists
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 2 → Lecture 2.7 → Merge Sort → Merge Step (secondary fit: also belongs to Week 4 Linked Lists, but the *merge* logic itself is taught here)
- **Pattern:** Two-pointer merge
- **Why here:** This problem **is** the merge step of merge sort, just applied to linked lists instead of arrays. Solving it right after 2.7 cements the merge mechanic before it's reused in LC 23 (Week 6) and the linked-list section (Week 4).
- **Prerequisites:** Linked list node basics (conceptually from 1.7's OOP, formalized in Week 4).
- **Best approach:** Dummy head node; advance whichever pointer has the smaller current value; splice in the remainder.
- **Time Complexity:** O(n + m)
- **Space Complexity:** O(1) iterative (excluding output list)
- ⚠️ **Common Mistakes:**
  - Forgetting to advance the "remainder" list once one input is exhausted.
  - Losing the head reference by not using a dummy node.
- **Interview Value:** High — a building block for LC 23 and LC 148-style merge problems.
- **Related Problems:** LC 23 (Merge k Sorted Lists), LC 148 (Sort List — not in NC150 but common extension).
- **Notes:** Revisit this exact merge logic when doing LC 23 in Week 6 — same idea, generalized with a heap.

### What should be solved immediately after Lecture 2.7
LC 21 (P1) — to literally apply the merge step you just learned.

## Lecture 2.8 — Analysis of Merge Sort
### What this lecture teaches
Formal recurrence-based derivation of Merge Sort's O(n log n) complexity.
### Core DSA ideas
Recurrence relations — directly used again in Week 8 (Divide & Conquer, Recursion Trees) and indirectly in every recursive DP solution's complexity analysis.
### Relevant NeetCode problems
None new — apply this analytical lens retroactively to LC 21 (the merge step is O(n+m), and you should be able to explain why the full recursive Merge Sort is O(n log n) even though the merge step alone is linear).

## Lecture 2.9 — Implementation of Searching and Sorting Algorithms
### What this lecture teaches
Hands-on coding of the searching/sorting algorithms covered in lectures 2.4–2.7.
### Core DSA ideas
Translating the theory into bug-free code — the same skill tested in every NeetCode problem.
### Relevant NeetCode problems
None new; use this lecture as a checkpoint to re-implement Selection Sort, Insertion Sort, and Merge Sort from scratch without notes before moving to Week 3.

### What should be solved immediately after Week 2
- LC 217, LC 1, LC 242 (P1) — core hashing
- LC 704 (P1) — core binary search foundation
- LC 21 (P1) — merge mechanic

### What should be solved during revision
- LC 49, LC 347 (P2) — solve same week, but these are the first candidates to re-attempt in a later revision pass.

### What should be left for later
- None major from this week's direct list — everything mapped here is either P1 or P2. (LC 215, LC 973 — alternate approaches to Top-K-style problems — are deferred to Weeks 6 and 8 respectively.)

---

# Week 3 — Quicksort & List/Array Internals

**Lectures covered:** 3.1 – 3.9
**Main topic:** Quicksort and its analysis; the conceptual and implementation-level distinction between Python lists and true arrays; building a flexible list ADT; dictionary implementation.
**DSA pattern introduced:** Partitioning (seed for Two Pointers and Quick Select); deep array/list mechanics that justify Two Pointers and Sliding Window complexity claims.

## Lecture 3.1 — Quicksort
### What this lecture teaches
Quicksort algorithm: pivot selection, partitioning, recursive sort of partitions.
### Core DSA ideas
**Partitioning** — the exact mechanism reused in Two Pointers problems and, later, Quick Select (Week 8).
### Relevant NeetCode problems

#### LC 75 is not in this list — skip. (No direct sorting-implementation NeetCode problem exists in NC150; Quicksort's NeetCode payoff arrives via Quick Select in Week 8.)

No problems mapped directly to 3.1 itself, but the **partitioning concept taught here is the prerequisite** for:
- LC 215 — Kth Largest Element in an Array (Week 8, Quick Select)
- Two-pointer array problems below (3.5–3.9)

## Lecture 3.2 — Analysis of Quicksort
### What this lecture teaches
Average-case O(n log n) vs worst-case O(n²) analysis of Quicksort, and why pivot choice matters.
### Core DSA ideas
Average-case vs worst-case reasoning — directly relevant when discussing Quick Select's O(n) average / O(n²) worst case in Week 8.
### Relevant NeetCode problems
None new.

## Lecture 3.3 — Implementation of Quicksort Algorithm
### What this lecture teaches
Hands-on coding of Quicksort (Lomuto or Hoare partition scheme).
### Core DSA ideas
Implementation fluency with partition logic — directly transferable to LC 215 in Week 8.
### Relevant NeetCode problems
None new — but this is the lecture to **memorize the partition function** cleanly, since you will reuse it nearly verbatim for Quick Select.

## Lecture 3.4 — Concluding Remarks on Sorting Algorithms
### What this lecture teaches
Comparative summary: stability, in-place-ness, best/worst/average case across Selection/Insertion/Merge/Quicksort.
### Core DSA ideas
The "which sort do I use when" decision table — useful general knowledge, rarely tested directly.
### Relevant NeetCode problems
None directly, but this comparative thinking resurfaces whenever a problem says "sort the array first" (e.g., LC 56 Merge Intervals in Week 7) and you should justify *why* O(n log n) sort is acceptable there.

## Lecture 3.5 — Difference Between Lists and Arrays (Theory)
### What this lecture teaches
Conceptual contrast: Python lists are dynamic arrays of pointers; true arrays are contiguous fixed-type memory blocks. Big-O implications of append, insert, delete, index.
### Core DSA ideas
This lecture is the **complexity justification** for treating Python list indexing/append as O(1) throughout every array problem in this handbook.
### Relevant NeetCode problems
None new directly, but this is the theoretical backbone for the entire Arrays & Hashing + Two Pointers + Sliding Window sections that follow.

## Lecture 3.6 — Designing a Flexible List and Operations on the Same
### What this lecture teaches
How dynamic arrays achieve amortized O(1) append via capacity doubling.
### Core DSA ideas
Amortized analysis — directly explains why repeatedly appending to a Python list in a sliding-window loop doesn't break the O(n) bound.
### Relevant NeetCode problems
None new — but this is exactly the justification needed when you write "O(n) amortized" for any of the sliding window problems below.

## Lecture 3.7 — Implementation of Lists in Python
### What this lecture teaches
Hands-on construction of a list-like structure from scratch.
### Core DSA ideas
Reinforces 3.5/3.6 with code.
### Relevant NeetCode problems
**This is the natural point in the syllabus to begin the Two Pointers and Sliding Window problem set**, since you now fully understand the cost model of the container you're operating on.

#### LC 125 — Valid Palindrome
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 3 → Lecture 3.7 → Two Pointers → Inward-converging pointers
- **Pattern:** Two Pointers (opposite ends)
- **Why here:** Simplest possible two-pointer problem; ideal first exposure right after confirming O(1) indexing cost from 3.5–3.7.
- **Prerequisites:** String indexing, `isalnum()`/character filtering.
- **Best approach:** `left`/`right` pointers from both ends, skip non-alphanumeric, compare lowercase chars, converge.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Creating a cleaned copy of the string first (works, but wastes the O(1)-space opportunity the pattern is meant to teach).
  - Mishandling case sensitivity.
- **Interview Value:** Medium.
- **Related Problems:** LC 167, LC 11, LC 15.
- **Notes:** 💡 **Pattern Recognition:** "palindrome check" + need O(1) space → two pointers from both ends.

#### LC 167 — Two Sum II (Input Array Is Sorted)
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 3 → Lecture 3.7 → Two Pointers → Sorted-array convergence
- **Pattern:** Two Pointers
- **Why here:** Direct contrast to LC 1: same problem, but sorted input makes the O(n) two-pointer approach beat the hashmap approach on space.
- **Prerequisites:** LC 1 (Week 2) solved first, so the contrast is meaningful.
- **Best approach:** `left=0`, `right=n-1`; move pointers inward based on whether current sum is too high or too low.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Defaulting to the hashmap solution out of habit, missing the intended O(1)-space pointer technique.
  - Off-by-one when returning 1-indexed answer (LeetCode requires 1-indexed here).
- **Interview Value:** High — interviewers love asking "now what if it's sorted?" as a follow-up to LC 1.
- **Related Problems:** LC 1, LC 15.
- **Notes:** 📌 **Revision Tip:** Be ready to explain *why* two pointers work only because the array is sorted — monotonicity is the enabling property.

#### LC 15 — 3Sum
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 3 → Lecture 3.7 → Two Pointers → Fixed pointer + inner two-pointer scan
- **Pattern:** Sort + Two Pointers, with duplicate-skipping
- **Why here:** Natural extension of LC 167 — fix one element, then run the same two-pointer scan on the rest.
- **Prerequisites:** LC 167 must be solid first; sorting (Week 2 lectures, justified again here).
- **Best approach:** Sort array; for each index `i`, run a two-pointer search on `[i+1, n-1]` for pairs summing to `-nums[i]`; skip duplicates at every level.
- **Time Complexity:** O(n²)
- **Space Complexity:** O(1) extra (excluding sort)
- ⚠️ **Common Mistakes:**
  - Forgetting to skip duplicate values for `i`, `left`, and `right`, producing duplicate triplets.
  - Not sorting first, making two pointers invalid.
- **Interview Value:** High — extremely common; tests whether you can compose two-pointer logic inside an outer loop.
- **Related Problems:** LC 167, LC 11, LC 18 (4Sum — not in NC150 but a common follow-up).
- **Notes:** ⚠️ **Common Trap:** Triplet de-duplication logic is the #1 source of bugs here — practice it deliberately.

#### LC 11 — Container With Most Water
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 3 → Lecture 3.7 → Two Pointers → Greedy pointer movement
- **Pattern:** Two Pointers with greedy elimination
- **Why here:** A different two-pointer flavor — instead of searching for a target sum, you greedily discard the shorter wall, reinforcing that "two pointers" is a family of techniques, not one trick.
- **Prerequisites:** LC 167, LC 15.
- **Best approach:** Start with widest container; move the pointer at the shorter wall inward, since the taller wall can never be the bottleneck again at a narrower width.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Moving both pointers simultaneously (incorrect — only the shorter wall's pointer should move).
  - Failing to prove to yourself *why* discarding the shorter wall is safe (interviewers ask this).
- **Interview Value:** High.
- **Related Problems:** LC 42 (Trapping Rain Water, harder variant).
- **Notes:** 💡 **Pattern Recognition:** "maximize area/volume between two boundaries" → greedy two pointers.

#### LC 42 — Trapping Rain Water
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 3 → Lecture 3.7 → Two Pointers → Running-max tracking
- **Pattern:** Two Pointers with prefix/suffix max tracking
- **Why here:** Direct escalation from LC 11 — same "shorter side moves" insight, but now accumulating trapped water rather than computing area once.
- **Prerequisites:** LC 11 solved and deeply understood.
- **Best approach:** Two pointers from both ends tracking `left_max` and `right_max`; add water at the side with the smaller max.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Trying to precompute left-max/right-max arrays (valid O(n) space solution, but misses the O(1) two-pointer insight).
  - Off-by-one when adding trapped water at boundary indices.
- **Interview Value:** High — one of the most-cited "hard but elegant" interview problems.
- **Related Problems:** LC 11.
- **Notes:** 📌 **Revision Tip:** Practice explaining out loud why `min(left_max, right_max)` is always safe to use, even without knowing the global max in advance.

### What should be solved immediately after Lecture 3.7
LC 125, LC 167, LC 15 (P1).

### What should be solved during revision
LC 11, LC 42 (P2) — same week is fine, but they're natural revision candidates too since LC 42 in particular is easy to forget the exact invariant for.

## Lecture 3.8 — Implementation of Dictionaries in Python
### What this lecture teaches
How Python dictionaries are implemented (hash tables): hashing, collision handling, average O(1) operations.
### Core DSA ideas
This is the **formal justification** for every "O(1) average lookup" claim made about hashmaps/sets in this handbook, going all the way back to Week 2.
### Relevant NeetCode problems

#### LC 238 — Product of Array Except Self
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 3 → Lecture 3.8/3.9 → Arrays → Prefix/Suffix Product
- **Pattern:** Prefix and Suffix products (array technique, not hashing — but placed here because it's the natural "what else can arrays do efficiently" follow-up)
- **Why here:** Tests whether you can avoid both division and a brute-force O(n²) approach using array preprocessing — natural next step after deepening array/list cost-model understanding.
- **Prerequisites:** Solid array indexing and iteration; understanding why division-based solutions are disallowed by the problem (division by zero edge case).
- **Best approach:** Build prefix-product array, then suffix-product array (or fold suffix into a single backward pass over the prefix array), multiply.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1) extra if folding suffix pass into the output array; O(n) otherwise.
- ⚠️ **Common Mistakes:**
  - Using division and not handling zeros in the input.
  - Allocating two full extra arrays when one pass can be folded into the output array directly.
- **Interview Value:** High.
- **Related Problems:** LC 53 (Maximum Subarray — different technique, same array-scanning spirit).
- **Notes:** Classic "no division allowed" constraint problem — always ask the interviewer to confirm constraints up front.

#### LC 36 — Valid Sudoku
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 3 → Lecture 3.8 → Hashing → Multi-key Set Tracking
- **Pattern:** Hash Set, multiple simultaneous trackers (rows, columns, boxes)
- **Why here:** Direct application of dictionary/set mechanics from 3.8 to a 2D validation problem — tests whether you can track multiple independent constraints with sets.
- **Prerequisites:** LC 217/242 set logic; 2D array indexing.
- **Best approach:** Maintain a set per row, per column, and per 3×3 box (often keyed as `(box_row, box_col)`); for each filled cell, check and record.
- **Time Complexity:** O(1) — board is fixed 9×9, so technically constant, but reasoned about as O(n²) for an n×n board.
- **Space Complexity:** O(1) (fixed-size board) / O(n²) generalized.
- ⚠️ **Common Mistakes:**
  - Incorrect box-index formula (`(row // 3, col // 3)`).
  - Forgetting to skip empty cells (`'.'`).
- **Interview Value:** Medium.
- **Related Problems:** LC 217, LC 242.
- **Notes:** Good test of whether hashing generalizes beyond 1D problems.

#### LC 271 — Encode and Decode Strings
- **Difficulty:** Medium
- **Priority:** P3
- **Mapped to:** Week 3 → Lecture 3.8/3.5 → Strings → Custom Serialization
- **Pattern:** String encoding with length-prefixing
- **Why here:** Tests string manipulation depth (related to 3.5's array/string distinction) rather than hashing per se; placed here as the last "strings as data" problem before pure graph/tree content begins in Week 4.
- **Prerequisites:** String slicing, careful index arithmetic.
- **Best approach:** Encode each string as `f"{len(s)}#{s}"`; decode by reading the length prefix up to `#`, then slicing exactly that many characters.
- **Time Complexity:** O(n) total over all strings.
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:**
  - Using a naive delimiter (like a comma) that can appear inside the strings themselves — length-prefixing avoids this entirely.
- **Interview Value:** Medium — mainly tests careful string-parsing discipline.
- **Related Problems:** LC 297 (Serialize/Deserialize Binary Tree, Week 5 — same length-prefix-style trick applies to other delimiters there too).
- **Notes:** LeetCode-premium-locked in some regions, but appears in NeetCode 150; still a great parsing exercise.

#### LC 128 — Longest Consecutive Sequence
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 3 → Lecture 3.8 → Hashing → Set-based Sequence Detection
- **Pattern:** Hash Set + sequence boundary detection
- **Why here:** A more advanced hashing problem than LC 217/242 — requires recognizing that only "sequence starts" need to trigger an expansion scan, which keeps the algorithm O(n) despite looking like it might be O(n²).
- **Prerequisites:** Comfortable hash set usage; the insight that checking `num - 1 not in set` identifies sequence starts.
- **Best approach:** Put all numbers in a set; for each number that is a sequence start (no `num-1` in set), count forward (`num+1`, `num+2`, …) while updating max length.
- **Time Complexity:** O(n) — looks like O(n²) but each number is only ever visited as part of one sequence expansion.
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:**
  - Sorting first (works but O(n log n), not optimal — fine as a fallback, but know the O(n) version).
  - Forgetting the `num - 1 not in set` start-check, causing repeated re-counting of the same sequence and accidental O(n²) blowup.
- **Interview Value:** High.
- **Related Problems:** LC 1, LC 217.
- **Notes:** 💡 **Pattern Recognition:** "longest run of consecutive integers" in an unsorted array → hash set + start-detection, not sorting, for the optimal answer.

### What should be solved immediately after Lecture 3.8
LC 238 (P1).

### What should be solved during revision
LC 36, LC 128 (P2/P2) — solve in-week, revisit during revision pass since both have a non-obvious "trick" (box-indexing; start-detection) that's easy to forget.

### What should be left for later
LC 271 (P3) — lower interview frequency; fine to push to a later revision-only pass.

## Lecture 3.9 — Difference Between Lists and Arrays (Implementation)
### What this lecture teaches
Code-level confirmation of the theory from 3.5, often comparing a hand-rolled array-backed list against Python's built-in list.
### Core DSA ideas
Closes the loop on container cost-model understanding before graphs begin in Week 4.
### Relevant NeetCode problems
None new — use this lecture as a final check that you can justify every Space/Time Complexity field written so far in this handbook with reference to *how Python's list/dict are actually implemented*, not just memorized Big-O labels.

---

# Week 4 — Graphs: Representation, BFS, DFS, DAGs

**Lectures covered:** 4.1 – 4.8
**Main topic:** Graph fundamentals — representation, the two universal traversal algorithms (BFS, DFS), their applications, and directed acyclic graphs with topological sorting.
**DSA pattern introduced:** Graph Traversal (BFS/DFS), Topological Sort, DAG longest path (a DP-on-graph pattern, foreshadowing Week 9).

> 📌 **Sequencing Note:** IITM PDSA does not have a dedicated "Linked Lists" or "Trees" week — these structures are implicitly assumed as simple applications of node-based objects (taught conceptually in Lecture 1.7) and are most naturally introduced as the *simplest possible graphs* right alongside Week 4's graph theory. This handbook places **Linked List and Tree problems in Week 4 and Week 5** respectively, explicitly flagged as **secondary fit**, because:
> - A singly linked list is a directed graph where every node has out-degree ≤ 1.
> - A binary tree is a directed acyclic graph where every node has out-degree ≤ 2 and exactly one path from the root to any node.
>
> This is not a forced mapping — it is the standard CS-theory framing, and IITM's own DAG/topological-sort lectures (4.6–4.8) make this connection explicit when discussing trees as a DAG special case.

## Lecture 4.1 — Introduction to Graphs
### What this lecture teaches
Formal definition of graphs: vertices, edges, directed vs undirected, weighted vs unweighted, degree.
### Core DSA ideas
Graph vocabulary used in every problem from here through Week 5.
### Relevant NeetCode problems
None directly — pure definitions.

## Lecture 4.2 — Representing Graphs
### What this lecture teaches
Adjacency list vs adjacency matrix representations, and their space/time tradeoffs.
### Core DSA ideas
Choosing the right representation directly affects the complexity of every traversal problem below.
### Relevant NeetCode problems

#### LC 133 — Clone Graph
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.2 → Graphs → Adjacency representation + DFS
- **Pattern:** DFS with a hashmap to track visited/cloned nodes
- **Why here:** Directly tests whether you can build a new adjacency-list-style structure while traversing an existing one — the practical embodiment of 4.2's representation theory.
- **Prerequisites:** 4.1's vocabulary; basic DFS recursion comfort (formalized fully in 4.4, but a simple version suffices here).
- **Best approach:** DFS (or BFS) from the given node; maintain a `old_node -> new_node` map to avoid infinite loops on cycles and to reuse already-cloned nodes.
- **Time Complexity:** O(V + E)
- **Space Complexity:** O(V)
- ⚠️ **Common Mistakes:**
  - Not checking the visited map before recursing, causing infinite recursion on cyclic graphs.
  - Cloning a node's value but forgetting to also clone/connect its neighbor list correctly.
- **Interview Value:** High.
- **Related Problems:** LC 200, LC 207.
- **Notes:** Good early signal of whether you instinctively reach for a hashmap to handle cycles.

### What should be solved immediately after Lecture 4.2
LC 133 (P1) is best attempted *after* 4.3/4.4 if you're not yet comfortable with raw recursive traversal — listed here for representation purposes, but you may solve it right after DFS (4.4) instead. Treat as P1 for "by end of Week 4," not strictly "right after 4.2."

## Lecture 4.3 — Breadth First Search (BFS)
### What this lecture teaches
BFS algorithm using a queue; level-by-level exploration; shortest path in unweighted graphs.
### Core DSA ideas
Queue-based traversal — the single most reused pattern in the Graphs category of this handbook.
### Relevant NeetCode problems

#### LC 200 — Number of Islands
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.3 → Graphs → BFS/DFS on implicit grid graph
- **Pattern:** Grid traversal (BFS or DFS), connected components
- **Why here:** The textbook first application of BFS to a grid treated as an implicit graph (each cell connects to up to 4 neighbors) — should be solved immediately after BFS is taught.
- **Prerequisites:** Queue usage (`collections.deque`); 2D grid indexing.
- **Best approach:** For each unvisited land cell, BFS/DFS outward marking all connected land as visited, incrementing the island count once per BFS/DFS launch.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols) worst case (visited set / recursion stack)
- ⚠️ **Common Mistakes:**
  - Forgetting to mark cells visited before/while enqueuing them, causing the same cell to be processed multiple times.
  - Off-grid index errors when checking neighbors.
- **Interview Value:** High — one of the most frequently asked graph problems in interviews.
- **Related Problems:** LC 695, LC 130, LC 994, LC 417.
- **Notes:** 💡 **Pattern Recognition:** "count connected regions in a grid" → BFS/DFS flood fill.

#### LC 695 — Max Area of Island
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.3 → Graphs → BFS/DFS Flood Fill, size tracking
- **Pattern:** Grid traversal with size accumulation
- **Why here:** Near-identical to LC 200 but requires tracking component *size* rather than just counting components — ideal immediate reinforcement.
- **Prerequisites:** LC 200 solved first.
- **Best approach:** Same flood-fill BFS/DFS as LC 200, but accumulate a counter per island and track the running maximum.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols)
- ⚠️ **Common Mistakes:** Same as LC 200 — visited tracking and grid bounds.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 200.
- **Notes:** Solve immediately after LC 200 — same-day repetition locks in the pattern.

#### LC 994 — Rotting Oranges
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.3 → Graphs → Multi-source BFS
- **Pattern:** Multi-source BFS, level = time step
- **Why here:** First "multi-source" BFS problem — all initially-rotten oranges start in the queue simultaneously, and BFS level corresponds directly to elapsed minutes. This is the natural next BFS variant after single-source flood fill.
- **Prerequisites:** LC 200/695.
- **Best approach:** Initialize queue with all rotten oranges; BFS level by level, incrementing a minute counter per layer; track remaining fresh oranges.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols)
- ⚠️ **Common Mistakes:**
  - Processing the queue one node at a time instead of one full level at a time, breaking the minute-counting logic.
  - Forgetting to check if any fresh oranges remain unreachable at the end.
- **Interview Value:** High.
- **Related Problems:** LC 286, LC 200.
- **Notes:** 💡 **Pattern Recognition:** "spreads/infects over time from multiple starting points" → multi-source BFS.

#### LC 286 — Walls and Gates
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 4 → Lecture 4.3 → Graphs → Multi-source BFS
- **Pattern:** Multi-source BFS, distance propagation
- **Why here:** Direct sibling of LC 994 — multiple sources (gates) propagate outward simultaneously, but this time recording distance instead of a time counter.
- **Prerequisites:** LC 994 solved first.
- **Best approach:** Initialize queue with all gate cells (distance 0); BFS outward, updating each empty room's distance the first time it's reached.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols)
- ⚠️ **Common Mistakes:** Using DFS from each gate separately (works but far less efficient than one combined multi-source BFS).
- **Interview Value:** Medium (LeetCode premium problem, but conceptually important and present in NC150).
- **Related Problems:** LC 994, LC 200.
- **Notes:** Solve right after LC 994 to compare "counting" vs "distance" multi-source BFS variants.

#### LC 127 — Word Ladder
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 4 → Lecture 4.3 → Graphs → BFS on an implicit word graph
- **Pattern:** BFS, shortest path, implicit graph construction
- **Why here:** Tests whether you can recognize a non-grid, non-explicit graph (words connected if they differ by one letter) and still apply BFS correctly for shortest path.
- **Prerequisites:** Comfortable BFS from grid problems above; string manipulation.
- **Best approach:** BFS from `beginWord`; at each step, try all single-character substitutions of the current word and check membership in the word set; track levels as path length.
- **Time Complexity:** O(n × 26 × L) where n = number of words, L = word length.
- **Space Complexity:** O(n × L)
- ⚠️ **Common Mistakes:**
  - Regenerating all words via comparison instead of generating substitutions directly (far slower).
  - Forgetting to remove visited words from the set, causing re-processing.
- **Interview Value:** High (frequently cited as a hard-but-important BFS problem).
- **Related Problems:** LC 269 (Alien Dictionary, Week 4 — different graph type), LC 200.
- **Notes:** 📌 **Revision Tip:** Practice the "generate all one-letter-substitution neighbors" trick — it generalizes to several implicit-graph problems.

### What should be solved immediately after Lecture 4.3
LC 200, LC 695, LC 994 (P1).

### What should be solved during revision
LC 286, LC 127 (P2).

## Lecture 4.4 — Depth First Search (DFS)
### What this lecture teaches
DFS algorithm using recursion or an explicit stack; pre/post-order notions; comparison with BFS.
### Core DSA ideas
Recursive traversal — the second pillar pattern alongside BFS, and the one most tree problems (Week 5) will rely on directly.
### Relevant NeetCode problems

#### LC 130 — Surrounded Regions
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.4 → Graphs → DFS, boundary-first traversal
- **Pattern:** DFS from borders ("reverse thinking" — mark what's safe rather than what's captured)
- **Why here:** A DFS problem where the *insight* (start DFS from the border, not from each region) matters more than mechanical traversal — ideal right after DFS is formalized.
- **Prerequisites:** LC 200-style flood fill comfort.
- **Best approach:** DFS/BFS from every border 'O', marking reachable cells as safe; then flip all remaining unmarked 'O's to 'X', since they must be fully surrounded.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols)
- ⚠️ **Common Mistakes:**
  - Starting the flood fill from inner 'O's directly and trying to detect "is this surrounded" locally (much harder and error-prone) instead of using the border-first reverse trick.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 200, LC 417.
- **Notes:** 💡 **Pattern Recognition:** "things touching the boundary are exempt" → flood-fill from the boundary inward, not the reverse.

#### LC 417 — Pacific Atlantic Water Flow
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 4 → Lecture 4.4 → Graphs → DFS, multi-source reverse traversal
- **Pattern:** DFS from both sets of borders independently, then intersect
- **Why here:** Combines the "reverse DFS from border" insight (LC 130) with multi-source thinking (LC 994/286) — a natural synthesis problem to close out the DFS block.
- **Prerequisites:** LC 130, LC 994.
- **Best approach:** Run DFS from all Pacific-border cells (tracking reachability backward, i.e., uphill), then from all Atlantic-border cells; intersect the two reachable sets.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols)
- ⚠️ **Common Mistakes:**
  - Trying to DFS forward from every single cell to both oceans (O((rows×cols)²) — far too slow).
  - Getting the "uphill" traversal direction backwards.
- **Interview Value:** Medium.
- **Related Problems:** LC 130, LC 200.
- **Notes:** 📌 **Revision Tip:** This "traverse backward from multiple targets" trick reappears in harder graph problems — worth deliberate re-derivation before interviews.

#### LC 207 — Course Schedule
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.4/4.6 → Graphs → Cycle Detection via DFS
- **Pattern:** DFS with three-color (unvisited/visiting/visited) cycle detection
- **Why here:** Bridges DFS (4.4) directly into the DAG concept (4.6) — a course schedule is only completable if its prerequisite graph is acyclic.
- **Prerequisites:** DFS recursion; recursion stack reasoning.
- **Best approach:** Build adjacency list; DFS each node tracking an "in current recursion path" set — if you revisit a node still in that path, there's a cycle.
- **Time Complexity:** O(V + E)
- **Space Complexity:** O(V + E)
- ⚠️ **Common Mistakes:**
  - Using only a single "visited" set without distinguishing "currently in this DFS path" vs "fully processed," which fails to detect cycles correctly.
- **Interview Value:** Very High — one of the most-asked graph problems overall.
- **Related Problems:** LC 210, LC 261, LC 269.
- **Notes:** 💡 **Pattern Recognition:** "can all tasks/courses be completed given dependencies" → cycle detection in a directed graph.

### What should be solved immediately after Lecture 4.4
LC 130, LC 207 (P1).

### What should be solved during revision
LC 417 (P2).

## Lecture 4.5 — Applications of BFS and DFS
### What this lecture teaches
Worked examples applying BFS/DFS to connectivity, bipartiteness, cycle detection — practical use cases beyond raw traversal.
### Core DSA ideas
Connected components — directly the Union-Find-adjacent problems below (solvable via DFS even before Union-Find is formally taught in Week 6).
### Relevant NeetCode problems

#### LC 323 — Number of Connected Components in an Undirected Graph
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.5 → Graphs → Connected Components via DFS (secondary fit: also solvable via Union-Find, Week 6)
- **Pattern:** DFS/BFS connected-component counting
- **Why here:** Directly the "application" lecture promises — counting components is the single most natural DFS application after cycle detection.
- **Prerequisites:** LC 200/207-level DFS comfort.
- **Best approach:** Build adjacency list; DFS/BFS from each unvisited node, incrementing a component counter once per launch.
- **Time Complexity:** O(V + E)
- **Space Complexity:** O(V + E)
- ⚠️ **Common Mistakes:** Forgetting the graph might be disconnected and only running one traversal instead of looping over all unvisited nodes.
- **Interview Value:** High.
- **Related Problems:** LC 684, LC 261 (revisit with Union-Find in Week 6 for an alternate solution).
- **Notes:** 📌 **Revision Tip:** Solve this once with DFS now, then once more with Union-Find in Week 6 — comparing both is high-value.

#### LC 261 — Graph Valid Tree
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 4 → Lecture 4.5 → Graphs → Tree Validity Check (secondary fit: Union-Find alternative in Week 6)
- **Pattern:** DFS cycle detection + connectivity check
- **Why here:** A graph is a valid tree iff it is connected AND has exactly n-1 edges with no cycle — synthesizes both cycle detection (4.4) and connectivity (4.5).
- **Prerequisites:** LC 207, LC 323.
- **Best approach:** Check edge count equals n-1 first (necessary condition); then run a single DFS/BFS from any node and confirm all n nodes are visited.
- **Time Complexity:** O(V + E)
- **Space Complexity:** O(V + E)
- ⚠️ **Common Mistakes:** Forgetting the n-1 edge count shortcut and writing more complex cycle-detection logic than necessary.
- **Interview Value:** Medium.
- **Related Problems:** LC 323, LC 684.
- **Notes:** Elegant problem once you know the n-1 edge fact; clunky without it.

### What should be solved immediately after Lecture 4.5
LC 323 (P1).

### What should be solved during revision
LC 261 (P2).

## Lecture 4.6 — Introduction to Directed Acyclic Graph (DAG)
### What this lecture teaches
DAG definition and significance — graphs with no directed cycles, used to model dependencies/precedence.
### Core DSA ideas
DAG concept directly justifies why LC 207 (Course Schedule) is framed as cycle detection.
### Relevant NeetCode problems
None new — conceptual lecture; LC 207 (above) is its main practical anchor, already placed under 4.4 for sequencing reasons.

## Lecture 4.7 — Topological Sorting
### What this lecture teaches
Topological ordering of a DAG — via DFS post-order reversal or Kahn's BFS (in-degree) algorithm.
### Core DSA ideas
Topological Sort — a named, reusable pattern distinct from plain DFS/BFS.
### Relevant NeetCode problems

#### LC 210 — Course Schedule II
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 4 → Lecture 4.7 → Graphs → Topological Sort
- **Pattern:** Kahn's Algorithm (BFS) or DFS post-order topological sort
- **Why here:** Direct upgrade of LC 207 — instead of just detecting a cycle, you must *produce* a valid ordering, which is exactly what 4.7 teaches.
- **Prerequisites:** LC 207 solved first.
- **Best approach:** Kahn's algorithm — compute in-degrees, repeatedly pop zero-in-degree nodes into a queue, append to result, decrement neighbors' in-degree.
- **Time Complexity:** O(V + E)
- **Space Complexity:** O(V + E)
- ⚠️ **Common Mistakes:**
  - Returning a partial order without checking that all V nodes were placed (which would indicate a cycle and should return an empty list).
- **Interview Value:** High.
- **Related Problems:** LC 207, LC 269, LC 332.
- **Notes:** 📌 **Revision Tip:** Know both the BFS (Kahn's) and DFS-postorder approaches — interviewers sometimes ask for both.

#### LC 269 — Alien Dictionary
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 4 → Lecture 4.7 → Graphs → Topological Sort, implicit graph construction
- **Pattern:** Topological Sort with graph built from pairwise word comparisons
- **Why here:** The hardest topological-sort variant in NC150 — building the graph itself (from adjacent-word comparisons) is non-trivial, on top of the standard topological sort.
- **Prerequisites:** LC 210 solid; careful edge-case handling.
- **Best approach:** For each adjacent pair of words, find the first differing character and add a directed edge (`word1[i] -> word2[i]`); run topological sort on the resulting character graph; handle invalid cases (e.g., a word is a prefix of an earlier word incorrectly).
- **Time Complexity:** O(C) where C is total character count across all words (graph construction) plus O(V+E) for the sort.
- **Space Complexity:** O(1) extra for 26-letter alphabet graph, or O(k²) generally.
- ⚠️ **Common Mistakes:**
  - Only comparing the first differing character between adjacent words pairwise, but forgetting non-adjacent pairs don't need direct comparison (sorted order is transitive — a common source of confusion).
  - Missing the invalid case where a longer word appears before its own prefix.
- **Interview Value:** High (Google/Meta-style favorite).
- **Related Problems:** LC 210, LC 332.
- **Notes:** ⚠️ **Common Trap:** Many learners try to compare every pair of words instead of only adjacent ones in sorted input order — review this carefully.

#### LC 332 — Reconstruct Itinerary
- **Difficulty:** Hard
- **Priority:** P3
- **Mapped to:** Week 4 → Lecture 4.7 → Graphs → Eulerian Path via DFS with lexical ordering (secondary fit: closer to Eulerian path theory than pure topological sort)
- **Pattern:** Hierholzer's-style DFS for Eulerian path, backtracking on dead ends
- **Why here:** Not a classic topological sort, but shares the "produce a valid full ordering using all edges" spirit — placed here as the most advanced graph-ordering problem in NC150, intentionally deferred to a later pass.
- **Prerequisites:** LC 210, comfort with multigraphs (multiple edges between same pair of nodes).
- **Best approach:** Sort/heapify each node's destination list; DFS greedily picking the lexicographically smallest unused edge; backtrack (insert at front) when a dead end is hit before using all tickets.
- **Time Complexity:** O(E log E) for sorting/heap edges.
- **Space Complexity:** O(E)
- ⚠️ **Common Mistakes:** Not handling multi-edges (duplicate routes) correctly with a simple visited set instead of an edge-usage count/multiset.
- **Interview Value:** Medium (niche pattern, less frequently asked than LC 210/269).
- **Related Problems:** LC 210, LC 269.
- **Notes:** P3 — defer to a dedicated revision pass; this is one of the trickier "Extra"-adjacent graph problems despite being a direct topic fit.

### What should be solved immediately after Lecture 4.7
LC 210 (P1).

### What should be solved during revision
LC 269 (P2).

### What should be left for later
LC 332 (P3) — revisit only once Course Schedule I/II and Alien Dictionary are fully solid.

## Lecture 4.8 — Longest Path in DAGs
### What this lecture teaches
Computing the longest path in a DAG using topological order + DP-style relaxation — the first explicit fusion of graph traversal and dynamic programming.
### Core DSA ideas
This lecture is the conceptual bridge to Week 9's Dynamic Programming — "DP on a DAG" is literally what longest-increasing-subsequence-style problems are doing under the hood.
### Relevant NeetCode problems

#### LC 329 — Longest Increasing Path in a Matrix
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 4 → Lecture 4.8 → Graphs → DAG Longest Path via DFS + Memoization (secondary fit: also classifiable as DP, Week 9)
- **Pattern:** DFS + memoization on an implicit DAG (grid where edges only go to strictly increasing neighbors)
- **Why here:** This is a textbook "longest path in a DAG" problem — the grid is implicitly a DAG because edges only point from smaller to larger values, exactly matching what 4.8 teaches, just dressed up as a grid problem.
- **Prerequisites:** LC 200-level grid DFS; basic memoization concept (formally covered in Week 9, but usable here as "cache repeated DFS results").
- **Best approach:** DFS from each cell with memoization — `dfs(cell)` = `1 + max(dfs(neighbor) for valid increasing neighbors)`, cached to avoid recomputation.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols)
- ⚠️ **Common Mistakes:**
  - Not memoizing, leading to exponential blowup (recomputing the same cell's longest path repeatedly).
  - Forgetting that this is inherently acyclic because edges only follow strictly increasing values, so cycle-safety doesn't need extra checks.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 300 (Longest Increasing Subsequence, Week 9 — same "longest chain" spirit in 1D).
- **Notes:** 📌 **Revision Tip:** Revisit this problem again after Week 9's memoization lecture — seeing it once as "DAG longest path" and once as "DP with memoization" cements that they are the same idea.

### What should be solved immediately after Lecture 4.8
None as strict P1 — LC 329 is P2 since it benefits from also having seen memoization formally (Week 9). Solving it now is good exposure; mastering it can wait.

### What should be solved during revision
LC 329 — revisit explicitly after Week 9.

---

# Week 5 — Shortest Paths & Minimum Spanning Trees (+ Linked Lists & Trees as Simple Graphs)

**Lectures covered:** 5.1 – 5.7
**Main topic:** Weighted graph shortest paths (Dijkstra, Bellman-Ford, Floyd-Warshall) and Minimum Spanning Trees (Prim's, Kruskal's).
**DSA pattern introduced:** Weighted Graph Traversal (priority-queue-driven Dijkstra), Dynamic-Programming-style relaxation (Bellman-Ford, Floyd-Warshall), Greedy MST construction.

> 📌 As flagged in Week 4, **Linked List and Tree problems are placed here/Week 4 as "simplest graph" special cases**, since IITM PDSA has no standalone week for them. This week handles **Linked Lists** (out-degree-1 directed graphs) since their traversal logic is a direct simplification of the graph traversal just learned; **Trees** (Week 6, alongside Heaps/Search Trees) get the fuller treatment once Search Trees are formally introduced.

## Lecture 5.1 — Shortest Paths in Weighted Graphs
### What this lecture teaches
Why unweighted BFS shortest-path logic breaks once edges have weights; motivates the need for specialized algorithms.
### Core DSA ideas
Sets up the contrast exploited by every weighted-shortest-path problem below.
### Relevant NeetCode problems
None directly — conceptual setup lecture.

**Linked List warm-up (placed here as the simplest directed-graph traversal):**

#### LC 206 — Reverse Linked List
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 5 → Lecture 5.1 (secondary fit: Linked Lists as degree-1 directed graphs) → Linked List → Pointer Reversal
- **Pattern:** Iterative pointer reversal (or recursive)
- **Why here:** The single most fundamental linked-list problem; placed at the start of this week's "simple graph" thread since reversing edge direction is conceptually a graph operation.
- **Prerequisites:** Node class familiarity (Lecture 1.7); pointer/reference semantics.
- **Best approach:** Iterative: maintain `prev = None`, walk forward reassigning `curr.next = prev` each step.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1) iterative; O(n) recursive (call stack).
- ⚠️ **Common Mistakes:**
  - Losing the reference to the next node before reassigning `curr.next`.
  - Forgetting to return the new head (the old tail).
- **Interview Value:** Very High — possibly the single most common linked-list interview question.
- **Related Problems:** LC 143, LC 21, LC 25.
- **Notes:** 📌 **Revision Tip:** Be able to write both iterative and recursive versions cold.

#### LC 143 — Reorder List
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 5 → Linked List → Two Pointers (fast/slow) + Reversal + Merge
- **Pattern:** Fast/slow pointer split + reverse second half + interleave merge
- **Why here:** Composes three previously-learned skills (two pointers from Week 3, reversal from LC 206, merge from LC 21/Week 2) into one problem — ideal synthesis exercise.
- **Prerequisites:** LC 206, LC 21, fast/slow pointer concept.
- **Best approach:** Find middle with fast/slow pointers; reverse the second half; merge the two halves by alternating nodes.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Off-by-one when splitting the list into exact halves (especially odd-length lists).
  - Forgetting to terminate the merged list properly (dangling `next` pointers causing cycles).
- **Interview Value:** High.
- **Related Problems:** LC 206, LC 21, LC 234 (Palindrome Linked List — not in NC150 but a close cousin).
- **Notes:** Excellent "composition" problem to test if earlier patterns actually stuck.

#### LC 19 — Remove Nth Node From End of List
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 5 → Linked List → Two Pointers (offset by n)
- **Pattern:** Two pointers with a fixed gap
- **Why here:** Simple, very common one-pass linked-list two-pointer trick — natural early problem in this block.
- **Prerequisites:** Dummy node usage; pointer traversal.
- **Best approach:** Advance a `fast` pointer n steps ahead, then move both `slow` and `fast` together until `fast` hits the end; `slow.next` is the node to remove.
- **Time Complexity:** O(n) — one pass.
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:**
  - Off-by-one in how many steps to advance `fast` first.
  - Not using a dummy head, causing trouble when removing the actual head node.
- **Interview Value:** High.
- **Related Problems:** LC 206, LC 143.
- **Notes:** Always use a dummy node for problems that might remove the head.

#### LC 138 — Copy List with Random Pointer
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 5 → Linked List → Hashmap-assisted cloning (secondary fit: directly parallels LC 133 Clone Graph from Week 4)
- **Pattern:** Hashmap `old -> new` node mapping, two-pass or interleaved
- **Why here:** Essentially LC 133 (Clone Graph) restricted to a linked list with an extra random pointer — ideal callback to Week 4's cloning pattern.
- **Prerequisites:** LC 133 conceptually; dict usage.
- **Best approach:** First pass creates all new nodes and maps old→new; second pass wires up `next` and `random` pointers using the map.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Trying to wire pointers in a single pass before all nodes exist, leading to `None` references for `random` pointers pointing forward.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 133, LC 206.
- **Notes:** 💡 **Pattern Recognition:** "clone a structure with extra cross-links" → hashmap-assisted two-pass cloning, every time.

#### LC 2 — Add Two Numbers
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 5 → Linked List → Simulated Arithmetic with Carry
- **Pattern:** Simultaneous traversal with carry propagation
- **Why here:** Tests careful linked-list traversal mechanics (different from pointer-rearrangement problems above) combined with elementary-school addition logic.
- **Prerequisites:** Dummy node pattern; careful loop termination conditions.
- **Best approach:** Traverse both lists simultaneously, summing digits plus carry, creating new nodes for the result; continue while either list or the carry remains.
- **Time Complexity:** O(max(n, m))
- **Space Complexity:** O(max(n, m)) for the output list.
- ⚠️ **Common Mistakes:**
  - Forgetting to handle a leftover carry after both lists are exhausted.
  - Off-by-one in loop condition when lists have different lengths.
- **Interview Value:** High.
- **Related Problems:** LC 43 (Multiply Strings — same carry-propagation spirit, Week 10).
- **Notes:** Clean, mechanical problem — practice writing it bug-free in one pass.

#### LC 141 — Linked List Cycle
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 5 → Linked List → Floyd's Cycle Detection (Fast/Slow Pointers)
- **Pattern:** Fast/slow pointer cycle detection
- **Why here:** Introduces Floyd's algorithm, which directly enables the harder LC 287 immediately after.
- **Prerequisites:** Pointer traversal comfort.
- **Best approach:** Two pointers moving at speeds 1 and 2; if they ever meet, a cycle exists; if `fast` reaches `None`, there is no cycle.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Checking `fast.next.next` without first checking `fast.next is not None`, causing a crash.
- **Interview Value:** High.
- **Related Problems:** LC 287.
- **Notes:** 💡 **Pattern Recognition:** "detect a cycle / find a repeated value via implicit linking" → Floyd's Tortoise and Hare.

#### LC 287 — Find the Duplicate Number
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 5 → Linked List → Floyd's Cycle Detection on an implicit "linked list" (array values as pointers)
- **Pattern:** Floyd's Cycle Detection, reframed on an array
- **Why here:** A clever non-linked-list problem that is solved by *treating the array as a linked list* (`index -> nums[index]`), reinforcing that Floyd's algorithm generalizes beyond literal node objects.
- **Prerequisites:** LC 141 solved and deeply understood first.
- **Best approach:** Treat `nums[i]` as a pointer to the next index; run Floyd's algorithm to find the cycle entry point, which is the duplicate value.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Not recognizing the array-as-implicit-linked-list reframing and instead reaching for an O(n) extra-space hashset (valid but not optimal under O(1)-space constraint).
- **Interview Value:** High — a favorite "test if you really understand Floyd's algorithm" problem.
- **Related Problems:** LC 141.
- **Notes:** 📌 **Revision Tip:** Re-derive *why* the cycle entry point equals the duplicate — don't just memorize the two-phase pointer trick.

#### LC 146 — LRU Cache
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 5 → Linked List → Doubly Linked List + Hashmap design
- **Pattern:** Hashmap + Doubly Linked List for O(1) get/put with eviction order
- **Why here:** The definitive linked-list "design" problem — combines hashmap O(1) lookup (Week 2/3 theory) with doubly-linked-list O(1) reordering, synthesizing nearly everything learned about lists so far.
- **Prerequisites:** LC 206 and general node-class fluency; dict basics.
- **Best approach:** Maintain a dict of `key -> node` plus a doubly linked list ordered by recency; on get/put, move the accessed node to the front (most-recently-used end) and evict from the back when over capacity.
- **Time Complexity:** O(1) per operation.
- **Space Complexity:** O(capacity)
- ⚠️ **Common Mistakes:**
  - Using a plain Python list/OrderedDict shortcut without understanding the underlying doubly-linked-list mechanics (acceptable in production, but interviewers usually want the from-scratch version).
  - Forgetting to update both `prev` and `next` pointers symmetrically when unlinking/relinking nodes.
- **Interview Value:** Very High — one of the most frequently asked "design" interview questions across all companies.
- **Related Problems:** LC 355, LC 295.
- **Notes:** ⚠️ **Common Trap:** Forgetting dummy head/tail sentinels, which simplifies edge cases enormously if used.

### What should be solved immediately after Lecture 5.1
LC 206, LC 143, LC 19, LC 141, LC 146 (P1).

### What should be solved during revision
LC 138, LC 2, LC 287 (P2).

## Lecture 5.2 — Single Source Shortest Paths (Dijkstra's Algorithm)
### What this lecture teaches
Dijkstra's algorithm using a priority queue to greedily settle shortest distances in a non-negatively-weighted graph.
### Core DSA ideas
Priority-queue-driven greedy shortest path — the canonical weighted-graph algorithm.
### Relevant NeetCode problems

#### LC 743 — Network Delay Time
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 5 → Lecture 5.2 → Graphs → Dijkstra's Algorithm
- **Pattern:** Dijkstra's Algorithm with a min-heap
- **Why here:** The single most direct, textbook application of Dijkstra's algorithm in NC150 — solve this immediately after the lecture.
- **Prerequisites:** Heap basics (formally covered Week 6, but Python's `heapq` module is usable now); adjacency list construction.
- **Best approach:** Min-heap of `(distance, node)`; pop the closest unvisited node, relax its neighbors' distances, repeat until heap is empty.
- **Time Complexity:** O(E log V)
- **Space Complexity:** O(V + E)
- ⚠️ **Common Mistakes:**
  - Not skipping a popped node if a shorter distance to it was already finalized (stale heap entries).
  - Forgetting Dijkstra fails with negative edge weights (motivates Bellman-Ford next, 5.3).
- **Interview Value:** High.
- **Related Problems:** LC 778, LC 787.
- **Notes:** 💡 **Pattern Recognition:** "shortest path, non-negative weights" → Dijkstra with a min-heap.

#### LC 1584 — Min Cost to Connect All Points
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 5 → Lecture 5.2 (secondary fit: more precisely Prim's MST, 5.6) → Graphs → MST via Prim's
- **Pattern:** Prim's Algorithm (min-heap-driven MST), structurally similar to Dijkstra
- **Why here:** Placed here because the heap-driven greedy mechanics are nearly identical to Dijkstra's, even though it's conceptually an MST problem (formally covered in 5.6) — solving it right after Dijkstra helps you see the structural similarity and difference (shortest path tree vs minimum spanning tree).
- **Prerequisites:** LC 743 solved first.
- **Best approach:** Prim's algorithm — start from any point, repeatedly add the minimum-cost edge connecting a new point to the growing tree, using a min-heap of candidate edges.
- **Time Complexity:** O(n² log n) or O(n²) with optimization for dense graphs (since this is effectively a complete graph on points).
- **Space Complexity:** O(n²) for all pairwise edges, or O(n) with lazy edge generation.
- ⚠️ **Common Mistakes:** Confusing Prim's (grows one connected tree) with Kruskal's (processes globally sorted edges) — know which one you're implementing.
- **Interview Value:** Medium.
- **Related Problems:** LC 743, LC 684 (Kruskal's-style, Week 6).
- **Notes:** 📌 **Revision Tip:** Revisit explicitly after Lecture 5.6/5.7 once Prim's and Kruskal's are formally distinguished.

### What should be solved immediately after Lecture 5.2
LC 743 (P1).

## Lecture 5.3 — Single Source Shortest Paths with Negative Weights (Bellman-Ford Algorithm)
### What this lecture teaches
Bellman-Ford's relaxation-based algorithm, which tolerates negative edge weights and detects negative cycles, at the cost of O(VE) complexity.
### Core DSA ideas
Edge relaxation repeated V-1 times — a DP-flavored algorithm (each relaxation pass is like a DP transition).
### Relevant NeetCode problems

#### LC 787 — Cheapest Flights Within K Stops
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 5 → Lecture 5.3 → Graphs → Bellman-Ford (bounded relaxations)
- **Pattern:** Modified Bellman-Ford, limited to K relaxation rounds
- **Why here:** A direct, almost literal application of Bellman-Ford where the "K stops" constraint maps exactly onto "K relaxation passes" — solve immediately after 5.3.
- **Prerequisites:** LC 743 (to contrast with Dijkstra, since this problem's "at most K stops" constraint breaks Dijkstra's standard greedy assumption).
- **Best approach:** Run Bellman-Ford-style relaxation for exactly K+1 rounds, using a temporary distance array per round to prevent using updated values within the same round.
- **Time Complexity:** O(K × E)
- **Space Complexity:** O(V)
- ⚠️ **Common Mistakes:**
  - Updating the distance array in place during a single round (allows using more than K edges in one effective "round," giving wrong answers).
  - Trying to force Dijkstra here without modification — fails because Dijkstra doesn't naturally respect a hop-count limit.
- **Interview Value:** High.
- **Related Problems:** LC 743.
- **Notes:** ⚠️ **Common Trap:** This problem is the most common place people misapply Dijkstra; always check if there's a hop/stop constraint before choosing your algorithm.

### What should be solved immediately after Lecture 5.3
LC 787 (P1).

## Lecture 5.4 — All Pairs Shortest Paths (Floyd-Warshall Algorithm)
### What this lecture teaches
Floyd-Warshall's O(V³) DP algorithm for computing shortest paths between every pair of vertices simultaneously.
### Core DSA ideas
All-pairs DP relaxation — another DP-on-graph pattern, reinforcing the Week 9 DP connection.
### Relevant NeetCode problems
No NeetCode 150 problem requires Floyd-Warshall specifically (all-pairs shortest path problems in NC150 are solvable with simpler single-source approaches). **Flagged as Interview Extra / Theory-Only for NC150 purposes** — understand the algorithm conceptually since it may appear in interviews outside the NC150 problem set, but no problem here needs it directly.

## Lecture 5.5 — Minimum Cost Spanning Trees
### What this lecture teaches
MST definition and motivation — the minimum-weight subset of edges connecting all vertices.
### Core DSA ideas
Sets up both greedy MST algorithms that follow.
### Relevant NeetCode problems
None directly — conceptual setup.

## Lecture 5.6 — Minimum Cost Spanning Trees (Prim's Algorithm)
### What this lecture teaches
Prim's algorithm: grow a single tree by repeatedly adding the cheapest edge to an unvisited vertex.
### Core DSA ideas
Greedy tree growth via a priority queue.
### Relevant NeetCode problems
**Revisit LC 1584 here** (originally placed under 5.2 for heap-mechanics similarity to Dijkstra) — this is its true formal home. 📌 **Revision Tip:** If you skipped it in 5.2, solve it now; if you solved it then, re-derive it from memory now to confirm you understand Prim's specifically (not just "a heap-based greedy algorithm").

## Lecture 5.7 — Minimum Cost Spanning Trees (Kruskal's Algorithm)
### What this lecture teaches
Kruskal's algorithm: globally sort all edges, greedily add the cheapest edge that doesn't create a cycle (using Union-Find to detect cycles efficiently).
### Core DSA ideas
This lecture is the direct motivation for **why Union-Find exists** — Kruskal's needs an efficient cycle check, which Week 6 formalizes.
### Relevant NeetCode problems

#### LC 684 — Redundant Connection
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 5 → Lecture 5.7 (secondary fit: pure Union-Find application, formalized Week 6) → Graphs → Union-Find Cycle Detection
- **Pattern:** Union-Find (Kruskal's-style edge processing without the MST weight-sorting, since this graph is unweighted)
- **Why here:** Directly demonstrates *why* Kruskal's needs Union-Find — finding the one edge that creates a cycle when added is the same sub-problem Kruskal's solves at every step.
- **Prerequisites:** Conceptual Union-Find idea (formally taught Week 6, but the lecture's mention of "using Union-Find to detect cycles" is enough to attempt this now, or defer to Week 6 if you prefer the formal structure first).
- **Best approach:** Process edges in input order; for each edge, check if its two endpoints are already connected (Union-Find `find`); if so, this edge is redundant; otherwise `union` them.
- **Time Complexity:** O(E) with union by rank/path compression (amortized near-O(1) per operation).
- **Space Complexity:** O(V)
- ⚠️ **Common Mistakes:** Implementing Union-Find without path compression/union by rank, degrading to O(E²) worst case.
- **Interview Value:** High.
- **Related Problems:** LC 323, LC 261.
- **Notes:** 📌 **Revision Tip:** This problem is listed here for thematic continuity with Kruskal's, but its *formal* prerequisite lecture is 6.1 — if Union-Find isn't comfortable yet, solve it in Week 6 instead and treat this listing as a forward pointer.

### What should be solved immediately after Week 5
LC 206, LC 143, LC 19, LC 141, LC 146, LC 743, LC 787 (P1) — and LC 684 once Union-Find is comfortable (Week 6).

### What should be solved during revision
LC 138, LC 2, LC 287, LC 1584 (P2).

### What should be left for later
Floyd-Warshall — theory only, no NC150 problem requires it directly.

---

# Week 6 — Union-Find, Priority Queues, Heaps & Search Trees

**Lectures covered:** 6.1 – 6.5
**Main topic:** Union-Find data structure; Priority Queues and Heaps as their implementation; applications of heaps; introduction to Search Trees (BSTs).
**DSA pattern introduced:** Union-Find (Disjoint Set), Heap/Priority Queue operations, Binary Search Tree property.

## Lecture 6.1 — Union-Find Data Structure
### What this lecture teaches
Disjoint Set Union (DSU): `find` and `union` operations, path compression, union by rank/size, near-O(1) amortized operations.
### Core DSA ideas
Union-Find as a formal, named structure — the proper home for LC 684 (previewed in Week 5) and its siblings.
### Relevant NeetCode problems

#### LC 684 — Redundant Connection *(formal treatment)*
*(See full entry under Week 5 → Lecture 5.7. This is its primary formal home — solve it here if deferred from Week 5.)*
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.1 → Union-Find → Cycle Detection

#### LC 323 — Number of Connected Components *(Union-Find alternative solution)*
- **Difficulty:** Medium
- **Priority:** P2 *(revision: re-solve using Union-Find instead of DFS)*
- **Mapped to:** Week 6 → Lecture 6.1 → Union-Find → Component Counting
- **Pattern:** Union-Find, counting distinct roots
- **Why here:** Same problem as Week 4's DFS solution — solving it again with Union-Find directly compares the two standard approaches to connectivity problems, which is excellent revision value.
- **Prerequisites:** LC 684 (Union-Find basics).
- **Best approach:** Initialize n disjoint sets; union each edge's endpoints; count distinct roots remaining (or track a running count, decrementing on each successful union).
- **Time Complexity:** O(E) amortized with path compression + union by rank.
- **Space Complexity:** O(V)
- ⚠️ **Common Mistakes:** Forgetting path compression, leading to degraded performance on long chains.
- **Interview Value:** High.
- **Related Problems:** LC 684, LC 261.
- **Notes:** 📌 **Revision Tip:** Practice writing a clean, reusable Union-Find class — it's reused across at least 3 problems in this handbook.

#### LC 261 — Graph Valid Tree *(Union-Find alternative solution)*
- **Priority:** P2 *(revision: re-solve using Union-Find)*
- **Mapped to:** Week 6 → Lecture 6.1 → Union-Find
- **Why here:** Same logic as LC 323 above — a graph is a tree iff union-find never detects a cycle and exactly n-1 unions succeed.
- *(Full field details under Week 4 entry — apply Union-Find as the alternate implementation here.)*

### What should be solved immediately after Lecture 6.1
LC 684 (P1, if not already solved in Week 5).

### What should be solved during revision
LC 323, LC 261 — re-solve with Union-Find (P2, revision pass).

## Lecture 6.2 — Priority Queues
### What this lecture teaches
The Priority Queue abstract data type: insert, extract-min/max — and why a naive array/list implementation is too slow for repeated extraction.
### Core DSA ideas
Motivates the heap as the efficient implementation of a priority queue.
### Relevant NeetCode problems
None directly — conceptual motivation lecture.

## Lecture 6.3 — Heaps
### What this lecture teaches
Binary heap structure (array-backed, implicit tree), heapify, insert/extract in O(log n).
### Core DSA ideas
The Heap data structure itself — the implementation vehicle for every Priority Queue problem below.
### Relevant NeetCode problems

#### LC 703 — Kth Largest Element in a Stream
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.3 → Heap/Priority Queue → Fixed-size min-heap
- **Pattern:** Min-heap of size k
- **Why here:** The simplest possible heap application — maintain a min-heap capped at size k; its top is always the kth largest seen so far. Ideal first heap problem.
- **Prerequisites:** Python `heapq` module basics.
- **Best approach:** Maintain a min-heap of size k; for each new value, push it, and if size exceeds k, pop the smallest.
- **Time Complexity:** O(log k) per insertion.
- **Space Complexity:** O(k)
- ⚠️ **Common Mistakes:** Using a max-heap by mistake (Python's `heapq` is min-heap only; negate values for max-heap behavior).
- **Interview Value:** Medium.
- **Related Problems:** LC 215, LC 973.
- **Notes:** 💡 **Pattern Recognition:** "kth largest/smallest, streaming or static" → fixed-size heap.

#### LC 1046 — Last Stone Weight
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.3 → Heap/Priority Queue → Max-heap simulation
- **Pattern:** Max-heap (via negation) repeated extraction
- **Why here:** Simple repeated extract-max-twice-and-reinsert simulation — good direct application immediately after heap basics.
- **Prerequisites:** LC 703.
- **Best approach:** Negate all values to simulate a max-heap with Python's min-heap; repeatedly pop the two largest, push back their (negated) difference, until one or zero stones remain.
- **Time Complexity:** O(n log n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Forgetting to re-negate values correctly when pushing the difference back.
- **Interview Value:** Low-Medium (simple, but good warm-up).
- **Related Problems:** LC 973, LC 1046.
- **Notes:** Quick, satisfying problem to build heap confidence.

#### LC 973 — K Closest Points to Origin
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.3 → Heap/Priority Queue → Fixed-size max-heap by custom key
- **Pattern:** Heap with custom comparison key (distance)
- **Why here:** Generalizes LC 703's "k closest/largest" idea to a custom distance metric and 2D points — natural next step.
- **Prerequisites:** LC 703.
- **Best approach:** Push `(-distance, point)` onto a heap capped at size k (or use `heapq.nsmallest`); alternatively sort by distance and take the first k.
- **Time Complexity:** O(n log k) with a capped heap.
- **Space Complexity:** O(k)
- ⚠️ **Common Mistakes:** Computing actual Euclidean distance (with sqrt) instead of squared distance — unnecessary and slower.
- **Interview Value:** High.
- **Related Problems:** LC 703, LC 215.
- **Notes:** 📌 **Revision Tip:** Compare three approaches: full sort O(n log n), heap O(n log k), and Quick Select O(n) average (Week 8) — know all three exist.

#### LC 215 — Kth Largest Element in an Array *(heap approach — Quick Select alternative in Week 8)*
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 6 → Lecture 6.3 → Heap/Priority Queue (secondary fit: Quick Select, Week 8 — the optimal approach)
- **Pattern:** Min-heap of size k (heap approach); Quick Select (optimal approach, Week 8)
- **Why here:** Solve once now with a heap for O(n log k) — you will re-solve it in Week 8 with Quick Select for the average-O(n) optimal approach, explicitly comparing both.
- **Prerequisites:** LC 703.
- **Best approach (heap):** Same fixed-size min-heap pattern as LC 703.
- **Time Complexity:** O(n log k) heap approach; O(n) average with Quick Select.
- **Space Complexity:** O(k) heap approach.
- ⚠️ **Common Mistakes:** Sorting the whole array (O(n log n)) when a heap or Quick Select is asymptotically better for k ≪ n.
- **Interview Value:** Very High — extremely common, and explicitly tests whether you know multiple approaches with different tradeoffs.
- **Related Problems:** LC 703, LC 973, LC 347.
- **Notes:** 📌 **Revision Tip:** This is one of the best "show me three approaches" problems to rehearse before interviews.

### What should be solved immediately after Lecture 6.3
LC 703, LC 1046, LC 973 (P1).

### What should be solved during revision
LC 215 (P2 — heap approach now, Quick Select approach in Week 8).

## Lecture 6.4 — Using Heaps in Algorithms
### What this lecture teaches
Heaps embedded inside larger algorithms (e.g., heap-based sorting, k-way merge, scheduling) rather than as standalone exercises.
### Core DSA ideas
Heap as a *component* of a bigger algorithm — directly the pattern in every problem below.
### Relevant NeetCode problems

#### LC 621 — Task Scheduler
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.4 → Heap/Priority Queue → Greedy scheduling with max-heap + cooldown queue
- **Pattern:** Max-heap (frequency-based) + cooldown tracking
- **Why here:** A heap embedded inside a greedy scheduling algorithm — exactly what 6.4 promises, combining heap mechanics with a queue-based cooldown structure.
- **Prerequisites:** Frequency counting (Week 2/3); heap basics.
- **Best approach:** Max-heap of task frequencies; repeatedly pop the most frequent task, decrement, and place it in a cooldown queue until `n` cycles have passed before it's eligible again.
- **Time Complexity:** O(n log 26) ≈ O(n) since the alphabet of tasks is bounded.
- **Space Complexity:** O(1) (bounded by 26 task types) / O(n) generally.
- ⚠️ **Common Mistakes:** Forgetting to still "spend" idle cycles even when the heap and cooldown queue are both temporarily empty.
- **Interview Value:** High.
- **Related Problems:** LC 1046, LC 295.
- **Notes:** ⚠️ **Common Trap:** A purely mathematical formula-based solution exists too (using max frequency and counting), but the heap simulation is more intuitive to derive under interview pressure.

#### LC 355 — Design Twitter
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 6 → Lecture 6.4 → Heap/Priority Queue → K-way merge via heap (secondary fit: System Design Extra)
- **Pattern:** Heap-based k-way merge of per-user tweet timelines
- **Why here:** The "get news feed" operation is structurally a k-way merge (merging each followed user's tweet list by timestamp), the same family as merge sort's merge step (Week 2) generalized via a heap.
- **Prerequisites:** LC 146 (design problem mechanics); heap basics.
- **Best approach:** Store tweets per user with timestamps; for `getNewsFeed`, push the most recent tweet of each followed user onto a max-heap (by timestamp), repeatedly pop and push the next tweet from that user, until 10 tweets are collected.
- **Time Complexity:** O(k log k) per feed fetch, where k = number of followees.
- **Space Complexity:** O(users × tweets)
- ⚠️ **Common Mistakes:** Re-sorting the entire tweet history on every feed request instead of using the heap-based k-way merge.
- **Interview Value:** Medium (less common than LRU Cache, but a good "design + heap" hybrid).
- **Related Problems:** LC 146, LC 23.
- **Notes:** A genuinely "design"-flavored problem — see Appendix E for more on Design questions as a category.

#### LC 295 — Find Median from Data Stream
- **Difficulty:** Hard
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.4 → Heap/Priority Queue → Two-heap technique
- **Pattern:** Two heaps (max-heap for lower half, min-heap for upper half)
- **Why here:** The canonical "two heaps" problem — a direct, high-value application of using heaps as algorithm components rather than standalone structures.
- **Prerequisites:** Heap basics, LC 215/973.
- **Best approach:** Maintain a max-heap for the smaller half of seen numbers and a min-heap for the larger half, keeping their sizes balanced (differ by at most 1); median is either the top of the larger heap or the average of both tops.
- **Time Complexity:** O(log n) per insertion, O(1) per median query.
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Letting the two heaps drift out of balance, or forgetting to rebalance after every insertion.
- **Interview Value:** Very High — a favorite hard-heap interview question across many companies.
- **Related Problems:** LC 703, LC 973, LC 215.
- **Notes:** 📌 **Revision Tip:** This is a "must be instant" problem before any interview — the two-heap balancing logic should be automatic.

### What should be solved immediately after Lecture 6.4
LC 621, LC 295 (P1).

### What should be solved during revision
LC 355 (P2).

## Lecture 6.5 — Search Trees
### What this lecture teaches
Binary Search Trees: the BST invariant (left < node < right), search/insert/delete operations, and why BSTs enable O(log n) operations on average (height-dependent).
### Core DSA ideas
This is the formal introduction to **Trees** as a topic — per this handbook's Week 4/5 framing, trees are DAGs with a single root and unique root-to-node paths; the BST adds an ordering invariant on top.

> 📌 **Sequencing Note:** Because trees only get formally introduced here, **all general binary tree problems (traversal, depth, diameter, etc.) are grouped into this lecture and the appendix's "Trees" topic**, even though many of them don't strictly require the BST ordering invariant. This is a deliberate, clearly-labeled grouping decision: general trees are introduced as a *specialization* of graphs (Week 4) that BSTs further specialize.

### Relevant NeetCode problems — General Binary Trees (secondary fit: grouped here for syllabus continuity)

#### LC 226 — Invert Binary Tree
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → Recursive DFS traversal
- **Pattern:** Recursive tree traversal (post-order-ish swap)
- **Why here:** The simplest possible tree-recursion problem — ideal first exposure to "trees as recursive structures" right as Search Trees are introduced.
- **Prerequisites:** Node class (1.7); basic recursion.
- **Best approach:** Recursively swap left and right children at every node.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h) recursion stack (h = height).
- ⚠️ **Common Mistakes:** Swapping references incorrectly (losing one subtree before reassigning).
- **Interview Value:** Medium (famous as "the Homebrew interview question" but genuinely a good fluency check).
- **Related Problems:** LC 100, LC 572.
- **Notes:** Often used as a 5-minute warm-up question.

#### LC 104 — Maximum Depth of Binary Tree
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → Recursive height computation
- **Pattern:** Recursive DFS, `1 + max(left, right)`
- **Why here:** The base pattern that LC 543, LC 110 directly build on.
- **Prerequisites:** LC 226.
- **Best approach:** `return 1 + max(depth(left), depth(right))`, base case `None -> 0`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Forgetting the base case returns 0, not 1.
- **Interview Value:** Medium.
- **Related Problems:** LC 543, LC 110.
- **Notes:** Foundational recursive tree pattern — internalize this exact recursion shape.

#### LC 543 — Diameter of Binary Tree
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → Recursive height + global max tracking
- **Pattern:** DFS height computation with a side-effect global/nonlocal max update
- **Why here:** Direct extension of LC 104 — instead of just returning height, you also track the best "left height + right height" seen at any node.
- **Prerequisites:** LC 104.
- **Best approach:** Recursive height function that, at each node, updates a running max of `left_height + right_height` before returning `1 + max(left_height, right_height)`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Computing diameter as "edges through the root" only, missing diameters entirely within a subtree.
- **Interview Value:** High.
- **Related Problems:** LC 104, LC 124.
- **Notes:** 💡 **Pattern Recognition:** "longest path between any two nodes" → height computation with a side max update, not a separate top-down check.

#### LC 110 — Balanced Binary Tree
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → Recursive height + early-exit on imbalance
- **Pattern:** Bottom-up DFS height with a sentinel "imbalanced" signal
- **Why here:** Another LC 104 variant, this time propagating a failure signal up the recursion to avoid O(n²) re-computation.
- **Prerequisites:** LC 104, LC 543.
- **Best approach:** Recursive height function that returns -1 (or similar sentinel) as soon as any subtree is found imbalanced, short-circuiting further computation.
- **Time Complexity:** O(n) with the sentinel trick; naive top-down recomputation is O(n²).
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Computing height and balance separately (top-down), causing O(n²) blowup on skewed trees.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 104, LC 543.
- **Notes:** Good test of whether you can fold a boolean check into a height-returning recursion.

#### LC 100 — Same Tree
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → Simultaneous recursive comparison
- **Pattern:** Synchronized DFS over two trees
- **Why here:** Simplest "compare two trees" problem — direct prerequisite skill for LC 572.
- **Prerequisites:** LC 226.
- **Best approach:** Recursively compare node values and structure of both trees simultaneously; base cases for both `None`, one `None`, or value mismatch.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Forgetting to check both subtrees' equality (returning early on just the left).
- **Interview Value:** Medium.
- **Related Problems:** LC 572.
- **Notes:** Foundational for tree-comparison-style problems.

#### LC 572 — Subtree of Another Tree
- **Difficulty:** Easy
- **Priority:** P2
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → Same-Tree check applied at every node
- **Pattern:** DFS + Same-Tree subroutine
- **Why here:** Direct composition: at every node of the main tree, run the LC 100 "same tree" check against the candidate subtree.
- **Prerequisites:** LC 100 must be solid.
- **Best approach:** DFS through the main tree; at each node, call the `isSameTree` helper comparing that node's subtree against the target subtree.
- **Time Complexity:** O(n × m) worst case (n = main tree size, m = subtree size).
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Comparing only values without verifying full structural equality (missing `None` mismatches).
- **Interview Value:** Medium.
- **Related Problems:** LC 100.
- **Notes:** Good composition exercise once LC 100 is automatic.

#### LC 102 — Binary Tree Level Order Traversal
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → BFS (secondary fit: directly reuses Week 4's BFS pattern)
- **Pattern:** BFS with level-boundary tracking
- **Why here:** First tree problem requiring BFS instead of DFS — direct callback to Week 4's queue-based traversal, now applied to trees specifically with explicit level grouping.
- **Prerequisites:** Week 4 BFS comfort; queue usage.
- **Best approach:** BFS with a queue; process one full level at a time by snapshotting the current queue size before the inner loop.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n) worst case (wide tree)
- ⚠️ **Common Mistakes:** Not snapshotting level size before the inner loop, causing incorrect level boundaries.
- **Interview Value:** Very High — extremely common, and the base pattern for LC 199.
- **Related Problems:** LC 199, LC 1448.
- **Notes:** 💡 **Pattern Recognition:** "process level by level" or "level order" → BFS with queue-size snapshotting.

#### LC 199 — Binary Tree Right Side View
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → BFS, last-element-per-level
- **Pattern:** BFS with level tracking, take rightmost
- **Why here:** Direct, minor variant of LC 102 — same level-order BFS, but only keep the last node visited per level.
- **Prerequisites:** LC 102.
- **Best approach:** Same level-order BFS as LC 102; append only the last node's value processed in each level's inner loop.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Trying to solve with DFS and getting the right/left traversal order confused (BFS is more naturally bug-free here).
- **Interview Value:** Medium-High.
- **Related Problems:** LC 102.
- **Notes:** Solve immediately after LC 102 for an easy confidence win.

#### LC 1448 — Count Good Nodes in Binary Tree
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 6 → Lecture 6.5 → Trees → DFS with running max parameter
- **Pattern:** DFS passing down an accumulated "max so far" value
- **Why here:** Introduces the technique of passing extra state *down* the recursion (not just returning state up), a pattern reused heavily in BST validation (LC 98) right after.
- **Prerequisites:** LC 226/104-level recursion comfort.
- **Best approach:** DFS(node, max_so_far) — a node is "good" if its value ≥ max_so_far; recurse into children with `max(max_so_far, node.val)`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Tracking max as a return value instead of a passed-down parameter, overcomplicating the solution.
- **Interview Value:** Medium.
- **Related Problems:** LC 98.
- **Notes:** 💡 **Pattern Recognition:** "track a running constraint from root to current node" → pass state down as a function parameter, don't try to return it up.

### Relevant NeetCode problems — Binary Search Trees (direct fit for 6.5)

#### LC 235 — Lowest Common Ancestor of a Binary Search Tree
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Search Trees → BST property exploitation
- **Pattern:** BST-guided descent (no need to explore both subtrees)
- **Why here:** The first problem that actually *requires* the BST ordering invariant (not just "is a tree") — ideal first BST-specific problem.
- **Prerequisites:** BST invariant understanding (6.5's core lecture content).
- **Best approach:** Starting at the root, move left if both target values are smaller, right if both are larger, otherwise the current node is the LCA.
- **Time Complexity:** O(h) — O(log n) for balanced, O(n) worst case for skewed.
- **Space Complexity:** O(1) iterative; O(h) recursive.
- ⚠️ **Common Mistakes:** Using the general-tree LCA algorithm (which works but is O(n) and ignores the BST property the problem hands you for free).
- **Interview Value:** High.
- **Related Problems:** LC 230, LC 98.
- **Notes:** 💡 **Pattern Recognition:** "lowest common ancestor" + "binary search tree" → use the ordering to guide a single descent, don't do general-tree LCA.

#### LC 98 — Validate Binary Search Tree
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Search Trees → DFS with valid-range bounds
- **Pattern:** DFS passing down (min, max) bounds — direct reuse of LC 1448's "state passed down" technique
- **Why here:** The canonical BST-property-checking problem, and the cleanest application of the "pass constraints down via parameters" technique just practiced in LC 1448.
- **Prerequisites:** LC 1448 (state-passing technique); BST invariant.
- **Best approach:** DFS(node, low, high) — node's value must satisfy `low < node.val < high`; recurse with updated bounds for each child.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Only checking a node against its immediate parent instead of the full inherited range (a classic bug that passes simple test cases but fails on deeper violations).
- **Interview Value:** Very High.
- **Related Problems:** LC 235, LC 230.
- **Notes:** ⚠️ **Common Trap:** "Compare only to parent" is the single most common wrong approach here — always use inherited min/max bounds.

#### LC 230 — Kth Smallest Element in a BST
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 6 → Lecture 6.5 → Search Trees → In-order traversal property
- **Pattern:** In-order DFS traversal (yields sorted order in a BST)
- **Why here:** Directly demonstrates the single most important BST fact: in-order traversal visits nodes in sorted order — essential, high-value insight.
- **Prerequisites:** BST invariant; basic DFS.
- **Best approach:** In-order traversal (iterative with an explicit stack is more efficient than full recursive traversal), counting nodes visited until the kth is reached; can stop early.
- **Time Complexity:** O(h + k)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Doing a full traversal into a list and then indexing (works, but wastes the early-termination opportunity of an iterative in-order traversal).
- **Interview Value:** High.
- **Related Problems:** LC 235, LC 98.
- **Notes:** 💡 **Pattern Recognition:** "kth smallest/sorted-order question about a BST" → in-order traversal, always.

### What should be solved immediately after Lecture 6.5
LC 226, LC 104, LC 543, LC 110, LC 100, LC 102, LC 235, LC 98, LC 230 (P1).

### What should be solved during revision
LC 572, LC 199, LC 1448 (P2).

---

# Week 7 — Balanced Search Trees & Greedy Algorithms

**Lectures covered:** 7.1 – 7.4
**Main topic:** Balanced BSTs (height-balancing motivation); Greedy algorithm design via three classic case studies — interval scheduling, minimizing lateness, Huffman coding.
**DSA pattern introduced:** Tree balancing concepts (Tries and advanced tree construction as extensions); Greedy choice + exchange-argument thinking; Interval scheduling pattern.

## Lecture 7.1 — Balanced Search Trees
### What this lecture teaches
Why unbalanced BSTs degrade to O(n) operations, and the motivation for self-balancing structures (AVL/Red-Black trees, taught conceptually, not necessarily implemented).
### Core DSA ideas
Height-balance guarantees — theoretical backing for why advanced tree-construction and Trie problems below are efficient.
### Relevant NeetCode problems — Advanced Tree Construction (secondary fit: grouped here for syllabus continuity with tree theory)

#### LC 105 — Construct Binary Tree from Preorder and Inorder Traversal
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.1 → Trees → Recursive construction from traversal arrays
- **Pattern:** Recursive divide using traversal array properties (preorder root-first, inorder split point)
- **Why here:** A natural extension of tree theory — building a tree from its traversal signature requires deep understanding of what each traversal order actually encodes, which is the same conceptual depth balanced-tree theory requires.
- **Prerequisites:** Solid grasp of preorder/inorder traversal definitions; LC 230's in-order intuition helps.
- **Best approach:** The first element of preorder is always the root; find that value's position in inorder to split left/right subtree ranges; recurse, using a hashmap for O(1) inorder index lookups.
- **Time Complexity:** O(n) with hashmap-indexed lookups; O(n²) naive with repeated linear search.
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Re-searching the inorder array linearly for each root instead of precomputing a value-to-index map.
- **Interview Value:** High.
- **Related Problems:** LC 297.
- **Notes:** 📌 **Revision Tip:** Practice deriving why preorder's first element is always the root, and why inorder's split point at that value gives exact left/right subtree boundaries — don't just memorize the recursion.

#### LC 124 — Binary Tree Maximum Path Sum
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 7 → Lecture 7.1 → Trees → DFS height-style recursion with global max tracking
- **Pattern:** Same "compute-and-track-global-max" pattern as LC 543 (Diameter), generalized to weighted path sums
- **Why here:** Direct generalization of LC 543's diameter technique — instead of height, you track the maximum downward path sum at each node, updating a global max with "left + right + node" at every step.
- **Prerequisites:** LC 543 must be solid.
- **Best approach:** Recursive function returns the best *single-direction* downward path sum from a node (clamped at 0 to ignore negative branches); at each node, update the global max using `left + right + node.val`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(h)
- ⚠️ **Common Mistakes:** Returning `left + right + node.val` from the recursion itself (incorrect — only one branch can be used going upward, not both).
- **Interview Value:** High.
- **Related Problems:** LC 543.
- **Notes:** ⚠️ **Common Trap:** Clamping negative subtree sums to 0 is essential — forgetting this breaks the answer on trees with negative values.

#### LC 297 — Serialize and Deserialize Binary Tree
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 7 → Lecture 7.1 → Trees → Preorder encoding with null markers
- **Pattern:** Preorder DFS serialization + recursive reconstruction
- **Why here:** Synthesizes LC 105's "reconstruct from traversal" thinking with LC 271's (Week 3) string-encoding discipline.
- **Prerequisites:** LC 105, LC 271.
- **Best approach:** Serialize via preorder DFS, explicitly encoding `null` for missing children (e.g., comma-separated string with a sentinel like `"N"`); deserialize by consuming the token stream in the same preorder fashion.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Omitting null markers (then the tree shape becomes ambiguous on deserialization — preorder alone isn't enough without them).
- **Interview Value:** High.
- **Related Problems:** LC 105, LC 271.
- **Notes:** 📌 **Revision Tip:** Use an iterator/index pointer (not array slicing) during deserialization for O(n) instead of accidental O(n²).

### Relevant NeetCode problems — Tries (secondary fit: balanced/efficient tree structures, formal home in Week 10's String Matching block, previewed here)

> 📌 The Trie data structure is formally taught in **Lecture 10.6 (String Matching - Tries)**. It is *mentioned* here only as a forward pointer because conceptually a Trie is a tree, and learners often want to attempt it once general tree-construction fluency (7.1) is solid. **Full entries for LC 208, LC 211, LC 212 are placed in Week 10**, where they belong by direct syllabus mapping — do not skip ahead unless comfortable.

### What should be solved immediately after Lecture 7.1
LC 105 (P1).

### What should be solved during revision
LC 124, LC 297 (P2).

## Lecture 7.2 — Greedy Algorithms: Interval Scheduling
### What this lecture teaches
The classic interval scheduling maximization problem: given intervals, select the maximum number that don't overlap, solved greedily by sorting on end time.
### Core DSA ideas
**Greedy + sort by relevant key** — the single most reusable pattern in the entire Intervals category.
### Relevant NeetCode problems

#### LC 57 — Insert Interval
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.2 → Intervals → Sorted Merge-Insertion
- **Pattern:** Linear scan exploiting pre-sorted input, three-phase merge
- **Why here:** Interval manipulation builds directly on the sort-and-scan thinking just introduced — a good "manipulate intervals" problem before the "select/count intervals" problems that follow.
- **Prerequisites:** Comfortable array/list manipulation; understanding of interval overlap conditions.
- **Best approach:** Three phases — add all intervals ending before the new interval starts, merge all overlapping intervals into one, then add all intervals starting after the merged interval ends.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Re-sorting the whole array when the input is already guaranteed sorted (wasteful and misses the intended O(n) linear-scan solution).
- **Interview Value:** High.
- **Related Problems:** LC 56, LC 1851.
- **Notes:** 💡 **Pattern Recognition:** "insert one interval into an already-sorted, non-overlapping list" → three-phase linear scan, not full re-sort.

#### LC 56 — Merge Intervals
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.2 → Intervals → Sort by start time, merge overlapping
- **Pattern:** Sort + linear merge scan
- **Why here:** The foundational interval-merging problem, directly using "sort by a key, then scan" — the core mechanic of greedy interval algorithms.
- **Prerequisites:** Sorting comfort (Week 2/3).
- **Best approach:** Sort intervals by start time; iterate, merging the current interval into the last result interval if they overlap, otherwise appending a new interval.
- **Time Complexity:** O(n log n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Forgetting to sort first (or sorting by the wrong key) — the merge logic only works correctly when intervals are processed in start-time order.
- **Interview Value:** Very High — one of the most-cited interval problems.
- **Related Problems:** LC 57, LC 435, LC 252, LC 253.
- **Notes:** 💡 **Pattern Recognition:** "merge/combine overlapping ranges" → sort by start, then linear scan with a "last merged interval" pointer.

#### LC 435 — Non-overlapping Intervals
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.2 → Intervals → Greedy, sort by end time, count removals
- **Pattern:** Classic interval scheduling maximization (inverted to count removals)
- **Why here:** This **is** the textbook interval scheduling problem from 7.2, almost verbatim — sort by end time, greedily keep non-overlapping intervals, count how many had to be discarded.
- **Prerequisites:** LC 56.
- **Best approach:** Sort by end time; greedily keep an interval if its start ≥ the last kept interval's end; count how many intervals were skipped (these are the removals).
- **Time Complexity:** O(n log n)
- **Space Complexity:** O(1) extra
- ⚠️ **Common Mistakes:** Sorting by start time instead of end time — this specific greedy proof only works when sorted by end time.
- **Interview Value:** High.
- **Related Problems:** LC 56, LC 1851.
- **Notes:** 📌 **Revision Tip:** Be ready to explain *why* sorting by end time (not start time) is the correct greedy choice — this is a classic "explain the greedy proof" interview follow-up.

#### LC 252 — Meeting Rooms
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.2 → Intervals → Sort + adjacent overlap check
- **Pattern:** Sort by start, check adjacent pairs for overlap
- **Why here:** The simplest possible interval-scheduling-style question — can a single person attend all meetings, i.e., are there any overlaps at all.
- **Prerequisites:** LC 56.
- **Best approach:** Sort by start time; check if any interval's start is before the previous interval's end.
- **Time Complexity:** O(n log n)
- **Space Complexity:** O(1) extra
- ⚠️ **Common Mistakes:** Off-by-one in the overlap condition (`<` vs `<=` depending on whether touching endpoints count as overlapping).
- **Interview Value:** Medium (often LeetCode premium-locked, but conceptually essential and present in NC150).
- **Related Problems:** LC 253, LC 56.
- **Notes:** Good 5-minute warm-up before LC 253.

#### LC 253 — Meeting Rooms II
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.2 → Intervals → Min-heap of end times (secondary fit: Heaps, Week 6)
- **Pattern:** Sort by start + min-heap tracking active meeting end times
- **Why here:** Direct escalation of LC 252 — instead of yes/no overlap, you need the minimum number of rooms, which requires tracking *how many* meetings are simultaneously active, naturally done with a heap of end times.
- **Prerequisites:** LC 252; heap basics (Week 6).
- **Best approach:** Sort by start time; maintain a min-heap of end times for ongoing meetings; for each new meeting, if the earliest-ending meeting has already ended, reuse that room (pop it); otherwise allocate a new room (push). Heap size at the end is the answer.
- **Time Complexity:** O(n log n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Trying to solve this without a heap using nested loops (works but O(n²), missing the intended O(n log n) approach).
- **Interview Value:** Very High — extremely common interview question (Google, Facebook favorite).
- **Related Problems:** LC 252, LC 1851, LC 295.
- **Notes:** 💡 **Pattern Recognition:** "minimum resources to handle overlapping intervals simultaneously" → min-heap of end times.

#### LC 1851 — Minimum Interval to Include Each Query
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 7 → Lecture 7.2 → Intervals → Sort + min-heap (offline query processing)
- **Pattern:** Sort intervals and queries, sweep with a min-heap of interval sizes
- **Why here:** The hardest interval problem in NC150 — combines interval sorting (7.2) with heap-based size tracking (Week 6), processing queries in sorted order for efficiency.
- **Prerequisites:** LC 253 (heap-of-intervals technique).
- **Best approach:** Sort intervals by start and queries by value; sweep through queries in increasing order, pushing all intervals that have started onto a min-heap keyed by interval size; pop expired intervals (end < query) lazily; the heap top is the smallest valid interval for that query.
- **Time Complexity:** O((n + q) log n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Processing queries in their original order instead of sorted order, breaking the sweep-line invariant.
- **Interview Value:** Medium (less common, but a great test of combining multiple patterns).
- **Related Problems:** LC 253, LC 56.
- **Notes:** Defer full mastery to a revision pass — this problem rewards having LC 56/57/253 already automatic.

### What should be solved immediately after Lecture 7.2
LC 57, LC 56, LC 435, LC 252, LC 253 (P1).

### What should be solved during revision
LC 1851 (P2).

## Lecture 7.3 — Greedy Algorithms: Minimizing Lateness
### What this lecture teaches
A second greedy case study — scheduling jobs with deadlines to minimize maximum lateness, solved by sorting on deadline (earliest-deadline-first).
### Core DSA ideas
Reinforces that **the correct sort key depends on the specific objective** — a different objective (lateness vs interval count) demands a different greedy sort key, even though the algorithmic shape ("sort, then scan greedily") is the same as 7.2.
### Relevant NeetCode problems

#### LC 134 — Gas Station
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → Single-pass greedy with reset-on-deficit
- **Pattern:** Greedy single pass, reset start point whenever the running total goes negative
- **Why here:** A different greedy flavor from 7.3 — instead of sorting, this problem uses a clever invariant (if the total gas ≥ total cost, a valid start exists, and the failure point itself reveals where to restart).
- **Prerequisites:** Comfortable greedy reasoning from 7.2/7.3.
- **Best approach:** Single pass tracking running tank balance; whenever it goes negative, reset the candidate start to the next station and reset the running balance to 0.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Trying a brute-force O(n²) check of every starting station instead of trusting the single-pass greedy invariant.
- **Interview Value:** High.
- **Related Problems:** LC 45, LC 55.
- **Notes:** ⚠️ **Common Trap:** This problem's greedy proof (why resetting at the failure point is always safe) is non-obvious — be ready to explain it, not just code it.

#### LC 55 — Jump Game
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → Furthest-reachable-index tracking
- **Pattern:** Greedy, track the maximum reachable index while scanning
- **Why here:** A clean, simple greedy-feasibility problem, good companion to Gas Station's "can we complete the circuit" feasibility check.
- **Prerequisites:** None beyond basic array scanning.
- **Best approach:** Track `max_reach`; iterate, and if the current index ever exceeds `max_reach`, return False; otherwise update `max_reach = max(max_reach, i + nums[i])`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Using DP/backtracking (works but unnecessary O(n²) or worse — the greedy max-reach approach is strictly better).
- **Interview Value:** High.
- **Related Problems:** LC 45, LC 134.
- **Notes:** 💡 **Pattern Recognition:** "can you reach the end given jump distances" → greedy max-reach tracking, not DP.

#### LC 45 — Jump Game II
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → BFS-flavored greedy "level" expansion
- **Pattern:** Greedy interval/level expansion (implicit BFS levels)
- **Why here:** Direct escalation of LC 55 — now minimizing the *number* of jumps, solved by greedily tracking the farthest reach of the "current jump's range" before being forced to take another jump (conceptually similar to BFS level boundaries from Week 4/6).
- **Prerequisites:** LC 55 must be solid.
- **Best approach:** Track `current_end` (farthest reachable with current jump count) and `farthest` (farthest reachable looking one jump ahead); when the scan index reaches `current_end`, increment jump count and update `current_end = farthest`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Incrementing the jump counter at the wrong index (off-by-one relative to when `current_end` is actually reached).
- **Interview Value:** High.
- **Related Problems:** LC 55, LC 134.
- **Notes:** 📌 **Revision Tip:** Draw out the "current range" vs "next range" boundary on paper before coding — this prevents the classic off-by-one bug.

#### LC 846 — Hand of Straights
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → Sort + greedy consume-from-smallest with frequency map
- **Pattern:** Frequency map + sorted greedy grouping
- **Why here:** Combines hashing (frequency counting, Week 2/3) with a greedy "always start a group from the smallest remaining card" rule — directly analogous to 7.3's "sort, then commit greedily" structure.
- **Prerequisites:** Frequency counting; LC 134/55-level greedy confidence.
- **Best approach:** Count frequencies; repeatedly take the smallest remaining card with count > 0 and consume it and the next `groupSize - 1` consecutive values, decrementing their counts; fail if any required card is missing.
- **Time Complexity:** O(n log n)
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Not always starting from the *current smallest* available card — starting from an arbitrary card can incorrectly fail valid groupings.
- **Interview Value:** Medium.
- **Related Problems:** LC 1899.
- **Notes:** 💡 **Pattern Recognition:** "split into consecutive groups" → always greedily start each group from the smallest remaining element.

#### LC 1899 — Merge Triplets to Form Target Triplet
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → Component-wise feasibility filtering
- **Pattern:** Greedy filtering + component-wise max tracking
- **Why here:** A "greedy by elimination" problem — filter out triplets that can never help (any component exceeding the target), then check if the max of remaining triplets per component reaches the target.
- **Prerequisites:** Comfortable greedy reasoning.
- **Best approach:** Discard any triplet with a component exceeding the corresponding target component; for the rest, track the running max of each of the three components; success if all three running maxes equal the target.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Forgetting to discard invalid triplets first, allowing a component that's too large to incorrectly "help" another component.
- **Interview Value:** Medium.
- **Related Problems:** LC 846.
- **Notes:** Clean, short problem once the filtering insight is seen.

#### LC 763 — Partition Labels
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → Last-occurrence tracking, interval-like partitioning
- **Pattern:** Greedy partition using precomputed last-occurrence indices
- **Why here:** Directly mirrors interval-merging logic (7.2) but derives the "intervals" implicitly from each character's first-to-last occurrence span, then merges/partitions exactly like LC 56.
- **Prerequisites:** LC 56's merge-interval mentality; hashmap for last-occurrence lookup.
- **Best approach:** Precompute the last index of each character; scan left to right, extending the current partition's end to the max last-occurrence seen so far; close the partition when the scan index reaches that end.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1) (bounded alphabet) / O(n) generally.
- ⚠️ **Common Mistakes:** Forgetting to extend the partition boundary dynamically as new characters with later last-occurrences are encountered within the current partition.
- **Interview Value:** High.
- **Related Problems:** LC 56.
- **Notes:** 💡 **Pattern Recognition:** "partition a sequence so each character/element stays within one group" → derive implicit intervals via last-occurrence, then merge like LC 56.

#### LC 678 — Valid Parenthesis String
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 7 → Lecture 7.3 → Greedy → Range tracking (min/max open-paren count)
- **Pattern:** Greedy range tracking for wildcard feasibility
- **Why here:** A greedy-feasibility problem in the same family as LC 55/134 — instead of tracking one value, you track a *range* of possible open-parenthesis counts to handle the wildcard `*`.
- **Prerequisites:** LC 20 (Valid Parentheses, Week 6/elsewhere) mental model; greedy range-tracking comfort.
- **Best approach:** Track `low` and `high` bounds on the possible number of unmatched open parentheses; `(` increments both, `)` decrements both (clamping `low` at 0), `*` decrements `low` and increments `high`; fail if `high` ever goes negative; succeed if `low` is 0 at the end.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Forgetting to clamp `low` at 0 (it cannot go negative, since a `*` can always act as nothing in the worst case).
- **Interview Value:** Medium-High.
- **Related Problems:** LC 22 (Generate Parentheses, Week 6/elsewhere).
- **Notes:** ⚠️ **Common Trap:** Treating `*` as always one specific character instead of tracking the full range of possibilities is the most common conceptual error here.

### What should be solved immediately after Lecture 7.3
LC 134, LC 55, LC 45, LC 763 (P1).

### What should be solved during revision
LC 846, LC 1899, LC 678 (P2).

## Lecture 7.4 — Greedy Algorithms: Huffman Coding
### What this lecture teaches
Huffman's algorithm for optimal prefix-free encoding — repeatedly merging the two lowest-frequency nodes using a min-heap, building an encoding tree bottom-up.
### Core DSA ideas
A greedy algorithm whose implementation vehicle is, once again, a heap (callback to Week 6) — and whose "build a tree bottom-up by merging smallest elements" logic is conceptually identical to the heap simulation in LC 1046 (Last Stone Weight) and LC 621 (Task Scheduler).
### Relevant NeetCode problems
No NeetCode 150 problem implements Huffman Coding directly. **Flagged as Interview Extra / Theory-Only** — the *technique* (repeated greedy merging via a min-heap) is the same one tested in LC 1046 and contributes conceptual depth, but no direct NC150 problem requires Huffman coding itself.

### What should be solved immediately after Week 7
LC 57, LC 56, LC 435, LC 252, LC 253, LC 134, LC 55, LC 45, LC 763, LC 105 (P1).

### What should be solved during revision
LC 1851, LC 846, LC 1899, LC 678, LC 124, LC 297 (P2).

### What should be left for later
Huffman Coding — theory only, no direct NC150 mapping.

---

# Week 8 — Divide and Conquer & Backtracking

**Lectures covered:** 8.1 – 8.6
**Main topic:** Divide-and-conquer algorithm design via four case studies (counting inversions, closest pair of points, integer multiplication, recursion tree analysis), culminating in Quick Select.
**DSA pattern introduced:** Divide & Conquer; Recursion Tree complexity analysis (Master Theorem intuition); Quick Select (partition-based selection); Backtracking (grouped here as recursive exhaustive search, a close cousin of D&C's recursive decomposition).

> 📌 **Sequencing Note:** IITM PDSA has no standalone "Backtracking" week. Backtracking is grouped into Week 8 because it shares Divide & Conquer's core mechanic — recursively breaking a problem into subproblems — but *without* the "combine" step; instead it explores all choices and undoes them (backtracks) on failure. This is a **secondary fit**, clearly labeled, chosen because Week 8 is the syllabus's deepest treatment of recursive problem decomposition, making it the most natural home for backtracking among IITM's actual lecture content.

## Lecture 8.1 — Divide and Conquer: Counting Inversions
### What this lecture teaches
Counting the number of out-of-order pairs in an array using a modified merge sort — O(n log n) instead of brute-force O(n²).
### Core DSA ideas
Augmenting merge sort's merge step to count something extra during the merge — a transferable technique.
### Relevant NeetCode problems
No NeetCode 150 problem requires inversion counting directly. **Flagged as Interview Extra / Theory-Only** — the *technique* of augmenting merge sort is valuable general knowledge (it appears in some "count smaller elements after self" style problems outside NC150) but no direct NC150 mapping exists.

## Lecture 8.2 — Divide and Conquer: Closest Pair of Points
### What this lecture teaches
Finding the closest pair of points in O(n log n) using a divide-and-conquer strategy on sorted coordinates plus a clever strip-merging step.
### Core DSA ideas
Geometric divide-and-conquer.
### Relevant NeetCode problems
No NeetCode 150 problem requires this specific algorithm. **Flagged as Interview Extra / Theory-Only.** (LC 973 — K Closest Points to Origin, Week 6 — is a *different* problem: nearest-to-origin selection via heap, not pairwise closest-pair geometry. Do not confuse the two.)

## Lecture 8.3 — Divide and Conquer: Integer Multiplication
### What this lecture teaches
Karatsuba-style fast multiplication, splitting numbers into halves to multiply in better than O(n²) time.
### Core DSA ideas
Divide-and-conquer applied to arithmetic rather than arrays — a different "shape" of D&C.
### Relevant NeetCode problems

#### LC 43 — Multiply Strings
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 8 → Lecture 8.3 → Math → Digit-by-digit multiplication (secondary fit: the *theory* here is Karatsuba D&C, but NC150's actual problem expects the simpler grade-school digit-multiplication approach, not full Karatsuba)
- **Pattern:** Simulated long multiplication with carry propagation
- **Why here:** Thematically linked to 8.3's "multiply large numbers represented as strings/arrays" framing, even though the expected solution is the simpler O(n×m) digit-by-digit approach rather than full Karatsuba — flagged honestly as a simplified instance of the lecture's theme.
- **Prerequisites:** LC 2 (Add Two Numbers) carry-propagation comfort.
- **Best approach:** Multiply digit by digit (like grade-school multiplication), accumulating results into a result array indexed by digit position, then handle carries at the end.
- **Time Complexity:** O(n × m)
- **Space Complexity:** O(n + m)
- ⚠️ **Common Mistakes:** Converting to native integers directly (works for small inputs but defeats the purpose of the problem, which tests manual big-number arithmetic).
- **Interview Value:** Medium.
- **Related Problems:** LC 2, LC 50.
- **Notes:** 📌 **Revision Tip:** Know that full Karatsuba multiplication (true D&C, O(n^1.585)) exists as a follow-up "can you do better?" question, even if LC 43 itself doesn't require it.

## Lecture 8.4 — Divide and Conquer: Recursion Trees
### What this lecture teaches
How to analyze recursive algorithms' complexity by drawing out the recursion tree and summing work per level (Master Theorem intuition).
### Core DSA ideas
This is the analytical tool used to justify the complexity of **every backtracking problem below** — most backtracking solutions are "exponential but pruned," and recursion-tree thinking is exactly how you reason about that.
### Relevant NeetCode problems — Backtracking begins here (secondary fit, see sequencing note above)

#### LC 78 — Subsets
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Include/Exclude decision tree
- **Pattern:** Backtracking, binary include/exclude choice at each index
- **Why here:** The cleanest possible backtracking template — at each index, recurse twice (include the element, then exclude it) — directly visualized as the recursion tree just taught in 8.4.
- **Prerequisites:** Recursion comfort; recursion-tree visualization (8.4).
- **Best approach:** Recursive helper with a `path` list and current index; at each call, add `path` to results, then recurse including `nums[i]`, backtrack (remove it), recurse excluding it.
- **Time Complexity:** O(2ⁿ) — the recursion tree has 2ⁿ leaves, exactly matching 8.4's tree-counting framework.
- **Space Complexity:** O(n) recursion depth, O(2ⁿ × n) for all output subsets.
- ⚠️ **Common Mistakes:** Forgetting to backtrack (remove the last added element) before trying the next branch, causing corrupted `path` state across recursive calls.
- **Interview Value:** Very High — the canonical backtracking template problem.
- **Related Problems:** LC 90, LC 46, LC 39.
- **Notes:** 💡 **Pattern Recognition:** "all subsets/combinations" → backtracking include/exclude template; memorize this exact skeleton.

#### LC 39 — Combination Sum
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Choice-with-repetition + pruning
- **Pattern:** Backtracking with a remaining-target sum and reusable elements
- **Why here:** Direct extension of LC 78's template, adding a pruning condition (stop if remaining target goes below 0) and allowing element reuse — natural second backtracking problem.
- **Prerequisites:** LC 78.
- **Best approach:** Recursive helper tracking remaining target and a start index (to allow reuse of the current element but never go backward, avoiding duplicate combinations); prune branches where remaining target < 0.
- **Time Complexity:** O(2^target) worst case, problem-dependent.
- **Space Complexity:** O(target / min(candidates)) recursion depth.
- ⚠️ **Common Mistakes:** Allowing the recursion to revisit earlier indices, causing duplicate combinations in different orders.
- **Interview Value:** High.
- **Related Problems:** LC 40, LC 78, LC 17.
- **Notes:** 📌 **Revision Tip:** The "don't go backward in index, but allow staying at the same index" trick (for reuse) is the key mechanical detail — isolate and practice it specifically.

#### LC 46 — Permutations
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Used-tracking + full-length paths
- **Pattern:** Backtracking with a "used" set/array
- **Why here:** A different backtracking shape from LC 78/39 — every element must be used exactly once, in every order, requiring a `used` tracker rather than an index-based "don't go back" rule.
- **Prerequisites:** LC 78, LC 39.
- **Best approach:** Recursive helper with a `path` and a `used` boolean array; at each call, try every unused element, mark it used, recurse, then backtrack (unmark).
- **Time Complexity:** O(n!)
- **Space Complexity:** O(n) recursion depth, O(n! × n) for all outputs.
- ⚠️ **Common Mistakes:** Forgetting to unmark an element as unused during backtracking, which silently corrupts later branches.
- **Interview Value:** High.
- **Related Problems:** LC 78, LC 90.
- **Notes:** 💡 **Pattern Recognition:** "all orderings/arrangements" → backtracking with a `used` tracker, not an index-based skip rule.

#### LC 90 — Subsets II
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Duplicate-skipping at the same recursion level
- **Pattern:** Backtracking + sort + same-level duplicate skip
- **Why here:** Direct extension of LC 78, adding the classic "sort first, then skip duplicates at the same recursion depth" technique needed whenever input has duplicate values.
- **Prerequisites:** LC 78 must be solid.
- **Best approach:** Sort input first; in the loop at each recursion level, skip an element if it equals the previous element *and* the previous element was not included in the current path (i.e., skip same-level duplicates, not same-branch reuse).
- **Time Complexity:** O(2ⁿ)
- **Space Complexity:** O(n) recursion depth.
- ⚠️ **Common Mistakes:** Confusing "skip if same as previous in the array" with "skip if same as previous *and only if the previous wasn't chosen this level*" — the second is the correct condition.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 78, LC 40.
- **Notes:** ⚠️ **Common Trap:** This same-level-duplicate-skip pattern is one of the top three sources of backtracking bugs — drill it deliberately.

#### LC 40 — Combination Sum II
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Combines LC 39's pruning with LC 90's duplicate-skip
- **Pattern:** Backtracking, sort + duplicate-skip + no-reuse + target pruning
- **Why here:** A direct synthesis problem — combines every backtracking technique learned so far (target pruning from LC 39, duplicate-skipping from LC 90), each element usable only once.
- **Prerequisites:** LC 39 and LC 90 both solid.
- **Best approach:** Sort; recursive helper advancing the start index strictly forward (no reuse) while skipping same-level duplicates and pruning when remaining target < 0.
- **Time Complexity:** O(2ⁿ)
- **Space Complexity:** O(n) recursion depth.
- ⚠️ **Common Mistakes:** Mixing up the "allow reuse" index logic from LC 39 with this problem's "no reuse" requirement.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 39, LC 90.
- **Notes:** Excellent synthesis checkpoint — if this is easy, your backtracking fundamentals are solid.

#### LC 79 — Word Search
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Grid DFS with path-marking and unmarking
- **Pattern:** Backtracking on a grid (DFS with temporary cell-marking)
- **Why here:** Applies backtracking to a 2D grid context (connecting back to Week 4's grid traversal), introducing the "mark visited, recurse, then unmark" backtracking discipline in a spatial setting.
- **Prerequisites:** Week 4 grid DFS comfort; LC 78-level backtracking discipline.
- **Best approach:** DFS from each starting cell matching the first letter; temporarily mark the current cell visited (e.g., overwrite with a sentinel), recurse into 4 directions matching subsequent letters, then restore the cell's original value on backtrack.
- **Time Complexity:** O(rows × cols × 4^L) where L is word length.
- **Space Complexity:** O(L) recursion depth.
- ⚠️ **Common Mistakes:** Using a separate visited set instead of in-place marking (works, but slightly less elegant); forgetting to restore the cell value after backtracking.
- **Interview Value:** High.
- **Related Problems:** LC 212, LC 200.
- **Notes:** 💡 **Pattern Recognition:** "search for a path/word in a grid" → backtracking DFS with mark-and-restore.

#### LC 131 — Palindrome Partitioning
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → String partition exploration
- **Pattern:** Backtracking over partition points, with a palindrome-check pruning condition
- **Why here:** Applies the backtracking template to string partitioning instead of array subsets — natural next variation.
- **Prerequisites:** LC 78-level backtracking; palindrome-checking (LC 125 mental model, Week 3).
- **Best approach:** At each recursion call, try every possible prefix of the remaining string; if it's a palindrome, recurse on the rest; backtrack by popping the path after each attempt.
- **Time Complexity:** O(n × 2ⁿ) worst case.
- **Space Complexity:** O(n) recursion depth.
- ⚠️ **Common Mistakes:** Re-checking palindrome status with a fresh O(n) scan every time instead of optionally precomputing a palindrome-validity table (acceptable for first pass, but know the optimization exists).
- **Interview Value:** Medium-High.
- **Related Problems:** LC 5, LC 647.
- **Notes:** 📌 **Revision Tip:** For a faster revisit, precompute an `is_palindrome[i][j]` DP table before backtracking — a nice DP+backtracking hybrid worth knowing.

#### LC 17 — Letter Combinations of a Phone Number
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Cartesian-product-style exploration
- **Pattern:** Backtracking over a fixed mapping (digit → letters)
- **Why here:** A simpler, very approachable backtracking problem — good to solve early in the backtracking block for confidence, despite being introduced slightly later in this listing for grouping clarity.
- **Prerequisites:** LC 78-level template comfort.
- **Best approach:** Recursive helper builds a path letter by letter, branching over all letters mapped to the current digit, until the path length equals the input length.
- **Time Complexity:** O(4ⁿ) worst case (some digits map to 4 letters).
- **Space Complexity:** O(n) recursion depth.
- ⚠️ **Common Mistakes:** Off-by-one in digit-to-letter mapping (especially digits 7 and 9, which map to 4 letters instead of 3).
- **Interview Value:** Medium-High.
- **Related Problems:** LC 78, LC 46.
- **Notes:** Good "easy win" backtracking problem to build momentum.

#### LC 51 — N-Queens
- **Difficulty:** Hard
- **Priority:** P1
- **Mapped to:** Week 8 → Lecture 8.4 → Backtracking → Constraint-based pruning
- **Pattern:** Backtracking with multi-directional constraint checking (row, column, both diagonals)
- **Why here:** The most advanced backtracking problem in NC150 — synthesizes everything (recursive choice exploration, pruning, mark/unmark) with a genuinely non-trivial constraint set (diagonals).
- **Prerequisites:** All prior backtracking problems in this section should be solid first.
- **Best approach:** Place queens row by row; track occupied columns and both diagonal sets (`row - col` and `row + col` are constant along each diagonal) to check placement validity in O(1); backtrack by removing the queen and its tracked constraints.
- **Time Complexity:** O(n!) worst case, heavily pruned in practice.
- **Space Complexity:** O(n) for tracking sets, O(n) recursion depth.
- ⚠️ **Common Mistakes:** Checking diagonal conflicts with an O(n) scan instead of using the `row-col`/`row+col` constant-diagonal trick, which turns each check into O(1).
- **Interview Value:** High (a favorite "hard backtracking" interview question at top companies).
- **Related Problems:** LC 51 is somewhat standalone in NC150, but shares DNA with LC 79.
- **Notes:** 📌 **Revision Tip:** Memorize the `row-col` / `row+col` diagonal-identification trick — it generalizes to many other diagonal-constraint problems beyond N-Queens.

### What should be solved immediately after Lecture 8.4
LC 78, LC 39, LC 46, LC 79, LC 17, LC 51 (P1).

### What should be solved during revision
LC 90, LC 40, LC 131 (P2).

## Lecture 8.5 — Divide and Conquer: Quick Select
### What this lecture teaches
Quick Select algorithm — a Quicksort-derived selection algorithm that finds the kth smallest/largest element in average O(n) time by only recursing into the relevant partition.
### Core DSA ideas
Directly reuses Week 3's partitioning logic, but now only recurses one side instead of both — the key insight that drops complexity from O(n log n) sorting to O(n) average selection.
### Relevant NeetCode problems

#### LC 215 — Kth Largest Element in an Array *(Quick Select — optimal approach)*
- **Difficulty:** Medium
- **Priority:** P1 *(final, optimal-approach pass — heap approach was P2 in Week 6)*
- **Mapped to:** Week 8 → Lecture 8.5 → Divide & Conquer → Quick Select
- **Pattern:** Quick Select (partition + recurse into only the needed side)
- **Why here:** This is the formal, optimal-complexity home for LC 215 — re-solve it here using Quick Select after having solved it with a heap in Week 6, explicitly comparing O(n log k) vs O(n) average.
- **Prerequisites:** Week 3's partition logic (Lecture 3.1–3.3); LC 215's heap-based solution from Week 6.
- **Best approach:** Partition the array around a pivot; if the pivot's final index matches the target rank, return it; otherwise recurse into only the side that contains the target rank.
- **Time Complexity:** O(n) average; O(n²) worst case (mitigated with random pivot selection).
- **Space Complexity:** O(1) iterative; O(log n) average recursive call stack.
- ⚠️ **Common Mistakes:** Recursing into both partitions (turning it back into Quicksort, losing the O(n) average advantage); not randomizing the pivot, risking worst-case behavior on adversarial input.
- **Interview Value:** Very High — explicitly testing Quick Select mastery is common at top-tier interviews.
- **Related Problems:** LC 347, LC 973, LC 703 (compare all approaches).
- **Notes:** 📌 **Revision Tip:** This is the single best problem to rehearse "three solutions, three complexities" (sort O(n log n), heap O(n log k), Quick Select O(n) average) — practice articulating all three and their tradeoffs out loud.

### What should be solved immediately after Lecture 8.5
LC 215 (P1, final pass with Quick Select).

## Lecture 8.6 — Implementation of Quick Select and Fast Select Algorithms
### What this lecture teaches
Hands-on coding of Quick Select (and "Fast Select," a deterministic-pivot variant with guaranteed O(n) worst case, e.g., median-of-medians).
### Core DSA ideas
Implementation fluency — translating 8.5's theory into bug-free, randomized-pivot code.
### Relevant NeetCode problems
None new — use this lecture to re-implement LC 215's Quick Select from scratch without notes, including random pivot selection, as a fluency check before moving to Week 9.

### What should be solved immediately after Week 8
LC 78, LC 39, LC 46, LC 79, LC 17, LC 51, LC 215 (P1).

### What should be solved during revision
LC 90, LC 40, LC 131, LC 43 (P2).

### What should be left for later
Counting Inversions, Closest Pair of Points, Karatsuba Integer Multiplication, Huffman Coding (from Week 7) — all theory-only, no direct NC150 mapping.

---

# Week 9 — Dynamic Programming

**Lectures covered:** 9.1 – 9.6
**Main topic:** Dynamic Programming foundations — recurrence relations, memoization, classic grid-path counting, subsequence/subword problems, edit distance, and matrix-chain multiplication.
**DSA pattern introduced:** Top-down memoization, bottom-up tabulation, 1D DP, 2D DP (grid DP, string DP), interval DP.

> 📌 This is the largest single-week problem set in this handbook, reflecting how heavily NeetCode 150 weights Dynamic Programming relative to a single IITM week. Problems are grouped by DP sub-pattern (1D DP, 2D Grid/String DP) rather than strictly by sub-lecture, since IITM's 9.1–9.6 progression is itself organized by increasing DP complexity, which naturally mirrors NC150's own DP groupings (NeetCode's own "1-D DP" and "2-D DP" categories).

## Lecture 9.1 — Dynamic Programming
### What this lecture teaches
The core DP idea: optimal substructure + overlapping subproblems, motivated by naive exponential recursion (e.g., Fibonacci) being collapsed via caching.
### Core DSA ideas
The conceptual foundation for every problem in this week.
### Relevant NeetCode problems — 1D DP, foundational

#### LC 70 — Climbing Stairs
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.1 → Dynamic Programming → 1D DP, Fibonacci-style recurrence
- **Pattern:** 1D DP, `dp[i] = dp[i-1] + dp[i-2]`
- **Why here:** The canonical first DP problem — it **is** the Fibonacci example most DP lectures (including this one) use to motivate memoization, almost unchanged.
- **Prerequisites:** Recursion (Week 1); recognizing overlapping subproblems.
- **Best approach:** Bottom-up with two rolling variables (no need for a full array): `a, b = 1, 1; for _ in range(n): a, b = b, a+b`.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1) with rolling variables; O(n) with a full array (also acceptable).
- ⚠️ **Common Mistakes:** Writing the naive exponential recursion without memoization (correct but O(2ⁿ), defeating the point of the lecture).
- **Interview Value:** Medium (too simple to be the main question, but a perfect warm-up).
- **Related Problems:** LC 746, LC 198.
- **Notes:** 💡 **Pattern Recognition:** "count ways to reach step n, where each step has a small fixed set of move sizes" → 1D DP, Fibonacci-shaped recurrence.

#### LC 746 — Min Cost Climbing Stairs
- **Difficulty:** Easy
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.1 → Dynamic Programming → 1D DP with cost minimization
- **Pattern:** 1D DP, `dp[i] = cost[i] + min(dp[i-1], dp[i-2])`
- **Why here:** Direct variant of LC 70 — same recurrence shape, but minimizing cost instead of counting paths.
- **Prerequisites:** LC 70.
- **Best approach:** Bottom-up with two rolling variables tracking minimum cost to reach each step.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Off-by-one on whether you need to reach index n or n-1 as the "top" (careful reading of problem statement required).
- **Interview Value:** Medium.
- **Related Problems:** LC 70, LC 198.
- **Notes:** Solve immediately after LC 70 — same recurrence, different objective function.

#### LC 198 — House Robber
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.1 → Dynamic Programming → 1D DP with adjacency-exclusion constraint
- **Pattern:** 1D DP, `dp[i] = max(dp[i-1], dp[i-2] + nums[i])`
- **Why here:** Introduces the "include or exclude, with a constraint on adjacent inclusion" DP shape — a slightly richer recurrence than LC 70/746.
- **Prerequisites:** LC 70, LC 746.
- **Best approach:** Two rolling variables tracking "max if we rob up to i-1" and "max if we rob up to i-2"; at each house, decide to skip or rob.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Greedily robbing every other house without considering that skipping two in a row might sometimes be better — must use the DP recurrence, not a fixed pattern.
- **Interview Value:** Very High — one of the most iconic DP interview questions.
- **Related Problems:** LC 213, LC 746.
- **Notes:** 💡 **Pattern Recognition:** "maximize sum, but can't pick two adjacent elements" → this exact DP recurrence.

#### LC 213 — House Robber II
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.1 → Dynamic Programming → 1D DP applied twice (circular constraint handling)
- **Pattern:** Same as LC 198, run twice on two linear sub-cases
- **Why here:** Direct extension of LC 198 — the houses are arranged in a circle, so you solve the linear LC 198 problem twice (excluding the first house once, excluding the last house once) and take the max.
- **Prerequisites:** LC 198 must be completely solid.
- **Best approach:** Run the LC 198 logic on `nums[:-1]` and on `nums[1:]` separately; return the max of both results (handles the circular wraparound by simply forbidding one of the two "ends" each time).
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)
- ⚠️ **Common Mistakes:** Trying to handle the circular constraint inside a single DP pass instead of decomposing into two linear sub-problems.
- **Interview Value:** High.
- **Related Problems:** LC 198.
- **Notes:** Good test of whether you can decompose a "circular" constraint into two linear DP calls — a reusable trick.

### What should be solved immediately after Lecture 9.1
LC 70, LC 746, LC 198, LC 213 (P1).

## Lecture 9.2 — Memoization
### What this lecture teaches
Top-down DP: writing the natural recursive solution first, then adding a cache (memo dict/array) to eliminate repeated subproblem computation.
### Core DSA ideas
Top-down memoization as an alternative (often easier to derive) to bottom-up tabulation — both covered here.
### Relevant NeetCode problems — 1D DP, string-decoding/word-breaking flavor

#### LC 91 — Decode Ways
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.2 → Dynamic Programming → 1D DP with conditional branching (top-down memoization fits naturally)
- **Pattern:** 1D DP / memoized recursion, branching on 1-digit vs 2-digit decode validity
- **Why here:** A natural top-down memoization problem — the recursive structure ("ways to decode the rest of the string") is more intuitive to derive recursively first, then memoize, exactly as 9.2 teaches.
- **Prerequisites:** LC 70's recurrence-shape comfort; string indexing.
- **Best approach:** `dp[i]` = ways to decode `s[i:]`; at each position, try a 1-digit decode (if nonzero) and a 2-digit decode (if it forms a valid 10–26 value), summing valid branches.
- **Time Complexity:** O(n)
- **Space Complexity:** O(n) memo array; O(1) with rolling variables.
- ⚠️ **Common Mistakes:** Forgetting that a leading `'0'` is never independently decodable, and forgetting to validate the two-digit case is ≤ 26.
- **Interview Value:** High.
- **Related Problems:** LC 70, LC 139.
- **Notes:** ⚠️ **Common Trap:** Edge cases around `'0'` (both as a single digit and within a 2-digit pair) are the most common source of bugs.

#### LC 322 — Coin Change
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.2 → Dynamic Programming → 1D DP, unbounded knapsack-style minimization
- **Pattern:** 1D DP, `dp[amount] = min(dp[amount - coin] + 1 for valid coins)`
- **Why here:** The canonical "minimum number of items to reach a target" DP problem — natural memoization candidate (top-down: "minimum coins to make amount X" recurses into smaller amounts).
- **Prerequisites:** LC 70/198-level DP recurrence comfort.
- **Best approach:** Bottom-up `dp` array indexed by amount, `dp[0] = 0`; for each amount, try every coin and take the minimum.
- **Time Complexity:** O(amount × number of coin types)
- **Space Complexity:** O(amount)
- ⚠️ **Common Mistakes:** Using a greedy "always use the largest coin first" approach, which fails for non-canonical coin systems (this is a DP problem, not a greedy one — a frequent misconception).
- **Interview Value:** Very High.
- **Related Problems:** LC 518, LC 139.
- **Notes:** 💡 **Pattern Recognition:** "minimum/maximum count to reach a target using a given set of items, reuse allowed" → unbounded-knapsack-style 1D DP, never greedy.

#### LC 139 — Word Break
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.2 → Dynamic Programming → 1D DP / memoized recursion, boolean feasibility
- **Pattern:** 1D DP, `dp[i] = any(dp[j] and s[j:i] in wordSet for valid j)`
- **Why here:** Another textbook top-down memoization candidate — the recursive question "can the rest of the string be segmented?" memoizes cleanly per starting index.
- **Prerequisites:** LC 91 (similar string-position-indexed DP).
- **Best approach:** `dp[i]` = True if `s[:i]` can be segmented using dictionary words; for each `i`, check all `j < i` where `dp[j]` is True and `s[j:i]` is in the word set.
- **Time Complexity:** O(n²) (or O(n² ) with set lookups, sometimes O(n³) if substring slicing cost is counted).
- **Space Complexity:** O(n)
- ⚠️ **Common Mistakes:** Re-deriving this with plain backtracking and no memoization, causing exponential blowup on adversarial inputs.
- **Interview Value:** High.
- **Related Problems:** LC 322, LC 91.
- **Notes:** 📌 **Revision Tip:** Convert the word list to a set first — checking substring membership against a list is a silent O(n) per check that destroys the intended complexity.

### What should be solved immediately after Lecture 9.2
LC 91, LC 322, LC 139 (P1).

## Lecture 9.3 — Grid Paths
### What this lecture teaches
2D DP for counting/optimizing paths through a grid (e.g., counting unique paths from top-left to bottom-right with only right/down moves).
### Core DSA ideas
2D DP — the recurrence now depends on two indices instead of one, with values typically derived from the cell above and the cell to the left.
### Relevant NeetCode problems

#### LC 62 — Unique Paths
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.3 → Dynamic Programming → 2D Grid DP
- **Pattern:** 2D DP, `dp[i][j] = dp[i-1][j] + dp[i][j-1]`
- **Why here:** This **is** the textbook grid-path-counting problem from 9.3, almost unchanged.
- **Prerequisites:** 1D DP comfort from 9.1/9.2; 2D array indexing.
- **Best approach:** Bottom-up 2D table (or a rolling 1D array to save space), where each cell's count is the sum of the cell above and the cell to the left; first row/column are all 1.
- **Time Complexity:** O(rows × cols)
- **Space Complexity:** O(rows × cols), reducible to O(cols) with a rolling 1D array.
- ⚠️ **Common Mistakes:** Forgetting to initialize the first row and first column correctly (each has exactly 1 path, since there's only one way to reach them).
- **Interview Value:** High.
- **Related Problems:** LC 329 (different grid DP flavor, Week 4).
- **Notes:** 💡 **Pattern Recognition:** "count paths in a grid moving only right/down" → 2D DP summing top and left neighbors.

### What should be solved immediately after Lecture 9.3
LC 62 (P1).

## Lecture 9.4 — Common Subwords and Subsequences
### What this lecture teaches
2D string DP for problems like Longest Common Subsequence — comparing two strings character by character with a 2D table.
### Core DSA ideas
The single most important 2D DP shape for string problems: `dp[i][j]` represents some property of `s1[:i]` and `s2[:j]`.
### Relevant NeetCode problems

#### LC 1143 — Longest Common Subsequence
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.4 → Dynamic Programming → 2D String DP
- **Pattern:** 2D DP, `dp[i][j] = dp[i-1][j-1] + 1` if chars match, else `max(dp[i-1][j], dp[i][j-1])`
- **Why here:** This **is** the lecture's titular example — the canonical two-string DP problem, and the base pattern for every other 2D string DP problem this week.
- **Prerequisites:** LC 62's 2D table comfort.
- **Best approach:** 2D table where `dp[i][j]` = LCS length of `text1[:i]` and `text2[:j]`; fill using the match/no-match recurrence above.
- **Time Complexity:** O(n × m)
- **Space Complexity:** O(n × m), reducible to O(min(n,m)) with rolling rows.
- ⚠️ **Common Mistakes:** Off-by-one in indexing between the 1-indexed DP table and 0-indexed strings (a near-universal source of bugs in 2D string DP).
- **Interview Value:** Very High — the base pattern for an enormous number of string DP interview questions.
- **Related Problems:** LC 72, LC 97, LC 115, LC 5, LC 647.
- **Notes:** 📌 **Revision Tip:** Memorize this exact recurrence cold — nearly every other 2D string DP problem in this handbook is a variant of it.

#### LC 309 — Best Time to Buy and Sell Stock with Cooldown
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 9 → Lecture 9.4 (secondary fit: state-machine DP, not literally subsequence-comparison, but shares the "DP over sequence positions with multiple states" spirit)
- **Pattern:** State-machine DP (holding / not-holding / cooldown states)
- **Why here:** A different DP "shape" than LCS — instead of comparing two strings, you track multiple parallel states per day — included here as the natural next escalation once 2D-table thinking (9.4) is comfortable, before moving to even more complex multi-dimensional DP later.
- **Prerequisites:** LC 198 (decision-based DP) helps conceptually.
- **Best approach:** Track three rolling states per day: `held` (max profit if holding a stock), `sold` (max profit if just sold today, triggering cooldown), `rest` (max profit if not holding and not in cooldown); transition between them daily.
- **Time Complexity:** O(n)
- **Space Complexity:** O(1) with rolling states.
- ⚠️ **Common Mistakes:** Forgetting that after selling, you must skip exactly one day before being allowed to buy again — incorrectly allowing a buy on the very next day.
- **Interview Value:** Medium-High.
- **Related Problems:** LC 121 (Week 3, simpler buy/sell), LC 198.
- **Notes:** 💡 **Pattern Recognition:** "sequence of decisions with mutually exclusive states that change daily" → state-machine DP with rolling state variables.

### What should be solved immediately after Lecture 9.4
LC 1143 (P1).

### What should be solved during revision
LC 309 (P2).

## Lecture 9.5 — Edit Distance
### What this lecture teaches
The classic Edit Distance (Levenshtein distance) 2D DP problem — minimum insertions/deletions/substitutions to transform one string into another.
### Core DSA ideas
A direct generalization of LC 1143's 2D string DP shape, now with three possible transitions (insert, delete, substitute) instead of two.
### Relevant NeetCode problems

#### LC 72 — Edit Distance
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 9 → Lecture 9.5 → Dynamic Programming → 2D String DP, three-way transition
- **Pattern:** 2D DP, `dp[i][j] = dp[i-1][j-1]` if chars match, else `1 + min(insert, delete, replace)`
- **Why here:** This **is** the lecture's exact titular problem — solve it immediately after 9.5, building directly on LC 1143's table-filling mechanics.
- **Prerequisites:** LC 1143 must be solid.
- **Best approach:** 2D table; if characters match, inherit diagonal value; otherwise take `1 + min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1])` (delete, insert, replace respectively).
- **Time Complexity:** O(n × m)
- **Space Complexity:** O(n × m), reducible to O(min(n,m)).
- ⚠️ **Common Mistakes:** Mixing up which of the three neighboring cells corresponds to insert vs delete (the direction depends on which string is rows vs columns — easy to flip).
- **Interview Value:** Very High — an extremely common "hard DP" interview question.
- **Related Problems:** LC 1143, LC 97, LC 115.
- **Notes:** 📌 **Revision Tip:** Draw the table by hand once with a tiny example (e.g., "ab" → "ba") to viscerally confirm which neighbor corresponds to which operation.

#### LC 97 — Interleaving String
- **Difficulty:** Medium
- **Priority:** P2
- **Mapped to:** Week 9 → Lecture 9.5 → Dynamic Programming → 2D String DP, boolean feasibility
- **Pattern:** 2D DP, `dp[i][j]` = can `s3[:i+j]` be formed by interleaving `s1[:i]` and `s2[:j]`
- **Why here:** A boolean-feasibility variant of the same 2D string DP shape, escalating naturally after Edit Distance's three-way numeric transition.
- **Prerequisites:** LC 72, LC 1143.
- **Best approach:** 2D boolean table; `dp[i][j]` is True if (`dp[i-1][j]` is True and `s1[i-1] == s3[i+j-1]`) or (`dp[i][j-1]` is True and `s2[j-1] == s3[i+j-1]`).
- **Time Complexity:** O(n × m)
- **Space Complexity:** O(n × m), reducible to O(min(n,m)).
- ⚠️ **Common Mistakes:** Forgetting the early length-mismatch check (`len(s1) + len(s2) != len(s3)` → immediately False).
- **Interview Value:** Medium.
- **Related Problems:** LC 72, LC 1143.
- **Notes:** Good test of whether 2D DP table-filling is automatic, since the recurrence itself is conceptually simple but easy to mis-index.

#### LC 115 — Distinct Subsequences
- **Difficulty:** Hard
- **Priority:** P3
- **Mapped to:** Week 9 → Lecture 9.5 → Dynamic Programming → 2D String DP, counting variant
- **Pattern:** 2D DP, counting distinct ways `t` appears as a subsequence of `s`
- **Why here:** A counting variant of the LCS/Edit-Distance table shape — included here for thematic continuity, but deferred (P3) since it's one of the less frequently asked 2D string DP problems.
- **Prerequisites:** LC 1143, LC 72.
- **Best approach:** `dp[i][j]` = number of ways `t[:j]` appears as a subsequence of `s[:i]`; `dp[i][j] = dp[i-1][j]` plus `dp[i-1][j-1]` if `s[i-1] == t[j-1]`.
- **Time Complexity:** O(n × m)
- **Space Complexity:** O(n × m), reducible to O(m).
- ⚠️ **Common Mistakes:** Initializing the base case incorrectly (`dp[i][0] = 1` for all i, since an empty `t` has exactly one — the empty — subsequence match).
- **Interview Value:** Medium (less common than LC 72/1143, but a good "hard mode" 2D DP drill).
- **Related Problems:** LC 1143, LC 72.
- **Notes:** Defer full mastery to a dedicated revision pass.

### What should be solved immediately after Lecture 9.5
LC 72 (P1).

### What should be solved during revision
LC 97 (P2), LC 115 (P3).

## Lecture 9.6 — Matrix Multiplication
### What this lecture teaches
Matrix Chain Multiplication — interval DP to find the optimal order of multiplying a chain of matrices to minimize scalar multiplications.
### Core DSA ideas
**Interval DP** — a third major DP "shape" (after 1D and 2D-string), where `dp[i][j]` represents the optimal cost for the *interval* from i to j, and the recurrence tries every possible "split point" k within that interval.
### Relevant NeetCode problems

#### LC 312 — Burst Balloons
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 9 → Lecture 9.6 → Dynamic Programming → Interval DP
- **Pattern:** Interval DP, `dp[i][j] = max over k in (i,j) of dp[i][k] + dp[k][j] + cost(i,k,j)`
- **Why here:** This is the direct NC150 analogue of Matrix Chain Multiplication's interval DP shape — instead of minimizing multiplication cost over a matrix chain, you maximize coin collection over balloon-bursting order, but the "try every split point within an interval" recurrence is structurally identical.
- **Prerequisites:** Comfortable with 2D DP tables (9.3–9.5); the conceptual leap of indexing by *interval* rather than *prefix*.
- **Best approach:** Pad the array with 1s on both ends; `dp[i][j]` = max coins from fully bursting all balloons strictly between i and j, trying every `k` as the *last* balloon burst in that range, since `nums[i]` and `nums[j]` survive until then.
- **Time Complexity:** O(n³)
- **Space Complexity:** O(n²)
- ⚠️ **Common Mistakes:** Thinking of `k` as the *first* balloon burst (which couples the two sub-intervals and breaks the DP) instead of the *last* balloon burst (which correctly decouples them, since the two sides never interact once boundaries `i` and `j` are fixed as survivors).
- **Interview Value:** Medium (a "show you've mastered interval DP" problem rather than a frequent generic ask).
- **Related Problems:** LC 1143, LC 72 (different DP shapes, useful contrast).
- **Notes:** ⚠️ **Common Trap:** The "think about which balloon bursts *last*, not first" reframing is the single hardest insight in this problem — internalize it explicitly, don't just memorize the code.

### What should be solved during revision
LC 312 (P2) — best attempted only once 1D and 2D-string DP are both completely automatic; interval DP is the hardest DP shape in this handbook.

### What should be solved immediately after Week 9
LC 70, LC 746, LC 198, LC 213, LC 91, LC 322, LC 139, LC 62, LC 1143, LC 72 (P1).

### What should be left for later
- **LC 152 — Maximum Product Subarray**, **LC 300 — Longest Increasing Subsequence**, **LC 416 — Partition Equal Subset Sum**, **LC 518 — Coin Change II**, **LC 494 — Target Sum**, **LC 5 — Longest Palindromic Substring**, **LC 647 — Palindromic Substrings**, **LC 10 — Regular Expression Matching** — these are all genuine DP problems thematically belonging to this week, but they are placed in **Appendix E (Extra/Later)** rather than forced into a specific sub-lecture, because IITM's 9.1–9.6 sequence does not explicitly cover knapsack-style subset-sum DP, Kadane's-style subarray DP, palindrome-interval DP, or automaton-based regex DP as named topics. They are NOT mapped to a fabricated lecture — see Appendix E for their full treatment, priority, and why they still matter for interviews.

---

# Week 10 — String Matching & Tries

**Lectures covered:** 10.1 – 10.7
**Main topic:** Classical string-matching algorithms (Boyer-Moore, Rabin-Karp, Automata-based, Knuth-Morris-Pratt), followed by Tries and Regular Expressions.
**DSA pattern introduced:** Pattern matching (various), Trie data structure, automaton-based matching (conceptual link to Regex DP).

## Lecture 10.1 — String Matching
### What this lecture teaches
The general string-matching problem statement and the naive O(n×m) brute-force baseline that motivates every algorithm that follows.
### Core DSA ideas
Baseline complexity to beat.
### Relevant NeetCode problems
None directly — conceptual setup. NeetCode 150 does not include a "find all occurrences of pattern in text" style problem requiring Boyer-Moore/Rabin-Karp/KMP explicitly.

## Lecture 10.2 — String Matching: Boyer-Moore Algorithm
## Lecture 10.3 — String Matching: Rabin-Karp Algorithm
## Lecture 10.4 — String Matching Using Automata
## Lecture 10.5 — String Matching: Knuth-Morris-Pratt Algorithm
### What these lectures teach
Four distinct algorithmic strategies for the same underlying problem (find pattern P in text T faster than brute force): bad-character/good-suffix heuristics (Boyer-Moore), rolling hash (Rabin-Karp), deterministic finite automaton matching (Automata), and the failure-function/prefix-function approach (KMP).
### Core DSA ideas
None of these map to a direct NeetCode 150 problem requiring their specific implementation.
### Relevant NeetCode problems
**Flagged as Interview Extra / Theory-Only for NC150 purposes.** No problem in NeetCode 150 requires implementing Boyer-Moore, Rabin-Karp, automaton-matching, or KMP directly. These remain valuable general CS knowledge (and occasionally appear as a follow-up "can you do this faster than brute force?" question after solving a basic substring search), but this handbook will not force a mapping here, per the explicit instruction not to force unnatural fits.
📌 **Revision Tip:** If your interview pipeline includes companies known for asking string-matching internals (rare outside specialized roles), revisit these four lectures' theory directly rather than looking for a NeetCode problem — none exists in this list.

## Lecture 10.6 — String Matching: Tries
### What this lecture teaches
The Trie (prefix tree) data structure — nodes represent characters, paths represent strings, enabling efficient prefix-based search/insert.
### Core DSA ideas
**Trie** as a named, formal data structure — its proper syllabus home.
### Relevant NeetCode problems

#### LC 208 — Implement Trie (Prefix Tree)
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 10 → Lecture 10.6 → Trie → Core Insert/Search/StartsWith
- **Pattern:** Trie construction and traversal
- **Why here:** The direct, foundational implementation of exactly what 10.6 teaches — build this first, before any Trie-based problem-solving.
- **Prerequisites:** Node/class basics (1.7); dict usage for children mapping.
- **Best approach:** Each `TrieNode` holds a dict of `char -> TrieNode` children and an `is_end` flag; `insert` walks/creates nodes character by character; `search`/`startsWith` walk existing nodes and check `is_end` (search only) at the final position.
- **Time Complexity:** O(L) per operation, where L is the word/prefix length.
- **Space Complexity:** O(total characters inserted) worst case.
- ⚠️ **Common Mistakes:** Forgetting the `is_end` flag distinction (a node existing for a prefix doesn't mean that exact prefix was ever inserted as a complete word).
- **Interview Value:** Very High — the foundational data-structure-design problem for Tries.
- **Related Problems:** LC 211, LC 212.
- **Notes:** 📌 **Revision Tip:** Write this from scratch with zero references — it underlies the next two problems entirely.

#### LC 211 — Design Add and Search Words Data Structure
- **Difficulty:** Medium
- **Priority:** P1
- **Mapped to:** Week 10 → Lecture 10.6 → Trie → Wildcard-supporting search via DFS
- **Pattern:** Trie + DFS for wildcard (`.`) matching
- **Why here:** Direct extension of LC 208 — adds a wildcard character that must try all children at that position, requiring a DFS-style search instead of a simple walk.
- **Prerequisites:** LC 208 must be solid.
- **Best approach:** Same Trie structure as LC 208; for `search`, recursively DFS — at a literal character, follow that one child; at `.`, try all children.
- **Time Complexity:** O(L) for words without wildcards; O(26^L) worst case with many wildcards (rare in practice).
- **Space Complexity:** O(total characters inserted)
- ⚠️ **Common Mistakes:** Implementing search iteratively (works for literal characters but breaks once a wildcard requires branching) instead of recursively/DFS-based.
- **Interview Value:** High.
- **Related Problems:** LC 208, LC 212.
- **Notes:** 💡 **Pattern Recognition:** "Trie search with a wildcard" → DFS branching at wildcard positions, not a simple linear walk.

#### LC 212 — Word Search II
- **Difficulty:** Hard
- **Priority:** P1
- **Mapped to:** Week 10 → Lecture 10.6 → Trie → Trie + Backtracking DFS on a grid
- **Pattern:** Trie (for efficient multi-word prefix checking) + grid backtracking (Week 8's LC 79 pattern)
- **Why here:** The capstone Trie problem — synthesizes LC 208's Trie construction with LC 79's (Week 8) grid backtracking, using the Trie to prune search paths that can't possibly lead to any target word.
- **Prerequisites:** LC 208, LC 79 (Week 8) both must be solid.
- **Best approach:** Build a Trie from all target words; DFS/backtrack from every grid cell, walking the Trie alongside the grid path; prune immediately if the current path's prefix doesn't exist in the Trie; mark found words to avoid duplicates.
- **Time Complexity:** O(rows × cols × 4^L) bounded by Trie pruning, much faster in practice than independently searching for each word.
- **Space Complexity:** O(total characters in all words) for the Trie.
- ⚠️ **Common Mistakes:** Searching for each word independently with LC 79's approach instead of building one shared Trie (technically correct but far slower — misses the entire point of the lecture).
- **Interview Value:** Very High — a favorite "combine two data structures" hard interview question.
- **Related Problems:** LC 208, LC 211, LC 79.
- **Notes:** ⚠️ **Common Trap:** Forgetting to remove a found word from the Trie (or mark it found) can cause duplicate results if the same word path is revisited.

### What should be solved immediately after Lecture 10.6
LC 208, LC 211, LC 212 (P1).

## Lecture 10.7 — String Matching: Regular Expressions
### What this lecture teaches
Regular expression matching via finite automata / backtracking, connecting string-matching theory to pattern languages.
### Core DSA ideas
Regex matching as a DP/automaton problem — a direct conceptual bridge back to Week 9's DP.
### Relevant NeetCode problems

#### LC 10 — Regular Expression Matching
- **Difficulty:** Hard
- **Priority:** P2
- **Mapped to:** Week 10 → Lecture 10.7 → String Matching → DP / Top-Down Memoization (secondary fit: also classifiable as Week 9 2D String DP)
- **Pattern:** 2D DP / memoized recursion handling `.` and `*` wildcards
- **Why here:** This is the direct, formal NC150 payoff for Lecture 10.7 — regex matching is exactly the topic taught, and the standard solution technique (memoized recursion over two string positions) is a direct callback to Week 9's 2D string DP shape (LC 1143/72).
- **Prerequisites:** LC 1143/72 (2D string DP); careful case analysis for `*`.
- **Best approach:** Memoized recursion `dp(i, j)` = does `s[i:]` match `p[j:]`; handle `*` by considering both "skip the preceding element + star" and "consume one character of s if it matches the preceding element."
- **Time Complexity:** O(n × m)
- **Space Complexity:** O(n × m) for memo table.
- ⚠️ **Common Mistakes:** Mishandling the `*` operator's "zero or more of the preceding element" semantics, especially the "zero occurrences" branch.
- **Interview Value:** High — a classic "hard DP on strings" interview question.
- **Related Problems:** LC 1143, LC 72 (Week 9).
- **Notes:** 📌 **Revision Tip:** Revisit this explicitly after re-confirming LC 1143/72 are automatic — the case-analysis for `*` is the only genuinely new difficulty here, the DP scaffolding is identical to Week 9.

### What should be solved during revision
LC 10 (P2).

### What should be solved immediately after Week 10
LC 208, LC 211, LC 212 (P1).

### What should be left for later
Boyer-Moore, Rabin-Karp, Automata-matching, KMP — theory-only, no direct NC150 mapping.

---


# Appendix F — Missing NeetCode 150 Problems

The following problems were not covered in the current handbook and should be added using the same structure as the existing entries.

---

# Sliding Window

| Priority | LC No. | Problem                                        |
| -------- | ------ | ---------------------------------------------- |
| P1       | LC 3   | Longest Substring Without Repeating Characters |
| P1       | LC 424 | Longest Repeating Character Replacement        |
| P1       | LC 567 | Permutation in String                          |
| P2       | LC 76  | Minimum Window Substring                       |
| P2       | LC 239 | Sliding Window Maximum                         |

**Recommended Mapping**

* **Week:** Week 3
* **Lecture:** 3.7 – Implementation of Lists in Python
* **Topic:** Arrays & Strings
* **Subtopic:** Sliding Window

---

# Stack

| Priority | LC No. | Problem                          |
| -------- | ------ | -------------------------------- |
| P1       | LC 155 | Min Stack                        |
| P1       | LC 150 | Evaluate Reverse Polish Notation |
| P1       | LC 739 | Daily Temperatures               |
| P2       | LC 853 | Car Fleet                        |
| P2       | LC 84  | Largest Rectangle in Histogram   |

**Recommended Mapping**

* **Week:** Week 3
* **Lecture:** 3.7
* **Topic:** Stack
* **Subtopic:** Monotonic Stack / Design Stack

---

# Binary Search

| Priority | LC No. | Problem                    |
| -------- | ------ | -------------------------- |
| P2       | LC 981 | Time Based Key-Value Store |

**Recommended Mapping**

* **Week:** Week 3
* **Lecture:** Searching & Binary Search
* **Topic:** Binary Search
* **Subtopic:** Binary Search on Answer / Ordered Map

---

# Matrix

| Priority | LC No. | Problem           |
| -------- | ------ | ----------------- |
| P2       | LC 48  | Rotate Image      |
| P2       | LC 54  | Spiral Matrix     |
| P2       | LC 73  | Set Matrix Zeroes |

**Recommended Mapping**

* **Week:** Week 3
* **Topic:** Matrix
* **Subtopic:** Matrix Traversal & Simulation

---

# Math

| Priority | LC No. | Problem         |
| -------- | ------ | --------------- |
| P3       | LC 202 | Happy Number    |
| P3       | LC 66  | Plus One        |
| P3       | LC 7   | Reverse Integer |

**Recommended Mapping**

* **Week:** Week 11
* **Category:** Interview Extras

---

# Bit Manipulation

| Priority | LC No. | Problem             |
| -------- | ------ | ------------------- |
| P2       | LC 136 | Single Number       |
| P2       | LC 191 | Number of 1 Bits    |
| P2       | LC 338 | Counting Bits       |
| P2       | LC 190 | Reverse Bits        |
| P2       | LC 268 | Missing Number      |
| P2       | LC 371 | Sum of Two Integers |

**Recommended Mapping**

* **Week:** Week 11
* **Topic:** Bit Manipulation
* **Subtopic:** Binary Operations

---

# Geometry

| Priority | LC No.  | Problem        |
| -------- | ------- | -------------- |
| P3       | LC 2013 | Detect Squares |

**Recommended Mapping**

* **Week:** Week 11
* **Category:** Interview Extras

---

# Completion Checklist

* [ ] LC 3 — Longest Substring Without Repeating Characters
* [ ] LC 424 — Longest Repeating Character Replacement
* [ ] LC 567 — Permutation in String
* [ ] LC 76 — Minimum Window Substring
* [ ] LC 239 — Sliding Window Maximum
* [ ] LC 155 — Min Stack
* [ ] LC 150 — Evaluate Reverse Polish Notation
* [ ] LC 739 — Daily Temperatures
* [ ] LC 853 — Car Fleet
* [ ] LC 84 — Largest Rectangle in Histogram
* [ ] LC 981 — Time Based Key-Value Store
* [ ] LC 48 — Rotate Image
* [ ] LC 54 — Spiral Matrix
* [ ] LC 73 — Set Matrix Zeroes
* [ ] LC 202 — Happy Number
* [ ] LC 66 — Plus One
* [ ] LC 7 — Reverse Integer
* [ ] LC 136 — Single Number
* [ ] LC 191 — Number of 1 Bits
* [ ] LC 338 — Counting Bits
* [ ] LC 190 — Reverse Bits
* [ ] LC 268 — Missing Number
* [ ] LC 371 — Sum of Two Integers
* [ ] LC 2013 — Detect Squares
