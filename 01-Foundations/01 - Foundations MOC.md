# 01 — Foundations MOC

> ← Back to [[Software Engineering - Map of Content]]

The bedrock of computer science. Everything in software engineering ultimately rests on these concepts.

---

## [[Data Structures]]

### Linear Structures
- **Arrays** — Contiguous memory, O(1) random access, fixed vs dynamic sizing
- **Linked Lists** — Singly, Doubly, Circular; pointer-based traversal, O(1) insert/delete at known position
- **Stacks** — LIFO, call stack, expression evaluation, undo mechanisms
- **Queues** — FIFO, priority queues, deques, circular buffers, BFS applications

### Tree Structures
- **Binary Trees** — Traversals (in-order, pre-order, post-order, level-order)
- **Binary Search Trees (BST)** — Search, insert, delete in O(log n) average
- **Self-Balancing Trees** — AVL trees, Red-Black trees, B-Trees, B+ Trees (used in [[Relational Databases]])
- **Heaps** — Min-heap, Max-heap, binary heap, Fibonacci heap, priority queue implementation
- **Tries (Prefix Trees)** — Autocomplete, spell-checking, IP routing
- **Segment Trees / Fenwick Trees** — Range queries, interval problems

### Graph Structures
- **Representations** — Adjacency list, adjacency matrix, edge list
- **Directed vs Undirected** — DAGs, cyclic graphs, weighted graphs
- **Special Graphs** — Bipartite, planar, sparse vs dense

### Hash-Based Structures
- **Hash Tables / Hash Maps** — Hash functions, collision resolution (chaining, open addressing)
- **Hash Sets** — Membership testing, deduplication
- **Bloom Filters** — Probabilistic membership, false positives, no false negatives
- **Consistent Hashing** — Used in [[Distributed Systems]] for partitioning

### Advanced Structures
- **Disjoint Set / Union-Find** — Connected components, Kruskal's algorithm
- **Skip Lists** — Probabilistic balancing, used in Redis
- **LRU Cache** — Combination of hash map + doubly linked list, used in [[Caching]]
- **Persistent Data Structures** — Immutable variants, structural sharing (used in [[Programming Paradigms|Functional Programming]])

---

## [[Algorithms]]

### Sorting
- **Comparison-Based** — Bubble, Selection, Insertion, Merge Sort, Quick Sort, Heap Sort
- **Non-Comparison** — Counting Sort, Radix Sort, Bucket Sort
- **Hybrid** — Timsort (Python/Java default), Introsort (C++ default)
- **Analysis** — Stability, in-place vs extra space, best/average/worst case

### Searching
- **Linear Search** — O(n), unsorted data
- **Binary Search** — O(log n), sorted data, bisect variants
- **Interpolation Search** — Uniformly distributed data
- **Ternary Search** — Unimodal functions

### Graph Algorithms
- **Traversal** — BFS, DFS, topological sort
- **Shortest Path** — Dijkstra, Bellman-Ford, Floyd-Warshall, A*
- **Minimum Spanning Tree** — Prim's, Kruskal's
- **Network Flow** — Ford-Fulkerson, Edmonds-Karp, max-flow min-cut
- **Strongly Connected Components** — Tarjan's, Kosaraju's
- **Cycle Detection** — Floyd's tortoise and hare, coloring

### Dynamic Programming
- **Core Concepts** — Overlapping subproblems, optimal substructure, memoization vs tabulation
- **Classic Problems** — Knapsack, LCS, LIS, edit distance, matrix chain multiplication, coin change
- **On Trees** — Tree DP, rerooting
- **Bitmask DP** — Subset enumeration, TSP approximation

### Greedy Algorithms
- **Core Concept** — Locally optimal choices lead to global optimum
- **Classic Problems** — Activity selection, Huffman coding, interval scheduling, fractional knapsack

### Backtracking & Recursion
- **Backtracking** — N-Queens, Sudoku solver, constraint satisfaction
- **Divide and Conquer** — Merge sort, quick sort, closest pair of points, Strassen's matrix multiplication
- **Recursion Patterns** — Tail recursion, mutual recursion, recursive descent parsing

### String Algorithms
- **Pattern Matching** — KMP, Rabin-Karp, Boyer-Moore, Aho-Corasick
- **Suffix Structures** — Suffix arrays, suffix trees
- **Edit Distance** — Levenshtein distance, longest common substring

### Randomized & Probabilistic
- **Monte Carlo** — Approximate answers, randomized primality testing
- **Las Vegas** — Always correct, randomized runtime (randomized quicksort)
- **Reservoir Sampling** — Streaming data, uniform sampling
- **HyperLogLog** — Cardinality estimation

---

## [[Computational Complexity]]

### Time Complexity
- **Big-O Notation** — Upper bound, worst case
- **Big-Ω (Omega)** — Lower bound
- **Big-Θ (Theta)** — Tight bound
- **Amortized Analysis** — Average over sequence of operations (e.g., dynamic array resizing)
- **Common Classes** — O(1), O(log n), O(n), O(n log n), O(n²), O(2ⁿ), O(n!)

### Space Complexity
- **Auxiliary Space** — Extra space beyond input
- **In-Place Algorithms** — O(1) extra space
- **Space-Time Tradeoffs** — Hash tables vs sorted arrays, memoization vs recomputation

### Complexity Classes
- **P** — Solvable in polynomial time
- **NP** — Verifiable in polynomial time
- **NP-Complete** — SAT, 3-SAT, traveling salesman (decision), graph coloring
- **NP-Hard** — At least as hard as NP-Complete, may not be in NP
- **P vs NP Problem** — The million-dollar open question
- **PSPACE, EXPTIME** — Higher complexity classes
- **Undecidable Problems** — Halting problem, Rice's theorem

### Reductions
- **Polynomial-Time Reductions** — Proving NP-completeness
- **Problem Transformations** — Reducing unknown to known problem

---

## [[Mathematics for CS]]

### Discrete Mathematics
- **Logic** — Propositional logic, predicate logic, proof techniques (induction, contradiction, pigeonhole)
- **Set Theory** — Sets, relations, functions, cardinality
- **Combinatorics** — Permutations, combinations, binomial coefficients, inclusion-exclusion
- **Graph Theory** — Euler/Hamiltonian paths, planarity, coloring, matching
- **Number Theory** — Modular arithmetic, GCD, primes, Fermat's little theorem (used in [[Cryptography]])
- **Recurrence Relations** — Solving recurrences, Master theorem

### Linear Algebra
- **Vectors and Matrices** — Operations, transpose, inverse
- **Eigenvalues/Eigenvectors** — PCA, spectral methods
- **Matrix Decompositions** — SVD, LU, QR (used in [[ML Fundamentals]])
- **Vector Spaces** — Basis, dimension, linear independence

### Probability & Statistics
- **Probability** — Conditional probability, Bayes' theorem, random variables, distributions
- **Distributions** — Normal, Bernoulli, Binomial, Poisson, Exponential
- **Expectation & Variance** — Linearity of expectation, law of large numbers
- **Statistical Inference** — Hypothesis testing, confidence intervals, p-values
- **Bayesian Statistics** — Prior, posterior, likelihood (used in [[ML Fundamentals]])
- **Markov Chains** — State transitions, steady state, PageRank

### Information Theory
- **Entropy** — Shannon entropy, information content
- **Compression** — Huffman coding, arithmetic coding, LZ77/LZ78
- **Error Correction** — Hamming codes, Reed-Solomon, checksums
- **Channel Capacity** — Shannon's theorem, noise

---

#foundations #cs-fundamentals
